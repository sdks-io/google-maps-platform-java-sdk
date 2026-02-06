
# Directions Transit Agency

*This model accepts additional fields of type Object.*

## Structure

`DirectionsTransitAgency`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Name` | `String` | Optional | The name of this transit agency. | String getName() | setName(String name) |
| `Phone` | `String` | Optional | The transit agency's phone number. | String getPhone() | setPhone(String phone) |
| `Url` | `String` | Optional | The transit agency's URL. | String getUrl() | setUrl(String url) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example (as JSON)

```json
{
  "name": "name4",
  "phone": "phone4",
  "url": "url8",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

