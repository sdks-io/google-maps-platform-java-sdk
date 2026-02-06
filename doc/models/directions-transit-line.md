
# Directions Transit Line

*This model accepts additional fields of type Object.*

## Structure

`DirectionsTransitLine`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Agencies` | [`List<DirectionsTransitAgency>`](../../doc/models/directions-transit-agency.md) | Required | The transit agency (or agencies) that operates this transit line. | List<DirectionsTransitAgency> getAgencies() | setAgencies(List<DirectionsTransitAgency> agencies) |
| `Color` | `String` | Optional | The color commonly used in signage for this line. | String getColor() | setColor(String color) |
| `Name` | `String` | Required | The full name of this transit line, e.g. "8 Avenue Local". | String getName() | setName(String name) |
| `ShortName` | `String` | Optional | The short name of this transit line. This will normally be a line number, such as "M7" or "355". | String getShortName() | setShortName(String shortName) |
| `TextColor` | `String` | Optional | The color commonly used in signage for this line. | String getTextColor() | setTextColor(String textColor) |
| `Url` | `String` | Optional | Contains the URL for this transit line as provided by the transit agency. | String getUrl() | setUrl(String url) |
| `Icon` | `String` | Optional | Contains the URL for the icon associated with this line. | String getIcon() | setIcon(String icon) |
| `Vehicle` | [`DirectionsTransitVehicle`](../../doc/models/directions-transit-vehicle.md) | Optional | - | DirectionsTransitVehicle getVehicle() | setVehicle(DirectionsTransitVehicle vehicle) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example (as JSON)

```json
{
  "agencies": [
    {
      "name": "name8",
      "phone": "phone2",
      "url": "url2",
      "exampleAdditionalProperty": {
        "key1": "val1",
        "key2": "val2"
      }
    }
  ],
  "color": "#ce8e00",
  "name": "name0",
  "text_color": "#121212",
  "short_name": "short_name8",
  "url": "url4",
  "icon": "icon2",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

