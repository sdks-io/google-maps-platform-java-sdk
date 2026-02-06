# Street View API

```java
StreetViewApi streetViewApi = client.getStreetViewApi();
```

## Class Name

`StreetViewApi`

## Methods

* [Street View](../../doc/controllers/street-view-api.md#street-view)
* [Street View Metadata](../../doc/controllers/street-view-api.md#street-view-metadata)


# Street View

The Street View Static API lets you embed a static (non-interactive) Street View panorama or thumbnail into your web page, without the use of JavaScript. The viewport is defined with URL parameters sent through a standard HTTP request, and is returned as a static image.

```java
CompletableFuture<ApiResponse<DynamicResponse>> streetViewAsync(
    final String size,
    final Double fov,
    final Double heading,
    final String location,
    final String pano,
    final Double pitch,
    final Double radius,
    final Boolean returnErrorCode,
    final String signature,
    final Source source)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `size` | `String` | Query, Required | Specifies the output size of the image in pixels. Must not exceed 640 pixels wide or high, anything over will default to 640 pixels. Size is specified as `{width}x{height}` - for example, `size=600x400` returns an image 600 pixels wide, and 400 high. |
| `fov` | `Double` | Query, Optional | Determines the horizontal field of view of the image. The field of view is expressed in degrees, with a maximum allowed value of 120. When dealing with a fixed-size viewport, as with a Street View image of a set size, field of view in essence represents zoom, with smaller numbers indicating a higher level of zoom. Default is 90. |
| `heading` | `Double` | Query, Optional | Indicates the compass heading of the camera. Accepted values are from 0 to 360 (both values indicating North, with 90 indicating East, and 180 South). If no heading is specified, a value will be calculated that directs the camera towards the specified location, from the point at which the closest photograph was taken. |
| `location` | `String` | Query, Optional | The point around which to retrieve place information. The Street View Static API will snap to the panorama photographed closest to this location. When an address text string is provided, the API may use a different camera location to better display the specified location. When a lat/lng is provided, the API searches a 50 meter radius for a photograph closest to this location. Because Street View imagery is periodically refreshed, and photographs may be taken from slightly different positions each time, it's possible that your `location` may snap to a different panorama when imagery is updated. |
| `pano` | `String` | Query, Optional | A specific panorama ID. These are generally stable, though panoramas may change ID over time as imagery is refreshed. |
| `pitch` | `Double` | Query, Optional | Specifies the up or down angle of the camera relative to the Street View vehicle. This is often, but not always, flat horizontal. Positive values angle the camera up (with 90 degrees indicating straight up); negative values angle the camera down (with -90 indicating straight down). Default is 0. |
| `radius` | `Double` | Query, Optional | Sets a radius, specified in meters, in which to search for a panorama, centered on the given latitude and longitude. Valid values are non-negative integers. Default is 50 meters. |
| `returnErrorCode` | `Boolean` | Query, Optional | Indicates whether the API should return a non `200 Ok` HTTP status when no image is found (`404 NOT FOUND`), or in response to an invalid request (400 BAD REQUEST). Valid values are `true` and `false`. If set to `true`, an error message is returned in place of the generic gray image. This eliminates the need to make a separate call to check for image availability. |
| `signature` | `String` | Query, Optional | A digital signature used to verify that any site generating requests using your API key is authorized to do so. Requests that do not include a digital signature might fail. For more information, see [Get a Key and Signature](https://developers.google.com/maps/documentation/streetview/get-api-key). |
| `source` | [`Source`](../../doc/models/source.md) | Query, Optional | Limits Street View searches to selected sources. Valid values are:<br><br>* `default` uses the default sources for Street View; searches are not limited to specific sources.<br>* `outdoor` limits searches to outdoor collections. Indoor collections are not included in search results. Note that outdoor panoramas may not exist for the specified location. Also note that the search only returns panoramas where it's possible to determine whether they're indoors or outdoors. For example, PhotoSpheres are not returned because it's unknown whether they are indoors or outdoors. |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type `DynamicResponse`.

## Example Usage

```java
String size = "size0";
String location = "40,-110";

streetViewApi.streetViewAsync(size, null, null, location, null, null, null, null, null, null).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```


# Street View Metadata

The Street View Static API metadata requests provide data about Street View panoramas. Using the metadata, you can find out if a Street View image is available at a given location, as well as getting programmatic access to the latitude and longitude, the panorama ID, the date the photo was taken, and the copyright information for the image. Accessing this metadata allows you to customize error behavior in your application.

```java
CompletableFuture<ApiResponse<StreetViewResponse>> streetViewMetadataAsync(
    final Double heading,
    final String location,
    final String pano,
    final Double pitch,
    final Double radius,
    final Boolean returnErrorCode,
    final String signature,
    final String size,
    final Source source)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `heading` | `Double` | Query, Optional | Indicates the compass heading of the camera. Accepted values are from 0 to 360 (both values indicating North, with 90 indicating East, and 180 South). If no heading is specified, a value will be calculated that directs the camera towards the specified location, from the point at which the closest photograph was taken. |
| `location` | `String` | Query, Optional | The point around which to retrieve place information. The Street View Static API will snap to the panorama photographed closest to this location. When an address text string is provided, the API may use a different camera location to better display the specified location. When a lat/lng is provided, the API searches a 50 meter radius for a photograph closest to this location. Because Street View imagery is periodically refreshed, and photographs may be taken from slightly different positions each time, it's possible that your `location` may snap to a different panorama when imagery is updated. |
| `pano` | `String` | Query, Optional | A specific panorama ID. These are generally stable, though panoramas may change ID over time as imagery is refreshed. |
| `pitch` | `Double` | Query, Optional | Specifies the up or down angle of the camera relative to the Street View vehicle. This is often, but not always, flat horizontal. Positive values angle the camera up (with 90 degrees indicating straight up); negative values angle the camera down (with -90 indicating straight down). Default is 0. |
| `radius` | `Double` | Query, Optional | Sets a radius, specified in meters, in which to search for a panorama, centered on the given latitude and longitude. Valid values are non-negative integers. Default is 50 meters. |
| `returnErrorCode` | `Boolean` | Query, Optional | Indicates whether the API should return a non `200 Ok` HTTP status when no image is found (`404 NOT FOUND`), or in response to an invalid request (400 BAD REQUEST). Valid values are `true` and `false`. If set to `true`, an error message is returned in place of the generic gray image. This eliminates the need to make a separate call to check for image availability. |
| `signature` | `String` | Query, Optional | A digital signature used to verify that any site generating requests using your API key is authorized to do so. Requests that do not include a digital signature might fail. For more information, see [Get a Key and Signature](https://developers.google.com/maps/documentation/streetview/get-api-key). |
| `size` | `String` | Query, Optional | Specifies the output size of the image in pixels. Size is specified as `{width}x{height}` - for example, `size=600x400` returns an image 600 pixels wide, and 400 high. |
| `source` | [`Source`](../../doc/models/source.md) | Query, Optional | Limits Street View searches to selected sources. Valid values are:<br><br>* `default` uses the default sources for Street View; searches are not limited to specific sources.<br>* `outdoor` limits searches to outdoor collections. Indoor collections are not included in search results. Note that outdoor panoramas may not exist for the specified location. Also note that the search only returns panoramas where it's possible to determine whether they're indoors or outdoors. For example, PhotoSpheres are not returned because it's unknown whether they are indoors or outdoors. |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`StreetViewResponse`](../../doc/models/street-view-response.md).

## Example Usage

```java
String location = "40,-110";

streetViewApi.streetViewMetadataAsync(null, location, null, null, null, null, null, null, null).thenAccept(result -> {
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
  "copyright": "© Google",
  "date": "2014-04",
  "location": {
    "lat": 46.41434210086409,
    "lng": 10.01400595356193
  },
  "pano_id": "vPnURflnc8AZu5NMLYRddw",
  "status": "OK"
}
```

