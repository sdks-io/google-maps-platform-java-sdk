
# Directions Traffic Speed Entry

*This model accepts additional fields of type Object.*

## Structure

`DirectionsTrafficSpeedEntry`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `SpeedCategory` | `String` | Required | The current traffic/speed conditions on this portion of a path. | String getSpeedCategory() | setSpeedCategory(String speedCategory) |
| `OffsetMeters` | `double` | Required | The offset along the path (in meters) up to which this speed category is valid. | double getOffsetMeters() | setOffsetMeters(double offsetMeters) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example (as JSON)

```json
{
  "speed_category": "speed_category6",
  "offset_meters": 251.06,
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

