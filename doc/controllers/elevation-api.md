# Elevation API

```java
ElevationApi elevationApi = client.getElevationApi();
```

## Class Name

`ElevationApi`


# Elevation

The Elevation API provides a simple interface to query locations on the earth for elevation data. Additionally, you may request sampled elevation data along paths, allowing you to calculate elevation changes along routes. With the Elevation API, you can develop hiking and biking applications, positioning applications, or low resolution surveying applications.

Elevation data is available for all locations on the surface of the earth, including depth locations on the ocean floor (which return negative values). In those cases where Google does not possess exact elevation measurements at the precise location you request, the service interpolates and returns an averaged value using the four nearest locations. Elevation values are expressed relative to local mean sea level (LMSL).

Requests to the Elevation API utilize different parameters based on whether the request is for discrete locations or for an ordered path. For discrete locations, requests for elevation return data on the specific locations passed in the request; for paths, elevation requests are instead sampled along the given path.

```java
CompletableFuture<ApiResponse<MapsApiElevationJsonResponse>> elevationAsync(
    final List<String> locations,
    final List<String> path,
    final Double samples)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `locations` | `List<String>` | Query, Optional | Positional requests are indicated through use of the locations parameter, indicating elevation requests for the specific locations passed as latitude/longitude values.<br><br>The locations parameter may take the following arguments:<br><br>- A single coordinate: `locations=40.714728,-73.998672`<br>- An array of coordinates separated using the pipe ('\|') character:<br>  ```<br>  locations=40.714728,-73.998672\|-34.397,150.644<br>  ```<br>- A set of encoded coordinates using the [Encoded Polyline Algorithm](https://developers.google.com/maps/documentation/utilities/polylinealgorithm):<br>  ```<br>  locations=enc:gfo}EtohhU<br>  ```<br><br>Latitude and longitude coordinate strings are defined using numerals within a comma-separated text string. For example, "40.714728,-73.998672" is a valid locations value. Latitude and longitude values must correspond to a valid location on the face of the earth. Latitudes can take any value between -90 and 90 while longitude values can take any value between -180 and 180. If you specify an invalid latitude or longitude value, your request will be rejected as a bad request.<br><br>You may pass any number of multiple coordinates within an array or encoded polyline, while still constructing a valid URL. Note that when passing multiple coordinates, the accuracy of any returned data may be of lower resolution than when requesting data for a single coordinate. |
| `path` | `List<String>` | Query, Optional | An array of comma separated `latitude,longitude` strings. |
| `samples` | `Double` | Query, Optional | Required if path parameter is set. |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`MapsApiElevationJsonResponse`](../../doc/models/maps-api-elevation-json-response.md).

## Example Usage

```java
List<String> locations = Arrays.asList(
    "35,-100",
    "40,-110"
);

List<String> path = Arrays.asList(
    "35,-110",
    "33,-110",
    "31,-110"
);

Double samples = 10D;

elevationApi.elevationAsync(locations, path, samples).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

## Example Response *(as JSON)*

```json
{
  "results": [
    {
      "elevation": 1608.637939453125,
      "location": {
        "lat": 39.7391536,
        "lng": -104.9847034
      },
      "resolution": 4.771975994110107
    }
  ],
  "status": "OK"
}
```

