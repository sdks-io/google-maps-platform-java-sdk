
# Place Opening Hours

An object describing the opening hours of a place.

*This model accepts additional fields of type Object.*

## Structure

`PlaceOpeningHours`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `OpenNow` | `Boolean` | Optional | A boolean value indicating if the place is open at the current time. | Boolean getOpenNow() | setOpenNow(Boolean openNow) |
| `Periods` | [`List<PlaceOpeningHoursPeriod>`](../../doc/models/place-opening-hours-period.md) | Optional | An array of opening periods covering seven days, starting from Sunday, in chronological order. | List<PlaceOpeningHoursPeriod> getPeriods() | setPeriods(List<PlaceOpeningHoursPeriod> periods) |
| `SpecialDays` | [`List<PlaceSpecialDay>`](../../doc/models/place-special-day.md) | Optional | An array of up to seven entries corresponding to the next seven days. | List<PlaceSpecialDay> getSpecialDays() | setSpecialDays(List<PlaceSpecialDay> specialDays) |
| `Type` | `String` | Optional | A type string used to identify the type of secondary hours (for example, `DRIVE_THROUGH`, `HAPPY_HOUR`, `DELIVERY`, `TAKEOUT`, `KITCHEN`, `BREAKFAST`, `LUNCH`, `DINNER`, `BRUNCH`, `PICKUP`, `SENIOR_HOURS`). Set for `secondary_opening_hours` only. | String getType() | setType(String type) |
| `WeekdayText` | `List<String>` | Optional | An array of strings describing in human-readable text the hours of the place. | List<String> getWeekdayText() | setWeekdayText(List<String> weekdayText) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example (as JSON)

```json
{
  "weekday_text": [
    "Monday: 9:00 AM – 5:00 PM",
    "Tuesday: 9:00 AM – 5:00 PM",
    "Wednesday: 9:00 AM – 5:00 PM",
    "Thursday: 9:00 AM – 5:00 PM",
    "Friday: 9:00 AM – 5:00 PM",
    "Saturday: Closed",
    "Sunday: Closed"
  ],
  "open_now": false,
  "periods": [
    {
      "open": {
        "date": "date8",
        "day": 0.52,
        "time": "time4",
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
    },
    {
      "open": {
        "date": "date8",
        "day": 0.52,
        "time": "time4",
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
    },
    {
      "open": {
        "date": "date8",
        "day": 0.52,
        "time": "time4",
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
  ],
  "special_days": [
    {
      "date": "date4",
      "exceptional_hours": false,
      "exampleAdditionalProperty": {
        "key1": "val1",
        "key2": "val2"
      }
    }
  ],
  "type": "type8",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

