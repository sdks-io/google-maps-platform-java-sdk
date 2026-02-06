
# Time Zone Text Value Object

An object containing Unix time, a time zone, and its formatted text representation.

*This model accepts additional fields of type Object.*

## Structure

`TimeZoneTextValueObject`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Text` | `String` | Required | The time specified as a string in the time zone. | String getText() | setText(String text) |
| `Value` | `double` | Required | The time specified as Unix time, or seconds since midnight, January 1, 1970 UTC. | double getValue() | setValue(double value) |
| `TimeZone` | `String` | Required | Contains the time zone. The value is the name of the time zone as defined in the [IANA Time Zone Database](http://www.iana.org/time-zones), e.g. "America/New_York". | String getTimeZone() | setTimeZone(String timeZone) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example (as JSON)

```json
{
  "text": "text6",
  "value": 199.08,
  "time_zone": "time_zone8",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

