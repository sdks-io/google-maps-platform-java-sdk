
# Custom Query Parameter



Documentation for accessing and setting credentials for ApiKeyAuth.

## Auth Credentials

| Name | Type | Description | Setter | Getter |
|  --- | --- | --- | --- | --- |
| key | `String` | - | `key` | `getKey()` |



**Note:** Auth credentials can be set using `customQueryAuthenticationCredentials` in the client builder and accessed through `getCustomQueryAuthenticationCredentials` method in the client instance.

## Usage Example

### Client Initialization

You must provide credentials in the client as shown in the following code snippet.

```java
import com.googleapis.maps.GoogleMapsPlatformClient;
import com.googleapis.maps.authentication.CustomQueryAuthenticationModel;

public class Program {
    public static void main(String[] args) {
        GoogleMapsPlatformClient client = new GoogleMapsPlatformClient.Builder()
            .customQueryAuthenticationCredentials(new CustomQueryAuthenticationModel.Builder(
                    "key"
                )
                .build())
            .build();
    }
}
```


