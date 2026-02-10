# Geolocation API

```java
GeolocationApi geolocationApi = client.getGeolocationApi();
```

## Class Name

`GeolocationApi`


# Geolocate

Geolocation API returns a location and accuracy radius based on information about cell towers and WiFi nodes that the mobile client can detect. This document describes the protocol used to send this data to the server and to return a response to the client.

Communication is done over HTTPS using POST. Both request and response are formatted as JSON, and the content type of both is `application/json`.

You must specify a key in your request, included as the value of a`key` parameter. A `key` is your application's  API key. This key identifies your application for purposes of quota management. Learn how to [get a key](https://developers.google.com/maps/documentation/geolocation/get-api-key).

```java
CompletableFuture<ApiResponse<GeolocationResponse>> geolocateAsync(
    final GeolocationRequest body)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`GeolocationRequest`](../../doc/models/geolocation-request.md) | Body, Optional | The request body must be formatted as JSON. |

## Server

`Server.GOOGLE_APIS`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`GeolocationResponse`](../../doc/models/geolocation-response.md).

## Example Usage

```java
GeolocationRequest body = new GeolocationRequest.Builder()
    .considerIp("false")
    .wifiAccessPoints(Arrays.asList(
        new WiFiAccessPoint.Builder(
            "84:d4:7e:09:a5:f1"
        )
        .signalStrength(-43)
        .signalToNoiseRatio(0)
        .build(),
        new WiFiAccessPoint.Builder(
            "44:48:c1:a6:f3:d0"
        )
        .signalStrength(-55)
        .signalToNoiseRatio(0)
        .build()
    ))
    .build();

geolocationApi.geolocateAsync(body).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    Throwable cause = exception.getCause();

    if (cause instanceof ErrorResponseException) {
        ErrorResponseException errorResponseException = (ErrorResponseException) cause;
        errorResponseException.printStackTrace();
    } else {
        // fallback for unexpected errors
        exception.printStackTrace();
    }

    return null;
});
```

## Example Response *(as JSON)*

```json
{
  "location": {
    "lat": 37.421925,
    "lng": -122.0841293
  },
  "accuracy": 30
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | 400 BAD REQUEST | [`ErrorResponseException`](../../doc/models/error-response-exception.md) |
| 404 | 404 NOT FOUND | [`ErrorResponseException`](../../doc/models/error-response-exception.md) |

