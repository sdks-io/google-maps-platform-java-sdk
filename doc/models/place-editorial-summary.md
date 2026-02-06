
# Place Editorial Summary

Contains a summary of the place. A summary is comprised of a textual overview, and also includes the language code for these if applicable. Summary text must be presented as-is and can not be modified or altered.

*This model accepts additional fields of type Object.*

## Structure

`PlaceEditorialSummary`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Overview` | `String` | Optional | A medium-length textual summary of the place. | String getOverview() | setOverview(String overview) |
| `Language` | `String` | Optional | The language of the previous fields. May not always be present. | String getLanguage() | setLanguage(String language) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example (as JSON)

```json
{
  "overview": "overview0",
  "language": "language0",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

