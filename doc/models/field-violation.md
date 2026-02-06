
# Field Violation

*This model accepts additional fields of type Object.*

## Structure

`FieldViolation`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Field` | `String` | Required | The name of the invalid field. | String getField() | setField(String field) |
| `Description` | `String` | Required | A short description of the error. | String getDescription() | setDescription(String description) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example (as JSON)

```json
{
  "field": "field8",
  "description": "description4",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

