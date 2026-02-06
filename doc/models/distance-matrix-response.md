
# Distance Matrix Response

*This model accepts additional fields of type Object.*

## Structure

`DistanceMatrixResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `OriginAddresses` | `List<String>` | Required | An array of addresses as returned by the API from your original request. These are formatted by the geocoder and localized according to the language parameter passed with the request. This content is meant to be read as-is. Do not programatically parse the formatted addresses. | List<String> getOriginAddresses() | setOriginAddresses(List<String> originAddresses) |
| `DestinationAddresses` | `List<String>` | Required | An array of addresses as returned by the API from your original request. As with `origin_addresses`, these are localized if appropriate. This content is meant to be read as-is. Do not programatically parse the formatted addresses. | List<String> getDestinationAddresses() | setDestinationAddresses(List<String> destinationAddresses) |
| `Rows` | [`List<DistanceMatrixRow>`](../../doc/models/distance-matrix-row.md) | Required | An array of elements, which in turn each contain a `status`, `duration`, and `distance` element. | List<DistanceMatrixRow> getRows() | setRows(List<DistanceMatrixRow> rows) |
| `Status` | [`DistanceMatrixStatus`](../../doc/models/distance-matrix-status.md) | Required | Status codes returned by service.<br><br>- `OK` indicates the response contains a valid result.<br>- `INVALID_REQUEST` indicates that the provided request was invalid.<br>- `MAX_ELEMENTS_EXCEEDED` indicates that the product of origins and destinations exceeds the per-query limit.<br>- `MAX_DIMENSIONS_EXCEEDED` indicates that the number of origins or destinations exceeds the per-query limit.<br>- `OVER_DAILY_LIMIT` indicates any of the following:<br>  - The API key is missing or invalid.<br>  - Billing has not been enabled on your account.<br>  - A self-imposed usage cap has been exceeded.<br>  - The provided method of payment is no longer valid (for example, a credit card has expired).<br>- `OVER_QUERY_LIMIT` indicates the service has received too many requests from your application within the allowed time period.<br>- `REQUEST_DENIED` indicates that the service denied use of the Distance Matrix service by your application.<br>- `UNKNOWN_ERROR` indicates a Distance Matrix request could not be processed due to a server error. The request may succeed if you try again. | DistanceMatrixStatus getStatus() | setStatus(DistanceMatrixStatus status) |
| `ErrorMessage` | `String` | Optional | A string containing the human-readable text of any errors encountered while the request was being processed. | String getErrorMessage() | setErrorMessage(String errorMessage) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example (as JSON)

```json
{
  "origin_addresses": [
    "origin_addresses7",
    "origin_addresses8",
    "origin_addresses9"
  ],
  "destination_addresses": [
    "destination_addresses0"
  ],
  "rows": [
    {
      "elements": [
        {
          "fare": {
            "currency": "currency0",
            "value": 12.62,
            "text": "text0",
            "exampleAdditionalProperty": {
              "key1": "val1",
              "key2": "val2"
            }
          },
          "distance": {
            "text": "text0",
            "value": 142.22,
            "exampleAdditionalProperty": {
              "key1": "val1",
              "key2": "val2"
            }
          },
          "duration_in_traffic": {
            "text": "text6",
            "value": 178.58,
            "exampleAdditionalProperty": {
              "key1": "val1",
              "key2": "val2"
            }
          },
          "duration": {
            "text": "text6",
            "value": 224.48,
            "exampleAdditionalProperty": {
              "key1": "val1",
              "key2": "val2"
            }
          },
          "status": "OK",
          "exampleAdditionalProperty": {
            "key1": "val1",
            "key2": "val2"
          }
        }
      ],
      "exampleAdditionalProperty": {
        "key1": "val1",
        "key2": "val2"
      }
    }
  ],
  "status": "MAX_ELEMENTS_EXCEEDED",
  "error_message": "You have exceeded your rate-limit for this API.",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

