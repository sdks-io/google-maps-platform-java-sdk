
# Geocoding Geometry

An object describing the location.

*This model accepts additional fields of type Object.*

## Structure

`GeocodingGeometry`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Location` | [`LatLngLiteral`](../../doc/models/lat-lng-literal.md) | Required | An object describing a specific location with Latitude and Longitude in decimal degrees. | LatLngLiteral getLocation() | setLocation(LatLngLiteral location) |
| `LocationType` | [`LocationType`](../../doc/models/location-type.md) | Required | Stores additional data about the specified location. The following values are currently supported:<br><br>- "ROOFTOP" indicates that the returned result is a precise geocode for which we have location information accurate down to street address precision.<br>- "RANGE_INTERPOLATED" indicates that the returned result reflects an approximation (usually on a road) interpolated between two precise points (such as intersections). Interpolated results are generally returned when rooftop geocodes are unavailable for a street address.<br>- "GEOMETRIC_CENTER" indicates that the returned result is the geometric center of a result such as a polyline (for example, a street) or polygon (region).<br>- "APPROXIMATE" indicates that the returned result is approximate. | LocationType getLocationType() | setLocationType(LocationType locationType) |
| `Bounds` | [`Bounds`](../../doc/models/bounds.md) | Optional | A rectangle in geographical coordinates from points at the southwest and northeast corners. | Bounds getBounds() | setBounds(Bounds bounds) |
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
  "location_type": "GEOMETRIC_CENTER",
  "bounds": {
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

