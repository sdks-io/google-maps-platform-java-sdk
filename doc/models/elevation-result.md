
# Elevation Result

*This model accepts additional fields of type Object.*

## Structure

`ElevationResult`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Elevation` | `double` | Required | The elevation of the location in meters. | double getElevation() | setElevation(double elevation) |
| `Resolution` | `Double` | Optional | The value indicating the maximum distance between data points from which the elevation was interpolated, in meters. This property will be missing if the resolution is not known. Note that elevation data becomes more coarse (larger resolution values) when multiple points are passed. To obtain the most accurate elevation value for a point, it should be queried independently. | Double getResolution() | setResolution(Double resolution) |
| `Location` | [`LatLngLiteral`](../../doc/models/lat-lng-literal.md) | Required | An object describing a specific location with Latitude and Longitude in decimal degrees. | LatLngLiteral getLocation() | setLocation(LatLngLiteral location) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example (as JSON)

```json
{
  "elevation": 162.84,
  "resolution": 230.26,
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

