
# Lat Lng Literal

An object describing a specific location with Latitude and Longitude in decimal degrees.

*This model accepts additional fields of type Object.*

## Structure

`LatLngLiteral`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Lat` | `double` | Required | Latitude in decimal degrees | double getLat() | setLat(double lat) |
| `Lng` | `double` | Required | Longitude in decimal degrees | double getLng() | setLng(double lng) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example (as JSON)

```json
{
  "lat": 174.02,
  "lng": 6.56,
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

