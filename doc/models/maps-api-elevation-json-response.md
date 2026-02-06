
# Maps Api Elevation Json Response

*This model accepts additional fields of type Object.*

## Structure

`MapsApiElevationJsonResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ErrorMessage` | `String` | Optional | When the service returns a status code other than `OK<`, there may be an additional `error_message` field within the response object. This field contains more detailed information about thereasons behind the given status code. This field is not always returned, and its content is subject to change. | String getErrorMessage() | setErrorMessage(String errorMessage) |
| `Status` | [`ElevationStatus`](../../doc/models/elevation-status.md) | Required | Status codes returned by service.<br><br>- `OK` indicating the API request was successful.<br>- `DATA_NOT_AVAILABLE` indicating that there's no available data for the input locations.<br>- `INVALID_REQUEST` indicating the API request was malformed.<br>- `OVER_DAILY_LIMIT` indicating any of the following:<br>  - The API key is missing or invalid.<br>  - Billing has not been enabled on your account.<br>  - A self-imposed usage cap has been exceeded.<br>  - The provided method of payment is no longer valid (for example, a credit card has expired).<br>- `OVER_QUERY_LIMIT` indicating the requestor has exceeded quota.<br>- `REQUEST_DENIED` indicating the API did not complete the request.<br>- `UNKNOWN_ERROR` indicating an unknown error. | ElevationStatus getStatus() | setStatus(ElevationStatus status) |
| `Results` | [`List<Result>`](../../doc/models/result.md) | Required | - | List<Result> getResults() | setResults(List<Result> results) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example (as JSON)

```json
{
  "error_message": "Invalid request. Invalid 'locations' parameter.",
  "status": "OK",
  "results": [
    {
      "elevation": 164.98,
      "resolution": 23.6,
      "location": {
        "lat": 205.22,
        "lng": 218.24,
        "exampleAdditionalProperty": {
          "key1": "val1",
          "key2": "val2"
        }
      },
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
```

