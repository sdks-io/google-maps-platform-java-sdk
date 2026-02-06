
# Nearest Roads Error Response Exception

*This model accepts additional fields of type Object.*

## Structure

`NearestRoadsErrorResponseException`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Error` | [`NearestRoadsError`](../../doc/models/nearest-roads-error.md) | Optional | - | NearestRoadsError getError() | setError(NearestRoadsError error) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example (as JSON)

```json
{
  "error": {
    "code": 238.32,
    "message": "message4",
    "status": "status6",
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
```

