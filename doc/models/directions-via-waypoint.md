
# Directions Via Waypoint

*This model accepts additional fields of type Object.*

## Structure

`DirectionsViaWaypoint`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Location` | [`LatLngLiteral`](../../doc/models/lat-lng-literal.md) | Optional | An object describing a specific location with Latitude and Longitude in decimal degrees. | LatLngLiteral getLocation() | setLocation(LatLngLiteral location) |
| `StepIndex` | `Integer` | Optional | The index of the step containing the waypoint. | Integer getStepIndex() | setStepIndex(Integer stepIndex) |
| `StepInterpolation` | `Double` | Optional | The position of the waypoint along the step's polyline, expressed as a ratio from 0 to 1. | Double getStepInterpolation() | setStepInterpolation(Double stepInterpolation) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example (as JSON)

```json
{
  "location": {
    "lat": 205.22,
    "lng": 218.24,
    "exampleAdditionalProperty": {
      "key1": "val1",
      "key2": "val2"
    }
  },
  "step_index": 200,
  "step_interpolation": 160.26,
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

