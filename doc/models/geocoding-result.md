
# Geocoding Result

*This model accepts additional fields of type Object.*

## Structure

`GeocodingResult`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AddressComponents` | [`List<AddressComponent>`](../../doc/models/address-component.md) | Required | An array containing the separate components applicable to this address. | List<AddressComponent> getAddressComponents() | setAddressComponents(List<AddressComponent> addressComponents) |
| `FormattedAddress` | `String` | Required | The human-readable address of this location. | String getFormattedAddress() | setFormattedAddress(String formattedAddress) |
| `Geometry` | [`GeocodingGeometry`](../../doc/models/geocoding-geometry.md) | Required | An object describing the location. | GeocodingGeometry getGeometry() | setGeometry(GeocodingGeometry geometry) |
| `PlaceId` | `String` | Required | A unique identifier that can be used with other Google APIs. For example, you can use the `place_id` in a Places API request to get details of a local business, such as phone number, opening hours, user reviews, and more. See the [place ID overview](https://developers.google.com/places/place-id). | String getPlaceId() | setPlaceId(String placeId) |
| `PlusCode` | [`PlusCode`](../../doc/models/plus-code.md) | Optional | An encoded location reference, derived from latitude and longitude coordinates, that represents an area, 1/8000th of a degree by 1/8000th of a degree (about 14m x 14m at the equator) or smaller. Plus codes can be used as a replacement for street addresses in places where they do not exist (where buildings are not numbered or streets are not named).<br><br>Site describing Plus Codes.: [https://plus.codes/](https://plus.codes/)<br><br>Site describing Plus Codes.: [https://plus.codes/](https://plus.codes/) | PlusCode getPlusCode() | setPlusCode(PlusCode plusCode) |
| `Types` | `List<String>` | Required | The `types[]` array indicates the type of the returned result. This array contains a set of zero or more tags identifying the type of feature returned in the result. For example, a geocode of "Chicago" returns "locality" which indicates that "Chicago" is a city, and also returns "political" which indicates it is a political entity. | List<String> getTypes() | setTypes(List<String> types) |
| `PostcodeLocalities` | `List<String>` | Optional | An array denoting all the localities contained in a postal code. This is only present when the result is a postal code that contains multiple localities. | List<String> getPostcodeLocalities() | setPostcodeLocalities(List<String> postcodeLocalities) |
| `PartialMatch` | `Boolean` | Optional | Indicates that the geocoder did not return an exact match for the original request, though it was able to match part of the requested address. You may wish to examine the original request for misspellings and/or an incomplete address.<br><br>Partial matches most often occur for street addresses that do not exist within the locality you pass in the request. Partial matches may also be returned when a request matches two or more locations in the same locality. | Boolean getPartialMatch() | setPartialMatch(Boolean partialMatch) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example (as JSON)

```json
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
  "formatted_address": "formatted_address6",
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
  "place_id": "place_id8",
  "types": [
    "types3",
    "types4",
    "types5"
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
    "postcode_localities7"
  ],
  "partial_match": false,
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

