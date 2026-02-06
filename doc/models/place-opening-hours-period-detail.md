
# Place Opening Hours Period Detail

*This model accepts additional fields of type Object.*

## Structure

`PlaceOpeningHoursPeriodDetail`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Date` | `String` | Optional | A date expressed in RFC3339 format in the local timezone for the place, for example 2010-12-31. | String getDate() | setDate(String date) |
| `Day` | `double` | Required | A number from 0–6, corresponding to the days of the week, starting on Sunday. For example, 2 means Tuesday. | double getDay() | setDay(double day) |
| `Time` | `String` | Required | May contain a time of day in 24-hour hhmm format. Values are in the range 0000–2359. The time will be reported in the place’s time zone. | String getTime() | setTime(String time) |
| `Truncated` | `Boolean` | Optional | True if a given period was truncated due to a seven-day cutoff, where the period starts before midnight on the date of the request and/or ends at or after  midnight on the last day. This property indicates that the period for open or close can extend past this seven-day cutoff. | Boolean getTruncated() | setTruncated(Boolean truncated) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example (as JSON)

```json
{
  "day": 142.06,
  "time": "1700",
  "date": "date8",
  "truncated": false,
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

