
# Directions Step

Each element in the steps array defines a single step of the calculated directions. A step is the most atomic unit of a direction's route, containing a single step describing a specific, single instruction on the journey. E.g. "Turn left at W. 4th St." The step not only describes the instruction but also contains distance and duration information relating to how this step relates to the following step. For example, a step denoted as "Merge onto I-80 West" may contain a duration of "37 miles" and "40 minutes," indicating that the next step is 37 miles/40 minutes from this step.

When using the Directions API to search for transit directions, the steps array will include additional transit details in the form of a transit_details array. If the directions include multiple modes of transportation, detailed directions will be provided for walking or driving steps in an inner steps array. For example, a walking step will include directions from the start and end locations: "Walk to Innes Ave & Fitch St". That step will include detailed walking directions for that route in the inner steps array, such as: "Head north-west", "Turn left onto Arelious Walker", and "Turn left onto Innes Ave".

*This model accepts additional fields of type Object.*

## Structure

`DirectionsStep`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Distance` | [`TextValueObject`](../../doc/models/text-value-object.md) | Optional | An object containing a numeric value and its formatted text representation. | TextValueObject getDistance() | setDistance(TextValueObject distance) |
| `Duration` | [`TextValueObject`](../../doc/models/text-value-object.md) | Required | An object containing a numeric value and its formatted text representation. | TextValueObject getDuration() | setDuration(TextValueObject duration) |
| `EndLocation` | [`LatLngLiteral`](../../doc/models/lat-lng-literal.md) | Required | An object describing a specific location with Latitude and Longitude in decimal degrees. | LatLngLiteral getEndLocation() | setEndLocation(LatLngLiteral endLocation) |
| `HtmlInstructions` | `String` | Required | Contains formatted instructions for this step, presented as an HTML text string. This content is meant to be read as-is. Do not programmatically parse this display-only content. | String getHtmlInstructions() | setHtmlInstructions(String htmlInstructions) |
| `Maneuver` | [`Maneuver`](../../doc/models/maneuver.md) | Optional | Contains the action to take for the current step (turn left, merge, straight, etc.). Values are subject to change, and new values may be introduced without prior notice. | Maneuver getManeuver() | setManeuver(Maneuver maneuver) |
| `Polyline` | [`DirectionsPolyline`](../../doc/models/directions-polyline.md) | Required | [Polyline encoding](https://developers.google.com/maps/documentation/utilities/polylinealgorithm) is a lossy compression algorithm that allows you to store a series of coordinates as a single string. Point coordinates are encoded using signed values. If you only have a few static points, you may also wish to use the interactive polyline encoding utility.<br><br>The encoding process converts a binary value into a series of character codes for ASCII characters using the familiar base64 encoding scheme: to ensure proper display of these characters, encoded values are summed with 63 (the ASCII character '?') before converting them into ASCII. The algorithm also checks for additional character codes for a given point by checking the least significant bit of each byte group; if this bit is set to 1, the point is not yet fully formed and additional data must follow.<br><br>Additionally, to conserve space, points only include the offset from the previous point (except of course for the first point). All points are encoded in Base64 as signed integers, as latitudes and longitudes are signed values. The encoding format within a polyline needs to represent two coordinates representing latitude and longitude to a reasonable precision. Given a maximum longitude of +/- 180 degrees to a precision of 5 decimal places (180.00000 to -180.00000), this results in the need for a 32 bit signed binary integer value. | DirectionsPolyline getPolyline() | setPolyline(DirectionsPolyline polyline) |
| `StartLocation` | [`LatLngLiteral`](../../doc/models/lat-lng-literal.md) | Required | An object describing a specific location with Latitude and Longitude in decimal degrees. | LatLngLiteral getStartLocation() | setStartLocation(LatLngLiteral startLocation) |
| `TransitDetails` | [`DirectionsTransitDetails`](../../doc/models/directions-transit-details.md) | Optional | Additional information that is not relevant for other modes of transportation. | DirectionsTransitDetails getTransitDetails() | setTransitDetails(DirectionsTransitDetails transitDetails) |
| `TravelMode` | [`TravelMode`](../../doc/models/travel-mode.md) | Required | - `DRIVING` (default) indicates calculation using the road network.<br>- `BICYCLING` requests calculation for bicycling via bicycle paths & preferred streets (where available).<br>- `TRANSIT` requests calculation via public transit routes (where available).<br>- `WALKING` requests calculation for walking via pedestrian paths & sidewalks (where available). | TravelMode getTravelMode() | setTravelMode(TravelMode travelMode) |
| `Steps` | `Object` | Optional | Contains detailed directions for walking or driving steps in transit directions. Substeps are only available when travel_mode is set to "transit". The inner steps array is of the same type as steps. | Object getSteps() | setSteps(Object steps) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example (as JSON)

```json
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
  "html_instructions": "html_instructions0",
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
  "maneuver": "ferry",
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
```

