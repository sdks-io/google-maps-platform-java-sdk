
# Latitude Longitude Literal

An object describing a specific location with Latitude and Longitude in decimal degrees.

*This model accepts additional fields of type Object.*

## Structure

`LatitudeLongitudeLiteral`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Latitude` | `double` | Required | Latitude in decimal degrees | double getLatitude() | setLatitude(double latitude) |
| `Longitude` | `double` | Required | Longitude in decimal degrees | double getLongitude() | setLongitude(double longitude) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example (as JSON)

```json
{
  "latitude": 92.4,
  "longitude": 161.4,
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

