
# Nearest Roads Response

*This model accepts additional fields of type Object.*

## Structure

`NearestRoadsResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `SnappedPoints` | [`List<SnappedPoint>`](../../doc/models/snapped-point.md) | Optional | An array of snapped points. Sometimes containing several snapped points for the same point with differing placeId or location. | List<SnappedPoint> getSnappedPoints() | setSnappedPoints(List<SnappedPoint> snappedPoints) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example (as JSON)

```json
{
  "snappedPoints": [
    {
      "location": {
        "latitude": 194.62,
        "longitude": 59.18,
        "exampleAdditionalProperty": {
          "key1": "val1",
          "key2": "val2"
        }
      },
      "originalIndex": 33.24,
      "placeId": "placeId0",
      "exampleAdditionalProperty": {
        "key1": "val1",
        "key2": "val2"
      }
    },
    {
      "location": {
        "latitude": 194.62,
        "longitude": 59.18,
        "exampleAdditionalProperty": {
          "key1": "val1",
          "key2": "val2"
        }
      },
      "originalIndex": 33.24,
      "placeId": "placeId0",
      "exampleAdditionalProperty": {
        "key1": "val1",
        "key2": "val2"
      }
    },
    {
      "location": {
        "latitude": 194.62,
        "longitude": 59.18,
        "exampleAdditionalProperty": {
          "key1": "val1",
          "key2": "val2"
        }
      },
      "originalIndex": 33.24,
      "placeId": "placeId0",
      "exampleAdditionalProperty": {
        "key1": "val1",
        "key2": "val2"
      }
    }
  ],
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

