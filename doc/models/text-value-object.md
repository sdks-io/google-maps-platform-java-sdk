
# Text Value Object

An object containing a numeric value and its formatted text representation.

*This model accepts additional fields of type Object.*

## Structure

`TextValueObject`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Text` | `String` | Required | String value. | String getText() | setText(String text) |
| `Value` | `double` | Required | Numeric value. | double getValue() | setValue(double value) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example (as JSON)

```json
{
  "text": "text6",
  "value": 40.06,
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

