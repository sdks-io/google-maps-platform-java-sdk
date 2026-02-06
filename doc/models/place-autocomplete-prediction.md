
# Place Autocomplete Prediction

*This model accepts additional fields of type Object.*

## Structure

`PlaceAutocompletePrediction`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Description` | `String` | Required | Contains the human-readable name for the returned result. For `establishment` results, this is usually the business name. This content is meant to be read as-is. Do not programmatically parse the formatted address. | String getDescription() | setDescription(String description) |
| `MatchedSubstrings` | [`List<PlaceAutocompleteMatchedSubstring>`](../../doc/models/place-autocomplete-matched-substring.md) | Required | A list of substrings that describe the location of the entered term in the prediction result text, so that the term can be highlighted if desired. | List<PlaceAutocompleteMatchedSubstring> getMatchedSubstrings() | setMatchedSubstrings(List<PlaceAutocompleteMatchedSubstring> matchedSubstrings) |
| `PlaceId` | `String` | Optional | A textual identifier that uniquely identifies a place. To retrieve information about the place, pass this identifier in the placeId field of a Places API request. For more information about place IDs, see the [Place IDs](https://developers.google.com/maps/documentation/places/web-service/place-id) overview. | String getPlaceId() | setPlaceId(String placeId) |
| `Reference` | `String` | Optional | See place_id. | String getReference() | setReference(String reference) |
| `StructuredFormatting` | [`PlaceAutocompleteStructuredFormat`](../../doc/models/place-autocomplete-structured-format.md) | Required | - | PlaceAutocompleteStructuredFormat getStructuredFormatting() | setStructuredFormatting(PlaceAutocompleteStructuredFormat structuredFormatting) |
| `Terms` | [`List<PlaceAutocompleteTerm>`](../../doc/models/place-autocomplete-term.md) | Required | Contains an array of terms identifying each section of the returned description (a section of the description is generally terminated with a comma). Each entry in the array has a `value` field, containing the text of the term, and an `offset` field, defining the start position of this term in the description, measured in Unicode characters. | List<PlaceAutocompleteTerm> getTerms() | setTerms(List<PlaceAutocompleteTerm> terms) |
| `Types` | `List<String>` | Optional | Contains an array of types that apply to this place. For example: `[ "political", "locality" ]` or `[ "establishment", "geocode", "beauty_salon" ]`. The array can contain multiple values. Learn more about [Place types](https://developers.google.com/maps/documentation/places/web-service/supported_types). | List<String> getTypes() | setTypes(List<String> types) |
| `DistanceMeters` | `Integer` | Optional | The straight-line distance in meters from the origin. This field is only returned for requests made with an `origin`. | Integer getDistanceMeters() | setDistanceMeters(Integer distanceMeters) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example (as JSON)

```json
{
  "description": "Paris, France",
  "matched_substrings": [
    {
      "length": 200.82,
      "offset": 96.92,
      "exampleAdditionalProperty": {
        "key1": "val1",
        "key2": "val2"
      }
    }
  ],
  "structured_formatting": {
    "main_text": "main_text6",
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
    "secondary_text": "secondary_text2",
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
  },
  "terms": [
    {
      "value": "value0",
      "offset": 246.22,
      "exampleAdditionalProperty": {
        "key1": "val1",
        "key2": "val2"
      }
    }
  ],
  "place_id": "place_id4",
  "reference": "reference4",
  "types": [
    "types9",
    "types0"
  ],
  "distance_meters": 174,
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

