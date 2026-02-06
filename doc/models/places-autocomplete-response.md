
# Places Autocomplete Response

*This model accepts additional fields of type Object.*

## Structure

`PlacesAutocompleteResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Predictions` | [`List<PlaceAutocompletePrediction>`](../../doc/models/place-autocomplete-prediction.md) | Required | Contains an array of predictions. | List<PlaceAutocompletePrediction> getPredictions() | setPredictions(List<PlaceAutocompletePrediction> predictions) |
| `Status` | [`PlacesAutocompleteStatus`](../../doc/models/places-autocomplete-status.md) | Required | Status codes returned by service.<br><br>- `OK` indicating the API request was successful.<br>- `ZERO_RESULTS` indicating that the search was successful but returned no results. This may occur if the search was passed a bounds in a remote location.<br>- `INVALID_REQUEST` indicating the API request was malformed, generally due to the missing `input` parameter.<br>- `OVER_QUERY_LIMIT` indicating any of the following:<br>  - You have exceeded the QPS limits.<br>  - Billing has not been enabled on your account.<br>  - The monthly $200 credit, or a self-imposed usage cap, has been exceeded.<br>  - The provided method of payment is no longer valid (for example, a credit card has expired).<br>    See the [Maps FAQ](https://developers.google.com/maps/faq#over-limit-key-error) for more information about how to resolve this error.<br>- `REQUEST_DENIED` indicating that your request was denied, generally because:<br>  - The request is missing an API key.<br>  - The `key` parameter is invalid.<br>- `UNKNOWN_ERROR` indicating an unknown error. | PlacesAutocompleteStatus getStatus() | setStatus(PlacesAutocompleteStatus status) |
| `ErrorMessage` | `String` | Optional | When the service returns a status code other than `OK<`, there may be an additional `error_message` field within the response object. This field contains more detailed information about thereasons behind the given status code. This field is not always returned, and its content is subject to change. | String getErrorMessage() | setErrorMessage(String errorMessage) |
| `InfoMessages` | `List<String>` | Optional | When the service returns additional information about the request specification, there may be an additional `info_messages` field within the response object. This field is only returned for successful requests. It may not always be returned, and its content is subject to change. | List<String> getInfoMessages() | setInfoMessages(List<String> infoMessages) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example (as JSON)

```json
{
  "predictions": [
    {
      "description": "Paris, France",
      "matched_substrings": [
        {
          "length": 200.82,
          "offset": 96.92,
          "exampleAdditionalProperty": {
            "key1": "val1",
            "key2": "val2"
          }
        }
      ],
      "structured_formatting": {
        "main_text": "main_text6",
        "main_text_matched_substrings": [
          {
            "length": 174.72,
            "offset": 22.62,
            "exampleAdditionalProperty": {
              "key1": "val1",
              "key2": "val2"
            }
          }
        ],
        "secondary_text": "secondary_text2",
        "secondary_text_matched_substrings": [
          {
            "length": 26.26,
            "offset": 178.36,
            "exampleAdditionalProperty": {
              "key1": "val1",
              "key2": "val2"
            }
          },
          {
            "length": 26.26,
            "offset": 178.36,
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
      },
      "terms": [
        {
          "value": "value0",
          "offset": 246.22,
          "exampleAdditionalProperty": {
            "key1": "val1",
            "key2": "val2"
          }
        }
      ],
      "place_id": "place_id8",
      "reference": "reference6",
      "types": [
        "types7",
        "types8",
        "types9"
      ],
      "distance_meters": 202,
      "exampleAdditionalProperty": {
        "key1": "val1",
        "key2": "val2"
      }
    }
  ],
  "status": "OK",
  "error_message": "error_message8",
  "info_messages": [
    "info_messages2"
  ],
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

