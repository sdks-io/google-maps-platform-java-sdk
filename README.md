
# Getting Started with Google Maps Platform

## Introduction

API Specification for Google Maps Platform

## Install the Package

Install the SDK by adding the following dependency in your project's pom.xml file:

```xml
<dependency>
  <groupId>io.sdks</groupId>
  <artifactId>google-maps-platform-sdk</artifactId>
  <version>1.0.4</version>
</dependency>
```

You can also view the package at:
https://central.sonatype.com/artifact/io.sdks/google-maps-platform-sdk/1.0.4

## Initialize the API Client

**_Note:_** Documentation for the client can be found [here.](https://www.github.com/sdks-io/google-maps-platform-java-sdk/tree/1.0.4/doc/client.md)

The following parameters are configurable for the API Client:

| Parameter | Type | Description |
|  --- | --- | --- |
| environment | [`Environment`](https://www.github.com/sdks-io/google-maps-platform-java-sdk/tree/1.0.4/README.md#environments) | The API environment. <br> **Default: `Environment.PRODUCTION`** |
| httpClientConfig | [`Consumer<HttpClientConfiguration.Builder>`](https://www.github.com/sdks-io/google-maps-platform-java-sdk/tree/1.0.4/doc/http-client-configuration-builder.md) | Set up Http Client Configuration instance. |
| loggingConfig | [`Consumer<ApiLoggingConfiguration.Builder>`](https://www.github.com/sdks-io/google-maps-platform-java-sdk/tree/1.0.4/doc/api-logging-configuration-builder.md) | Set up Logging Configuration instance. |
| customQueryAuthenticationCredentials | [`CustomQueryAuthenticationCredentials`](https://www.github.com/sdks-io/google-maps-platform-java-sdk/tree/1.0.4/doc/auth/custom-query-parameter.md) | The Credentials Setter for Custom Query Parameter |

The API client can be initialized as follows:

```java
import com.googleapis.maps.Environment;
import com.googleapis.maps.GoogleMapsPlatformClient;
import com.googleapis.maps.authentication.CustomQueryAuthenticationModel;
import com.googleapis.maps.exceptions.ApiException;
import com.googleapis.maps.http.response.ApiResponse;
import org.slf4j.event.Level;

public class Program {
    public static void main(String[] args) {
        GoogleMapsPlatformClient client = new GoogleMapsPlatformClient.Builder()
            .loggingConfig(builder -> builder
                    .level(Level.DEBUG)
                    .requestConfig(logConfigBuilder -> logConfigBuilder.body(true))
                    .responseConfig(logConfigBuilder -> logConfigBuilder.headers(true)))
            .httpClientConfig(configBuilder -> configBuilder
                    .timeout(0))
            .customQueryAuthenticationCredentials(new CustomQueryAuthenticationModel.Builder(
                    "key"
                )
                .build())
            .environment(Environment.PRODUCTION)
            .build();

    }
}
```

## Environments

The SDK can be configured to use a different environment for making API calls. Available environments are:

### Fields

| Name | Description |
|  --- | --- |
| PRODUCTION | **Default** |

## Authorization

This API uses the following authentication schemes.

* [`ApiKeyAuth (Custom Query Parameter)`](https://www.github.com/sdks-io/google-maps-platform-java-sdk/tree/1.0.4/doc/auth/custom-query-parameter.md)

## List of APIs

* [Geolocation API](https://www.github.com/sdks-io/google-maps-platform-java-sdk/tree/1.0.4/doc/controllers/geolocation-api.md)
* [Directions API](https://www.github.com/sdks-io/google-maps-platform-java-sdk/tree/1.0.4/doc/controllers/directions-api.md)
* [Elevation API](https://www.github.com/sdks-io/google-maps-platform-java-sdk/tree/1.0.4/doc/controllers/elevation-api.md)
* [Geocoding API](https://www.github.com/sdks-io/google-maps-platform-java-sdk/tree/1.0.4/doc/controllers/geocoding-api.md)
* [Time Zone API](https://www.github.com/sdks-io/google-maps-platform-java-sdk/tree/1.0.4/doc/controllers/time-zone-api.md)
* [Roads API](https://www.github.com/sdks-io/google-maps-platform-java-sdk/tree/1.0.4/doc/controllers/roads-api.md)
* [Distance Matrix API](https://www.github.com/sdks-io/google-maps-platform-java-sdk/tree/1.0.4/doc/controllers/distance-matrix-api.md)
* [Places API](https://www.github.com/sdks-io/google-maps-platform-java-sdk/tree/1.0.4/doc/controllers/places-api.md)
* [Street View API](https://www.github.com/sdks-io/google-maps-platform-java-sdk/tree/1.0.4/doc/controllers/street-view-api.md)

## SDK Infrastructure

### Configuration

* [ApiLoggingConfiguration](https://www.github.com/sdks-io/google-maps-platform-java-sdk/tree/1.0.4/doc/api-logging-configuration.md)
* [ApiLoggingConfiguration.Builder](https://www.github.com/sdks-io/google-maps-platform-java-sdk/tree/1.0.4/doc/api-logging-configuration-builder.md)
* [ApiRequestLoggingConfiguration.Builder](https://www.github.com/sdks-io/google-maps-platform-java-sdk/tree/1.0.4/doc/api-request-logging-configuration-builder.md)
* [ApiResponseLoggingConfiguration.Builder](https://www.github.com/sdks-io/google-maps-platform-java-sdk/tree/1.0.4/doc/api-response-logging-configuration-builder.md)
* [Configuration Interface](https://www.github.com/sdks-io/google-maps-platform-java-sdk/tree/1.0.4/doc/configuration-interface.md)
* [HttpClientConfiguration](https://www.github.com/sdks-io/google-maps-platform-java-sdk/tree/1.0.4/doc/http-client-configuration.md)
* [HttpClientConfiguration.Builder](https://www.github.com/sdks-io/google-maps-platform-java-sdk/tree/1.0.4/doc/http-client-configuration-builder.md)
* [HttpProxyConfiguration](https://www.github.com/sdks-io/google-maps-platform-java-sdk/tree/1.0.4/doc/http-proxy-configuration.md)
* [HttpProxyConfiguration.Builder](https://www.github.com/sdks-io/google-maps-platform-java-sdk/tree/1.0.4/doc/http-proxy-configuration-builder.md)

### HTTP

* [Headers](https://www.github.com/sdks-io/google-maps-platform-java-sdk/tree/1.0.4/doc/headers.md)
* [HttpCallback Interface](https://www.github.com/sdks-io/google-maps-platform-java-sdk/tree/1.0.4/doc/http-callback-interface.md)
* [HttpContext](https://www.github.com/sdks-io/google-maps-platform-java-sdk/tree/1.0.4/doc/http-context.md)
* [HttpBodyRequest](https://www.github.com/sdks-io/google-maps-platform-java-sdk/tree/1.0.4/doc/http-body-request.md)
* [HttpRequest](https://www.github.com/sdks-io/google-maps-platform-java-sdk/tree/1.0.4/doc/http-request.md)
* [HttpResponse](https://www.github.com/sdks-io/google-maps-platform-java-sdk/tree/1.0.4/doc/http-response.md)
* [HttpStringResponse](https://www.github.com/sdks-io/google-maps-platform-java-sdk/tree/1.0.4/doc/http-string-response.md)

### Utilities

* [ApiException](https://www.github.com/sdks-io/google-maps-platform-java-sdk/tree/1.0.4/doc/api-exception.md)
* [ApiResponse](https://www.github.com/sdks-io/google-maps-platform-java-sdk/tree/1.0.4/doc/api-response.md)
* [ApiHelper](https://www.github.com/sdks-io/google-maps-platform-java-sdk/tree/1.0.4/doc/api-helper.md)
* [FileWrapper](https://www.github.com/sdks-io/google-maps-platform-java-sdk/tree/1.0.4/doc/file-wrapper.md)

