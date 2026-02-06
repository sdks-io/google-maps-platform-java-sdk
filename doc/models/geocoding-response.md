
# Geocoding Response

*This model accepts additional fields of type Object.*

## Structure

`GeocodingResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `PlusCode` | [`PlusCode`](../../doc/models/plus-code.md) | Optional | An encoded location reference, derived from latitude and longitude coordinates, that represents an area, 1/8000th of a degree by 1/8000th of a degree (about 14m x 14m at the equator) or smaller. Plus codes can be used as a replacement for street addresses in places where they do not exist (where buildings are not numbered or streets are not named).<br><br>Site describing Plus Codes.: [https://plus.codes/](https://plus.codes/)<br><br>Site describing Plus Codes.: [https://plus.codes/](https://plus.codes/) | PlusCode getPlusCode() | setPlusCode(PlusCode plusCode) |
| `Results` | [`List<GeocodingResult>`](../../doc/models/geocoding-result.md) | Required | - | List<GeocodingResult> getResults() | setResults(List<GeocodingResult> results) |
| `Status` | [`GeocodingStatus`](../../doc/models/geocoding-status.md) | Required | The `status` field within the Geocoding response object contains the status of the request, and may contain debugging information to help you track down why geocoding is not working. The "status" field may contain the following values:<br><br>- `OK` indicates that no errors occurred; the address was successfully parsed and at least one geocode was returned.<br>- `ZERO_RESULTS` indicates that the geocode was successful but returned no results. This may occur if the geocoder was passed a non-existent address or a `latlng` in a remote location.<br>- `OVER_DAILY_LIMIT` indicates any of the following:<br>  - The API key is missing or invalid.<br>  - Billing has not been enabled on your account.<br>  - A self-imposed usage cap has been exceeded.<br>  - The provided method of payment is no longer valid (for example, a credit card has expired).<br>- `OVER_QUERY_LIMIT` indicates that you are over your quota.<br>- `REQUEST_DENIED` indicates that your request was denied.<br>- `INVALID_REQUEST` generally indicates that the query (address, components, or latlng) is missing.<br>- `UNKNOWN_ERROR` indicates that the request could not be processed due to a server error. The request may succeed if you try again. | GeocodingStatus getStatus() | setStatus(GeocodingStatus status) |
| `ErrorMessage` | `String` | Optional | A short description of the error. | String getErrorMessage() | setErrorMessage(String errorMessage) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example (as JSON)

```json
{
  "results": [
    {
      "address_components": [
        {
          "long_name": "Council of the City of Sydney",
          "short_name": "Sydney",
          "types": [
            "administrative_area_level_2",
            "political"
          ],
          "exampleAdditionalProperty": {
            "key1": "val1",
            "key2": "val2"
          }
        }
      ],
      "formatted_address": "formatted_address8",
      "geometry": {
        "location": {
          "lat": 205.22,
          "lng": 218.24,
          "exampleAdditionalProperty": {
            "key1": "val1",
            "key2": "val2"
          }
        },
        "location_type": "ROOFTOP",
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
      },
      "place_id": "place_id0",
      "types": [
        "types5",
        "types6",
        "types7"
      ],
      "plus_code": {
        "compound_code": "compound_code2",
        "global_code": "global_code4",
        "exampleAdditionalProperty": {
          "key1": "val1",
          "key2": "val2"
        }
      },
      "postcode_localities": [
        "postcode_localities9"
      ],
      "partial_match": false,
      "exampleAdditionalProperty": {
        "key1": "val1",
        "key2": "val2"
      }
    }
  ],
  "status": "OVER_DAILY_LIMIT",
  "error_message": "Invalid request. Missing the `address`, `components`, `latlng` or `place_id` parameter.",
  "plus_code": {
    "compound_code": "compound_code2",
    "global_code": "global_code4",
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

