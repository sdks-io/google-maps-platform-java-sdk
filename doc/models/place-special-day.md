
# Place Special Day

*This model accepts additional fields of type Object.*

## Structure

`PlaceSpecialDay`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Date` | `String` | Optional | A date expressed in RFC3339 format in the local timezone for the place, for example 2010-12-31. | String getDate() | setDate(String date) |
| `ExceptionalHours` | `Boolean` | Optional | True if there are exceptional hours for this day. If `true`, this means that there is at least one exception for this day. Exceptions cause different values to occur in the subfields of `current_opening_hours` and `secondary_opening_hours` such as `periods`, `weekday_text`, `open_now`. The exceptions apply to the hours, and the hours are used to generate the other fields. | Boolean getExceptionalHours() | setExceptionalHours(Boolean exceptionalHours) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example (as JSON)

```json
{
  "date": "date0",
  "exceptional_hours": false,
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

