
# Directions Response

*This model accepts additional fields of type Object.*

## Structure

`DirectionsResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `GeocodedWaypoints` | [`List<DirectionsGeocodedWaypoint>`](../../doc/models/directions-geocoded-waypoint.md) | Optional | Contains an array with details about the geocoding of origin, destination and waypoints. Elements in the geocoded_waypoints array correspond, by their zero-based position, to the origin, the waypoints in the order they are specified, and the destination.<br><br>These details will not be present for waypoints specified as textual latitude/longitude values if the service returns no results. This is because such waypoints are only reverse geocoded to obtain their representative address after a route has been found. An empty JSON object will occupy the corresponding places in the geocoded_waypoints array. | List<DirectionsGeocodedWaypoint> getGeocodedWaypoints() | setGeocodedWaypoints(List<DirectionsGeocodedWaypoint> geocodedWaypoints) |
| `Routes` | [`List<DirectionsRoute>`](../../doc/models/directions-route.md) | Required | Contains an array of routes from the origin to the destination. Routes consist of nested Legs and Steps. | List<DirectionsRoute> getRoutes() | setRoutes(List<DirectionsRoute> routes) |
| `Status` | [`DirectionsStatus`](../../doc/models/directions-status.md) | Required | The status field within the Directions response object contains the status of the request, and may contain debugging information to help you track down why the Directions service failed. The status field may contain the following values:<br><br>- `OK` indicates the response contains a valid result.<br>- `NOT_FOUND` indicates at least one of the locations specified in the request's origin, destination, or waypoints could not be geocoded.<br>- `ZERO_RESULTS` indicates no route could be found between the origin and destination.<br>- `MAX_WAYPOINTS_EXCEEDED` indicates that too many waypoints were provided in the request. For applications using the Directions API as a web service, or the directions service in the Maps JavaScript API, the maximum allowed number of waypoints is 25, plus the origin and destination.<br>- `MAX_ROUTE_LENGTH_EXCEEDED` indicates the requested route is too long and cannot be processed. This error occurs when more complex directions are returned. Try reducing the number of waypoints, turns, or instructions.<br>- `INVALID_REQUEST` indicates that the provided request was invalid. Common causes of this status include an invalid parameter or parameter value.<br>- `OVER_DAILY_LIMIT` indicates any of the following:<br>  - The API key is missing or invalid.<br>  - Billing has not been enabled on your account.<br>  - A self-imposed usage cap has been exceeded.<br>  - The provided method of payment is no longer valid (for example, a credit card has expired).<br>    See the [Maps FAQ](https://developers.google.com/maps/faq#over-limit-key-error) to learn how to fix this.<br>- `OVER_QUERY_LIMIT` indicates the service has received too many requests from your application within the allowed time period.<br>- `REQUEST_DENIED` indicates that the service denied use of the directions service by your application.<br>- `UNKNOWN_ERROR` indicates a directions request could not be processed due to a server error. The request may succeed if you try again. | DirectionsStatus getStatus() | setStatus(DirectionsStatus status) |
| `AvailableTravelModes` | [`List<TravelMode>`](../../doc/models/travel-mode.md) | Optional | Contains an array of available travel modes. This field is returned when a request specifies a travel mode and gets no results. The array contains the available travel modes in the countries of the given set of waypoints. This field is not returned if one or more of the waypoints are 'via waypoints'. | List<TravelMode> getAvailableTravelModes() | setAvailableTravelModes(List<TravelMode> availableTravelModes) |
| `ErrorMessage` | `String` | Optional | When the service returns a status code other than `OK`, there may be an additional `error_message` field within the response object. This field contains more detailed information about the reasons behind the given status code. This field is not always returned, and its content is subject to change. | String getErrorMessage() | setErrorMessage(String errorMessage) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example (as JSON)

```json
{
  "routes": [
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
      "copyrights": "copyrights4",
      "summary": "summary8",
      "waypoint_order": [
        97
      ],
      "warnings": [
        "warnings2"
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
  ],
  "status": "OK",
  "geocoded_waypoints": [
    {
      "geocoder_status": "OK",
      "partial_match": {
        "key1": "val1",
        "key2": "val2"
      },
      "place_id": "place_id4",
      "types": [
        "administrative_area_level_4",
        "administrative_area_level_5",
        "amusement_park"
      ],
      "exampleAdditionalProperty": {
        "key1": "val1",
        "key2": "val2"
      }
    },
    {
      "geocoder_status": "OK",
      "partial_match": {
        "key1": "val1",
        "key2": "val2"
      },
      "place_id": "place_id4",
      "types": [
        "administrative_area_level_4",
        "administrative_area_level_5",
        "amusement_park"
      ],
      "exampleAdditionalProperty": {
        "key1": "val1",
        "key2": "val2"
      }
    },
    {
      "geocoder_status": "OK",
      "partial_match": {
        "key1": "val1",
        "key2": "val2"
      },
      "place_id": "place_id4",
      "types": [
        "administrative_area_level_4",
        "administrative_area_level_5",
        "amusement_park"
      ],
      "exampleAdditionalProperty": {
        "key1": "val1",
        "key2": "val2"
      }
    }
  ],
  "available_travel_modes": [
    "WALKING",
    "DRIVING",
    "BICYCLING"
  ],
  "error_message": "error_message0",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

