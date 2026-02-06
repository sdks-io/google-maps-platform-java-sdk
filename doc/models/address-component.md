
# Address Component

*This model accepts additional fields of type Object.*

## Structure

`AddressComponent`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `LongName` | `String` | Required | The full text description or name of the address component as returned by the Geocoder. | String getLongName() | setLongName(String longName) |
| `ShortName` | `String` | Required | An abbreviated textual name for the address component, if available. For example, an address component for the state of Alaska may have a long_name of "Alaska" and a short_name of "AK" using the 2-letter postal abbreviation. | String getShortName() | setShortName(String shortName) |
| `Types` | `List<String>` | Required | An array indicating the type of the address component. See the list of [supported types](https://developers.google.com/maps/documentation/places/web-service/supported_types). | List<String> getTypes() | setTypes(List<String> types) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example (as JSON)

```json
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
```

