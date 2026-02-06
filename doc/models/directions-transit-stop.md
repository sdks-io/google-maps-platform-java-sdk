
# Directions Transit Stop

*This model accepts additional fields of type Object.*

## Structure

`DirectionsTransitStop`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Location` | [`LatLngLiteral`](../../doc/models/lat-lng-literal.md) | Required | An object describing a specific location with Latitude and Longitude in decimal degrees. | LatLngLiteral getLocation() | setLocation(LatLngLiteral location) |
| `Name` | `String` | Required | The name of the transit stop. | String getName() | setName(String name) |
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
  "name": "name6",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

