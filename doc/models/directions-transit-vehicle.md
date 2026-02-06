
# Directions Transit Vehicle

*This model accepts additional fields of type Object.*

## Structure

`DirectionsTransitVehicle`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Icon` | `String` | Optional | Contains the URL for an icon associated with this vehicle type. | String getIcon() | setIcon(String icon) |
| `LocalIcon` | `String` | Optional | Contains the URL for the icon associated with this vehicle type, based on the local transport signage. | String getLocalIcon() | setLocalIcon(String localIcon) |
| `Name` | `String` | Required | The name of this vehicle, capitalized. | String getName() | setName(String name) |
| `Type` | [`Type1`](../../doc/models/type-1.md) | Required | The type of vehicle used.<br><br>* `BUS` -	Bus.<br>* `CABLE_CAR` -	A vehicle that operates on a cable, usually on the ground. Aerial cable cars may be of the type GONDOLA_LIFT.<br>* `COMMUTER_TRAIN` -	Commuter rail.<br>* `FERRY` -	Ferry.<br>* `FUNICULAR` -	A vehicle that is pulled up a steep incline by a cable. A Funicular typically consists of two cars, with each car acting as a counterweight for the other.<br>* `GONDOLA_LIFT` -	An aerial cable car.<br>* `HEAVY_RAIL` -	Heavy rail.<br>* `HIGH_SPEED_TRAIN` -	High speed train.<br>* `INTERCITY_BUS` -	Intercity bus.<br>* `LONG_DISTANCE_TRAIN` -	Long distance train.<br>* `METRO_RAIL` -	Light rail transit.<br>* `MONORAIL` -	Monorail.<br>* `OTHER` -	All other vehicles will return this type.<br>* `RAIL` -	Rail.<br>* `SHARE_TAXI` -	Share taxi is a kind of bus with the ability to drop off and pick up passengers anywhere on its route.<br>* `SUBWAY` -	Underground light rail.<br>* `TRAM` -	Above ground light rail.<br>* `TROLLEYBUS` -	Trolleybus. | Type1 getType() | setType(Type1 type) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example (as JSON)

```json
{
  "name": "Train",
  "type": "SHARE_TAXI",
  "icon": "icon6",
  "local_icon": "local_icon0",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

