
# Cell Tower

Attributes used to describe a cell tower. The following optional fields are not currently used, but may be included if values are available: `age`, `signalStrength`, `timingAdvance`.

*This model accepts additional fields of type Object.*

## Structure

`CellTower`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `CellId` | `int` | Required | Unique identifier of the cell. On GSM, this is the Cell ID (CID); CDMA networks use the Base Station ID (BID). WCDMA networks use the UTRAN/GERAN Cell Identity (UC-Id), which is a 32-bit value concatenating the Radio Network Controller (RNC) and Cell ID. Specifying only the 16-bit Cell ID value in WCDMA networks may return inaccurate results. | int getCellId() | setCellId(int cellId) |
| `LocationAreaCode` | `int` | Required | The Location Area Code (LAC) for GSM and WCDMA networks. The Network ID (NID) for CDMA networks. | int getLocationAreaCode() | setLocationAreaCode(int locationAreaCode) |
| `MobileCountryCode` | `int` | Required | The cell tower's Mobile Country Code (MCC). | int getMobileCountryCode() | setMobileCountryCode(int mobileCountryCode) |
| `MobileNetworkCode` | `int` | Required | The cell tower's Mobile Network Code. This is the MNC for GSM and WCDMA; CDMA uses the System ID (SID). | int getMobileNetworkCode() | setMobileNetworkCode(int mobileNetworkCode) |
| `Age` | `Integer` | Optional | The number of milliseconds since this cell was primary. If age is 0, the cellId represents a current measurement. | Integer getAge() | setAge(Integer age) |
| `SignalStrength` | `Double` | Optional | Radio signal strength measured in dBm. | Double getSignalStrength() | setSignalStrength(Double signalStrength) |
| `TimingAdvance` | `Double` | Optional | The timing advance value. | Double getTimingAdvance() | setTimingAdvance(Double timingAdvance) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example (as JSON)

```json
{
  "cellId": 42,
  "locationAreaCode": 136,
  "mobileCountryCode": 110,
  "mobileNetworkCode": 116,
  "age": 252,
  "signalStrength": 183.64,
  "timingAdvance": 53.38,
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

