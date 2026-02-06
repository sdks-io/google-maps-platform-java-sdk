
# Directions Transit Details

Additional information that is not relevant for other modes of transportation.

*This model accepts additional fields of type Object.*

## Structure

`DirectionsTransitDetails`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ArrivalStop` | [`DirectionsTransitStop`](../../doc/models/directions-transit-stop.md) | Optional | - | DirectionsTransitStop getArrivalStop() | setArrivalStop(DirectionsTransitStop arrivalStop) |
| `ArrivalTime` | [`TimeZoneTextValueObject`](../../doc/models/time-zone-text-value-object.md) | Optional | An object containing Unix time, a time zone, and its formatted text representation. | TimeZoneTextValueObject getArrivalTime() | setArrivalTime(TimeZoneTextValueObject arrivalTime) |
| `DepartureStop` | [`DirectionsTransitStop`](../../doc/models/directions-transit-stop.md) | Optional | - | DirectionsTransitStop getDepartureStop() | setDepartureStop(DirectionsTransitStop departureStop) |
| `DepartureTime` | [`TimeZoneTextValueObject`](../../doc/models/time-zone-text-value-object.md) | Optional | An object containing Unix time, a time zone, and its formatted text representation. | TimeZoneTextValueObject getDepartureTime() | setDepartureTime(TimeZoneTextValueObject departureTime) |
| `Headsign` | `String` | Optional | Specifies the direction in which to travel on this line, as it is marked on the vehicle or at the departure stop. This will often be the terminus station. | String getHeadsign() | setHeadsign(String headsign) |
| `Headway` | `Integer` | Optional | Specifies the expected number of seconds between departures from the same stop at this time. For example, with a `headway` value of 600, you would expect a ten minute wait if you should miss your bus. | Integer getHeadway() | setHeadway(Integer headway) |
| `Line` | [`DirectionsTransitLine`](../../doc/models/directions-transit-line.md) | Optional | - | DirectionsTransitLine getLine() | setLine(DirectionsTransitLine line) |
| `NumStops` | `Integer` | Optional | The number of stops from the departure to the arrival stop. This includes the arrival stop, but not the departure stop. For example, if your directions involve leaving from Stop A, passing through stops B and C, and arriving at stop D, `num_stops` will return 3. | Integer getNumStops() | setNumStops(Integer numStops) |
| `TripShortName` | `String` | Optional | The text that appears in schedules and sign boards to identify a transit trip to passengers. The text should uniquely identify a trip within a service day. For example, "538" is the `trip_short_name` of the Amtrak train that leaves San Jose, CA at 15:10 on weekdays to Sacramento, CA. | String getTripShortName() | setTripShortName(String tripShortName) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example (as JSON)

```json
{
  "trip_short_name": "538",
  "arrival_stop": {
    "location": {
      "lat": 205.22,
      "lng": 218.24,
      "exampleAdditionalProperty": {
        "key1": "val1",
        "key2": "val2"
      }
    },
    "name": "name8",
    "exampleAdditionalProperty": {
      "key1": "val1",
      "key2": "val2"
    }
  },
  "arrival_time": {
    "text": "text4",
    "value": 165.86,
    "time_zone": "time_zone6",
    "exampleAdditionalProperty": {
      "key1": "val1",
      "key2": "val2"
    }
  },
  "departure_stop": {
    "location": {
      "lat": 205.22,
      "lng": 218.24,
      "exampleAdditionalProperty": {
        "key1": "val1",
        "key2": "val2"
      }
    },
    "name": "name4",
    "exampleAdditionalProperty": {
      "key1": "val1",
      "key2": "val2"
    }
  },
  "departure_time": {
    "text": "text0",
    "value": 77.12,
    "time_zone": "time_zone2",
    "exampleAdditionalProperty": {
      "key1": "val1",
      "key2": "val2"
    }
  },
  "headsign": "headsign2",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

