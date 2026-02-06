
# Places Details Response

*This model accepts additional fields of type Object.*

## Structure

`PlacesDetailsResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `HtmlAttributions` | `List<String>` | Required | May contain a set of attributions about this listing which must be displayed to the user (some listings may not have attribution). | List<String> getHtmlAttributions() | setHtmlAttributions(List<String> htmlAttributions) |
| `Result` | [`Place`](../../doc/models/place.md) | Required | Attributes describing a place. Not all attributes will be available for all place types. | Place getResult() | setResult(Place result) |
| `Status` | [`PlacesDetailsStatus`](../../doc/models/places-details-status.md) | Required | Status codes returned by service.<br><br>- `OK` indicating the API request was successful.<br>- `ZERO_RESULTS` indicating that the referenced location, `place_id`, was valid but no longer refers to a valid result. This may occur if the establishment is no longer in business.<br>- `NOT_FOUND` indicating that that the referenced location, `place_id`, was not found in the Places database.<br>- `INVALID_REQUEST` indicating the API request was malformed.<br>- `OVER_QUERY_LIMIT` indicating any of the following:<br>  - You have exceeded the QPS limits.<br>  - Billing has not been enabled on your account.<br>  - The monthly $200 credit, or a self-imposed usage cap, has been exceeded.<br>  - The provided method of payment is no longer valid (for example, a credit card has expired).<br>    See the [Maps FAQ](https://developers.google.com/maps/faq#over-limit-key-error) for more information about how to resolve this error.<br>- `REQUEST_DENIED` indicating that your request was denied, generally because:<br>  - The request is missing an API key.<br>  - The `key` parameter is invalid.<br>- `UNKNOWN_ERROR` indicating an unknown error. | PlacesDetailsStatus getStatus() | setStatus(PlacesDetailsStatus status) |
| `InfoMessages` | `List<String>` | Optional | When the service returns additional information about the request specification, there may be an additional `info_messages` field within the response object. This field is only returned for successful requests. It may not always be returned, and its content is subject to change. | List<String> getInfoMessages() | setInfoMessages(List<String> infoMessages) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example (as JSON)

```json
{
  "html_attributions": [
    "html_attributions1",
    "html_attributions2",
    "html_attributions3"
  ],
  "result": {
    "adr_address": "<span class=\"street-address\">48 Pirrama Rd</span>, <span class=\"locality\">Pyrmont</span> <span class=\"region\">NSW</span> <span class=\"postal-code\">2009</span>, <span class=\"country-name\">Australia</span>",
    "formatted_address": "48 Pirrama Rd, Pyrmont NSW 2009, Australia",
    "formatted_phone_number": "(02) 9374 4000",
    "icon": "https://maps.gstatic.com/mapfiles/place_api/icons/v1/png_71/generic_business-71.png",
    "international_phone_number": "+61 2 9374 4000",
    "name": "Google Workplace 6",
    "place_id": "ChIJN1t_tDeuEmsRUsoyG83frY4",
    "rating": 4.1,
    "types": [
      "point_of_interest",
      "establishment"
    ],
    "url": "https://maps.google.com/?cid=10281119596374313554",
    "user_ratings_total": 931,
    "utc_offset": 600,
    "vicinity": "48 Pirrama Road, Pyrmont",
    "website": "http://google.com",
    "address_components": [
      {
        "long_name": "long_name4",
        "short_name": "short_name0",
        "types": [
          "types7",
          "types8"
        ],
        "exampleAdditionalProperty": {
          "key1": "val1",
          "key2": "val2"
        }
      },
      {
        "long_name": "long_name4",
        "short_name": "short_name0",
        "types": [
          "types7",
          "types8"
        ],
        "exampleAdditionalProperty": {
          "key1": "val1",
          "key2": "val2"
        }
      }
    ],
    "business_status": "OPERATIONAL",
    "curbside_pickup": false,
    "current_opening_hours": {
      "open_now": false,
      "periods": [
        {
          "open": {
            "date": "date8",
            "day": 0.52,
            "time": "time4",
            "truncated": false,
            "exampleAdditionalProperty": {
              "key1": "val1",
              "key2": "val2"
            }
          },
          "close": {
            "date": "date4",
            "day": 26.5,
            "time": "time8",
            "truncated": false,
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
      ],
      "special_days": [
        {
          "date": "date4",
          "exceptional_hours": false,
          "exampleAdditionalProperty": {
            "key1": "val1",
            "key2": "val2"
          }
        },
        {
          "date": "date4",
          "exceptional_hours": false,
          "exampleAdditionalProperty": {
            "key1": "val1",
            "key2": "val2"
          }
        }
      ],
      "type": "type0",
      "weekday_text": [
        "weekday_text5",
        "weekday_text6",
        "weekday_text7"
      ],
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
  "status": "REQUEST_DENIED",
  "info_messages": [
    "info_messages0",
    "info_messages1",
    "info_messages2"
  ],
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

