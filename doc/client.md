
# Client Class Documentation

The following parameters are configurable for the API Client:

| Parameter | Type | Description |
|  --- | --- | --- |
| environment | [`Environment`](../README.md#environments) | The API environment. <br> **Default: `Environment.PRODUCTION`** |
| httpClientConfig | [`Consumer<HttpClientConfiguration.Builder>`](../doc/http-client-configuration-builder.md) | Set up Http Client Configuration instance. |
| loggingConfig | [`Consumer<ApiLoggingConfiguration.Builder>`](../doc/api-logging-configuration-builder.md) | Set up Logging Configuration instance. |
| customQueryAuthenticationCredentials | [`CustomQueryAuthenticationCredentials`](auth/custom-query-parameter.md) | The Credentials Setter for Custom Query Parameter |

The API client can be initialized as follows:

```java
import com.googleapis.www.Environment;
import com.googleapis.www.GoogleMapsPlatformClient;
import com.googleapis.www.authentication.CustomQueryAuthenticationModel;
import com.googleapis.www.exceptions.ApiException;
import com.googleapis.www.http.response.ApiResponse;
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

## Google Maps PlatformClient Class

The gateway for the SDK. This class acts as a factory for the Apis and also holds the configuration of the SDK.

### Apis

| Name | Description | Return Type |
|  --- | --- | --- |
| `getGeolocationApi()` | Provides access to GeolocationApi controller. | `GeolocationApi` |
| `getDirectionsApi()` | Provides access to DirectionsApi controller. | `DirectionsApi` |
| `getElevationApi()` | Provides access to ElevationApi controller. | `ElevationApi` |
| `getGeocodingApi()` | Provides access to GeocodingApi controller. | `GeocodingApi` |
| `getTimeZoneApi()` | Provides access to TimeZoneApi controller. | `TimeZoneApi` |
| `getRoadsApi()` | Provides access to RoadsApi controller. | `RoadsApi` |
| `getDistanceMatrixApi()` | Provides access to DistanceMatrixApi controller. | `DistanceMatrixApi` |
| `getPlacesApi()` | Provides access to PlacesApi controller. | `PlacesApi` |
| `getStreetViewApi()` | Provides access to StreetViewApi controller. | `StreetViewApi` |

### Methods

| Name | Description | Return Type |
|  --- | --- | --- |
| `shutdown()` | Shutdown the underlying HttpClient instance. | `void` |
| `getEnvironment()` | Current API environment. | `Environment` |
| `getHttpClient()` | The HTTP Client instance to use for making HTTP requests. | `HttpClient` |
| `getHttpClientConfig()` | Http Client Configuration instance. | [`ReadonlyHttpClientConfiguration`](../doc/http-client-configuration.md) |
| `getLoggingConfig()` | Logging Configuration instance. | [`ReadonlyLoggingConfiguration`](../doc/api-logging-configuration.md) |
| `getCustomQueryAuthenticationCredentials()` | The credentials to use with CustomQueryAuthentication. | [`CustomQueryAuthenticationCredentials`](auth/custom-query-parameter.md) |
| `getBaseUri(Server server)` | Get base URI by current environment | `String` |
| `getBaseUri()` | Get base URI by current environment | `String` |

