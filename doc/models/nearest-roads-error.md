
# Nearest Roads Error

*This model accepts additional fields of type Object.*

## Structure

`NearestRoadsError`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Code` | `double` | Required | This is the same as the HTTP status of the response. | double getCode() | setCode(double code) |
| `Message` | `String` | Required | A short description of the error. | String getMessage() | setMessage(String message) |
| `Status` | `String` | Required | An error such as `INVALID_ARGUMENT`. | String getStatus() | setStatus(String status) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example (as JSON)

```json
{
  "code": 229.44,
  "message": "message6",
  "status": "status2",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

