
# Place Opening Hours Period

*This model accepts additional fields of type Object.*

## Structure

`PlaceOpeningHoursPeriod`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Open` | [`PlaceOpeningHoursPeriodDetail`](../../doc/models/place-opening-hours-period-detail.md) | Required | - | PlaceOpeningHoursPeriodDetail getOpen() | setOpen(PlaceOpeningHoursPeriodDetail open) |
| `Close` | [`PlaceOpeningHoursPeriodDetail`](../../doc/models/place-opening-hours-period-detail.md) | Optional | - | PlaceOpeningHoursPeriodDetail getClose() | setClose(PlaceOpeningHoursPeriodDetail close) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example (as JSON)

```json
{
  "open": {
    "day": 0.52,
    "time": "1700",
    "date": "date8",
    "truncated": false,
    "exampleAdditionalProperty": {
      "key1": "val1",
      "key2": "val2"
    }
  },
  "close": {
    "date": "date4",
    "day": 26.5,
    "time": "time8",
    "truncated": false,
    "exampleAdditionalProperty": {
      "key1": "val1",
      "key2": "val2"
    }
  },
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

