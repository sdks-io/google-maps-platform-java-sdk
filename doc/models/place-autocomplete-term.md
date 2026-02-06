
# Place Autocomplete Term

*This model accepts additional fields of type Object.*

## Structure

`PlaceAutocompleteTerm`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Value` | `String` | Required | The text of the term. | String getValue() | setValue(String value) |
| `Offset` | `double` | Required | Defines the start position of this term in the description, measured in Unicode characters | double getOffset() | setOffset(double offset) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example (as JSON)

```json
{
  "value": "value6",
  "offset": 244.56,
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

