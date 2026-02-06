
# Directions Route

Routes consist of nested `legs` and `steps`.

*This model accepts additional fields of type Object.*

## Structure

`DirectionsRoute`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Legs` | [`List<DirectionsLeg>`](../../doc/models/directions-leg.md) | Required | An array which contains information about a leg of the route, between two locations within the given route. A separate leg will be present for each waypoint or destination specified. (A route with no waypoints will contain exactly one leg within the legs array.) Each leg consists of a series of steps. | List<DirectionsLeg> getLegs() | setLegs(List<DirectionsLeg> legs) |
| `Bounds` | [`Bounds`](../../doc/models/bounds.md) | Required | A rectangle in geographical coordinates from points at the southwest and northeast corners. | Bounds getBounds() | setBounds(Bounds bounds) |
| `Copyrights` | `String` | Required | Contains the copyright notices to be displayed for this route. You must handle and display this information yourself. This content is meant to be read as-is. Do not programmatically parse this display-only content. | String getCopyrights() | setCopyrights(String copyrights) |
| `Summary` | `String` | Required | Contains a short textual description for the route, suitable for naming and disambiguating the route from alternatives. | String getSummary() | setSummary(String summary) |
| `WaypointOrder` | `List<Integer>` | Required | An array indicating the order of any waypoints in the calculated route. This waypoints may be reordered if the request was passed optimize:true within its waypoints parameter. | List<Integer> getWaypointOrder() | setWaypointOrder(List<Integer> waypointOrder) |
| `Warnings` | `List<String>` | Required | Contains an array of warnings to be displayed when showing these directions. You must handle and display these warnings yourself. | List<String> getWarnings() | setWarnings(List<String> warnings) |
| `OverviewPolyline` | [`DirectionsPolyline`](../../doc/models/directions-polyline.md) | Required | [Polyline encoding](https://developers.google.com/maps/documentation/utilities/polylinealgorithm) is a lossy compression algorithm that allows you to store a series of coordinates as a single string. Point coordinates are encoded using signed values. If you only have a few static points, you may also wish to use the interactive polyline encoding utility.<br><br>The encoding process converts a binary value into a series of character codes for ASCII characters using the familiar base64 encoding scheme: to ensure proper display of these characters, encoded values are summed with 63 (the ASCII character '?') before converting them into ASCII. The algorithm also checks for additional character codes for a given point by checking the least significant bit of each byte group; if this bit is set to 1, the point is not yet fully formed and additional data must follow.<br><br>Additionally, to conserve space, points only include the offset from the previous point (except of course for the first point). All points are encoded in Base64 as signed integers, as latitudes and longitudes are signed values. The encoding format within a polyline needs to represent two coordinates representing latitude and longitude to a reasonable precision. Given a maximum longitude of +/- 180 degrees to a precision of 5 decimal places (180.00000 to -180.00000), this results in the need for a 32 bit signed binary integer value. | DirectionsPolyline getOverviewPolyline() | setOverviewPolyline(DirectionsPolyline overviewPolyline) |
| `Fare` | [`Fare`](../../doc/models/fare.md) | Optional | The total fare for the route.<br><br>```<br>{<br>  "currency" : "USD",<br>  "value" : 6,<br>  "text" : "$6.00"<br>}<br>``` | Fare getFare() | setFare(Fare fare) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example (as JSON)

```json
{
  "legs": [
    {
      "end_address": "end_address8",
      "end_location": {
        "lat": 207.76,
        "lng": 215.7,
        "exampleAdditionalProperty": {
          "key1": "val1",
          "key2": "val2"
        }
      },
      "start_address": "start_address0",
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
  ],
  "bounds": {
    "northeast": {
      "lat": 194.96,
      "lng": 27.5,
      "exampleAdditionalProperty": {
        "key1": "val1",
        "key2": "val2"
      }
    },
    "southwest": {
      "lat": 1.22,
      "lng": 166.24,
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
  "copyrights": "copyrights2",
  "summary": "summary6",
  "waypoint_order": [
    211
  ],
  "warnings": [
    "warnings0"
  ],
  "overview_polyline": {
    "points": "chnwEbderQ?XR@D?@?",
    "exampleAdditionalProperty": {
      "key1": "val1",
      "key2": "val2"
    }
  },
  "fare": {
    "currency": "currency0",
    "value": 12.62,
    "text": "text0",
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

