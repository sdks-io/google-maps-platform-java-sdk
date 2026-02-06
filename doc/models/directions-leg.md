
# Directions Leg

*This model accepts additional fields of type Object.*

## Structure

`DirectionsLeg`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ArrivalTime` | [`TimeZoneTextValueObject`](../../doc/models/time-zone-text-value-object.md) | Optional | An object containing Unix time, a time zone, and its formatted text representation. | TimeZoneTextValueObject getArrivalTime() | setArrivalTime(TimeZoneTextValueObject arrivalTime) |
| `DepartureTime` | [`TimeZoneTextValueObject`](../../doc/models/time-zone-text-value-object.md) | Optional | An object containing Unix time, a time zone, and its formatted text representation. | TimeZoneTextValueObject getDepartureTime() | setDepartureTime(TimeZoneTextValueObject departureTime) |
| `Distance` | [`TextValueObject`](../../doc/models/text-value-object.md) | Optional | An object containing a numeric value and its formatted text representation. | TextValueObject getDistance() | setDistance(TextValueObject distance) |
| `Duration` | [`TextValueObject`](../../doc/models/text-value-object.md) | Optional | An object containing a numeric value and its formatted text representation. | TextValueObject getDuration() | setDuration(TextValueObject duration) |
| `DurationInTraffic` | [`TextValueObject`](../../doc/models/text-value-object.md) | Optional | An object containing a numeric value and its formatted text representation. | TextValueObject getDurationInTraffic() | setDurationInTraffic(TextValueObject durationInTraffic) |
| `EndAddress` | `String` | Required | Contains the human-readable address (typically a street address) from reverse geocoding the `end_location` of this leg. This content is meant to be read as-is. Do not programmatically parse the formatted address. | String getEndAddress() | setEndAddress(String endAddress) |
| `EndLocation` | [`LatLngLiteral`](../../doc/models/lat-lng-literal.md) | Required | An object describing a specific location with Latitude and Longitude in decimal degrees. | LatLngLiteral getEndLocation() | setEndLocation(LatLngLiteral endLocation) |
| `StartAddress` | `String` | Required | Contains the human-readable address (typically a street address) resulting from reverse geocoding the `start_location` of this leg. This content is meant to be read as-is. Do not programmatically parse the formatted address. | String getStartAddress() | setStartAddress(String startAddress) |
| `StartLocation` | [`LatLngLiteral`](../../doc/models/lat-lng-literal.md) | Required | An object describing a specific location with Latitude and Longitude in decimal degrees. | LatLngLiteral getStartLocation() | setStartLocation(LatLngLiteral startLocation) |
| `Steps` | [`List<DirectionsStep>`](../../doc/models/directions-step.md) | Required | An array of steps denoting information about each separate step of the leg of the journey. | List<DirectionsStep> getSteps() | setSteps(List<DirectionsStep> steps) |
| `TrafficSpeedEntry` | [`List<DirectionsTrafficSpeedEntry>`](../../doc/models/directions-traffic-speed-entry.md) | Required | Information about traffic speed along the leg. | List<DirectionsTrafficSpeedEntry> getTrafficSpeedEntry() | setTrafficSpeedEntry(List<DirectionsTrafficSpeedEntry> trafficSpeedEntry) |
| `ViaWaypoint` | [`List<DirectionsViaWaypoint>`](../../doc/models/directions-via-waypoint.md) | Required | The locations of via waypoints along this leg. | List<DirectionsViaWaypoint> getViaWaypoint() | setViaWaypoint(List<DirectionsViaWaypoint> viaWaypoint) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example (as JSON)

```json
{
  "end_address": "end_address0",
  "end_location": {
    "lat": 207.76,
    "lng": 215.7,
    "exampleAdditionalProperty": {
      "key1": "val1",
      "key2": "val2"
    }
  },
  "start_address": "start_address2",
  "start_location": {
    "lat": 108.44,
    "lng": 59.02,
    "exampleAdditionalProperty": {
      "key1": "val1",
      "key2": "val2"
    }
  },
  "steps": [
    {
      "duration": {
        "text": "text6",
        "value": 224.48,
        "exampleAdditionalProperty": {
          "key1": "val1",
          "key2": "val2"
        }
      },
      "end_location": {
        "lat": 207.76,
        "lng": 215.7,
        "exampleAdditionalProperty": {
          "key1": "val1",
          "key2": "val2"
        }
      },
      "html_instructions": "html_instructions6",
      "polyline": {
        "points": "chnwEbderQ?XR@D?@?",
        "exampleAdditionalProperty": {
          "key1": "val1",
          "key2": "val2"
        }
      },
      "start_location": {
        "lat": 108.44,
        "lng": 59.02,
        "exampleAdditionalProperty": {
          "key1": "val1",
          "key2": "val2"
        }
      },
      "travel_mode": "TRANSIT",
      "distance": {
        "text": "text0",
        "value": 142.22,
        "exampleAdditionalProperty": {
          "key1": "val1",
          "key2": "val2"
        }
      },
      "maneuver": "turn-slight-left",
      "transit_details": {
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
        "headsign": "headsign6",
        "exampleAdditionalProperty": {
          "key1": "val1",
          "key2": "val2"
        }
      },
      "steps": {
        "key1": "val1",
        "key2": "val2"
      },
      "exampleAdditionalProperty": {
        "key1": "val1",
        "key2": "val2"
      }
    }
  ],
  "traffic_speed_entry": [
    {
      "speed_category": "speed_category6",
      "offset_meters": 59.06,
      "exampleAdditionalProperty": {
        "key1": "val1",
        "key2": "val2"
      }
    }
  ],
  "via_waypoint": [
    {
      "location": {
        "lat": 205.22,
        "lng": 218.24,
        "exampleAdditionalProperty": {
          "key1": "val1",
          "key2": "val2"
        }
      },
      "step_index": 140,
      "step_interpolation": 36.54,
      "exampleAdditionalProperty": {
        "key1": "val1",
        "key2": "val2"
      }
    }
  ],
  "arrival_time": {
    "text": "text4",
    "value": 165.86,
    "time_zone": "time_zone6",
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
  "distance": {
    "text": "text0",
    "value": 142.22,
    "exampleAdditionalProperty": {
      "key1": "val1",
      "key2": "val2"
    }
  },
  "duration": {
    "text": "text6",
    "value": 224.48,
    "exampleAdditionalProperty": {
      "key1": "val1",
      "key2": "val2"
    }
  },
  "duration_in_traffic": {
    "text": "text6",
    "value": 178.58,
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

