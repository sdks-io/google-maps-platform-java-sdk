
# Geolocation Request

The request body must be formatted as JSON. The following fields are supported, and all fields are optional.

*This model accepts additional fields of type Object.*

## Structure

`GeolocationRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `HomeMobileCountryCode` | `Integer` | Optional | The cell tower's Mobile Country Code (MCC). | Integer getHomeMobileCountryCode() | setHomeMobileCountryCode(Integer homeMobileCountryCode) |
| `HomeMobileNetworkCode` | `Integer` | Optional | The cell tower's Mobile Network Code. This is the MNC for GSM and WCDMA; CDMA uses the System ID (SID). | Integer getHomeMobileNetworkCode() | setHomeMobileNetworkCode(Integer homeMobileNetworkCode) |
| `RadioType` | `String` | Optional | The mobile radio type. Supported values are lte, gsm, cdma, and wcdma. While this field is optional, it should be included if a value is available, for more accurate results. | String getRadioType() | setRadioType(String radioType) |
| `Carrier` | `String` | Optional | The carrier name. | String getCarrier() | setCarrier(String carrier) |
| `ConsiderIp` | `String` | Optional | Specifies whether to fall back to IP geolocation if wifi and cell tower signals are not available. Defaults to true. Set considerIp to false to disable fall back. | String getConsiderIp() | setConsiderIp(String considerIp) |
| `CellTowers` | [`List<CellTower>`](../../doc/models/cell-tower.md) | Optional | The request body's cellTowers array contains zero or more cell tower objects. | List<CellTower> getCellTowers() | setCellTowers(List<CellTower> cellTowers) |
| `WifiAccessPoints` | [`List<WiFiAccessPoint>`](../../doc/models/wi-fi-access-point.md) | Optional | An array of two or more WiFi access point objects. | List<WiFiAccessPoint> getWifiAccessPoints() | setWifiAccessPoints(List<WiFiAccessPoint> wifiAccessPoints) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example (as JSON)

```json
{
  "homeMobileCountryCode": 172,
  "homeMobileNetworkCode": 120,
  "radioType": "radioType6",
  "carrier": "carrier4",
  "considerIp": "considerIp6",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

