
# Street View Response

*This model accepts additional fields of type Object.*

## Structure

`StreetViewResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Copyright` | `String` | Optional | Contains the copyright notices associated with this panorama. | String getCopyright() | setCopyright(String copyright) |
| `Date` | `String` | Optional | A string indicating year and month that the panorama was captured. | String getDate() | setDate(String date) |
| `Location` | [`LatLngLiteral`](../../doc/models/lat-lng-literal.md) | Optional | An object describing a specific location with Latitude and Longitude in decimal degrees. | LatLngLiteral getLocation() | setLocation(LatLngLiteral location) |
| `PanoId` | `String` | Optional | A specific panorama ID. These are generally stable, though panoramas may change ID over time as imagery is refreshed. | String getPanoId() | setPanoId(String panoId) |
| `Status` | [`StreetViewStatus`](../../doc/models/street-view-status.md) | Required | The `status` field within the Streetview Metadata response object contains the status of the request. The `status` field may contain the following values:<br><br>- `OK` indicates that no errors occurred; a panorama is found and metadata is returned.<br>- `INVALID_REQUEST` indicates that the request was malformed.<br>- `NOT_FOUND` indicates that the address string provided in the `location` parameter could not be found. This may occur if a non-existent address is given.<br>- `ZERO_RESULTS` indicates that no panorama could be found near the provided location. This may occur if a non-existent or invalid `pano` id is given.<br>- `OVER_QUERY_LIMIT` indicates the requestor has exceeded quota.<br>- `REQUEST_DENIED` indicates that your request was denied. This may occur if you did not [authorize](https://developers.google.com/maps/documentation/streetview/get-api-key) your request, or if the Street View Static API is not activated in the Google Cloud Console project containing your API key.<br>- `UNKNOWN_ERROR` indicates that the request could not be processed due to a server error. This is often a temporary status. The request may succeed if you try again | StreetViewStatus getStatus() | setStatus(StreetViewStatus status) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example (as JSON)

```json
{
  "pano_id": "tu510ie_z4ptBZYo2BGEJg",
  "status": "ZERO_RESULTS",
  "copyright": "copyright6",
  "date": "date6",
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

