
# Geometry

An object describing the location.

*This model accepts additional fields of type Object.*

## Structure

`Geometry`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Location` | [`LatLngLiteral`](../../doc/models/lat-lng-literal.md) | Required | An object describing a specific location with Latitude and Longitude in decimal degrees. | LatLngLiteral getLocation() | setLocation(LatLngLiteral location) |
| `Viewport` | [`Bounds`](../../doc/models/bounds.md) | Required | A rectangle in geographical coordinates from points at the southwest and northeast corners. | Bounds getViewport() | setViewport(Bounds viewport) |
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
  "viewport": {
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
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

