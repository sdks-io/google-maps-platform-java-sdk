
# Result

*This model accepts additional fields of type Object.*

## Structure

`Result`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Elevation` | `Double` | Optional | - | Double getElevation() | setElevation(Double elevation) |
| `Resolution` | `Double` | Optional | - | Double getResolution() | setResolution(Double resolution) |
| `Location` | [`LatLngLiteral`](../../doc/models/lat-lng-literal.md) | Optional | An object describing a specific location with Latitude and Longitude in decimal degrees. | LatLngLiteral getLocation() | setLocation(LatLngLiteral location) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example (as JSON)

```json
{
  "elevation": 143.32,
  "resolution": 45.26,
  "location": {
    "lat": 205.22,
    "lng": 218.24,
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

