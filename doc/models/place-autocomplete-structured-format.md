
# Place Autocomplete Structured Format

*This model accepts additional fields of type Object.*

## Structure

`PlaceAutocompleteStructuredFormat`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `MainText` | `String` | Required | Contains the main text of a prediction, usually the name of the place. | String getMainText() | setMainText(String mainText) |
| `MainTextMatchedSubstrings` | [`List<PlaceAutocompleteMatchedSubstring>`](../../doc/models/place-autocomplete-matched-substring.md) | Required | Contains an array with `offset` value and `length`. These describe the location of the entered term in the prediction result text, so that the term can be highlighted if desired. | List<PlaceAutocompleteMatchedSubstring> getMainTextMatchedSubstrings() | setMainTextMatchedSubstrings(List<PlaceAutocompleteMatchedSubstring> mainTextMatchedSubstrings) |
| `SecondaryText` | `String` | Optional | Contains the secondary text of a prediction, usually the location of the place. | String getSecondaryText() | setSecondaryText(String secondaryText) |
| `SecondaryTextMatchedSubstrings` | [`List<PlaceAutocompleteMatchedSubstring>`](../../doc/models/place-autocomplete-matched-substring.md) | Optional | Contains an array with `offset` value and `length`. These describe the location of the entered term in the prediction result text, so that the term can be highlighted if desired. | List<PlaceAutocompleteMatchedSubstring> getSecondaryTextMatchedSubstrings() | setSecondaryTextMatchedSubstrings(List<PlaceAutocompleteMatchedSubstring> secondaryTextMatchedSubstrings) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example (as JSON)

```json
{
  "main_text": "main_text2",
  "main_text_matched_substrings": [
    {
      "length": 174.72,
      "offset": 22.62,
      "exampleAdditionalProperty": {
        "key1": "val1",
        "key2": "val2"
      }
    }
  ],
  "secondary_text": "secondary_text8",
  "secondary_text_matched_substrings": [
    {
      "length": 26.26,
      "offset": 178.36,
      "exampleAdditionalProperty": {
        "key1": "val1",
        "key2": "val2"
      }
    },
    {
      "length": 26.26,
      "offset": 178.36,
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

