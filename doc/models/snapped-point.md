
# Snapped Point

*This model accepts additional fields of type Object.*

## Structure

`SnappedPoint`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Location` | [`LatitudeLongitudeLiteral`](../../doc/models/latitude-longitude-literal.md) | Required | An object describing a specific location with Latitude and Longitude in decimal degrees. | LatitudeLongitudeLiteral getLocation() | setLocation(LatitudeLongitudeLiteral location) |
| `OriginalIndex` | `Double` | Optional | An integer that indicates the corresponding value in the original request. Each value in the request should map to a snapped value in the response. However, if you've set interpolate=true or if you're using nearest roads, then it's possible that the response will contain more coordinates than the request. Interpolated values will not have an `originalIndex`. These values are indexed from `0`, so a point with an originalIndex of `4` will be the snapped value of the 5th latitude/longitude passed to the path parameter. Nearest Roads points may contain several points for single coordinates with differing location or placeId. | Double getOriginalIndex() | setOriginalIndex(Double originalIndex) |
| `PlaceId` | `String` | Required | A unique identifier for a place. All place IDs returned by the Roads API correspond to road segments. | String getPlaceId() | setPlaceId(String placeId) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example (as JSON)

```json
{
  "location": {
    "latitude": 194.62,
    "longitude": 59.18,
    "exampleAdditionalProperty": {
      "key1": "val1",
      "key2": "val2"
    }
  },
  "originalIndex": 95.92,
  "placeId": "placeId8",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

