
# Place Autocomplete Matched Substring

*This model accepts additional fields of type Object.*

## Structure

`PlaceAutocompleteMatchedSubstring`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Length` | `double` | Required | Length of the matched substring in the prediction result text. | double getLength() | setLength(double length) |
| `Offset` | `double` | Required | Start location of the matched substring in the prediction result text. | double getOffset() | setOffset(double offset) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example (as JSON)

```json
{
  "length": 32.78,
  "offset": 119.32,
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

