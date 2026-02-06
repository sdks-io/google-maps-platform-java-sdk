
# Wi Fi Access Point

Attributes used to describe a WiFi access point.

*This model accepts additional fields of type Object.*

## Structure

`WiFiAccessPoint`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `MacAddress` | `String` | Required | The MAC address of the WiFi node. It's typically called a BSS, BSSID or MAC address. Separators must be `:` (colon). | String getMacAddress() | setMacAddress(String macAddress) |
| `SignalStrength` | `Integer` | Optional | The current signal strength measured in dBm. | Integer getSignalStrength() | setSignalStrength(Integer signalStrength) |
| `SignalToNoiseRatio` | `Integer` | Optional | The current signal to noise ratio measured in dB. | Integer getSignalToNoiseRatio() | setSignalToNoiseRatio(Integer signalToNoiseRatio) |
| `Age` | `Integer` | Optional | The number of milliseconds since this access point was detected. | Integer getAge() | setAge(Integer age) |
| `Channel` | `Integer` | Optional | The channel over which the client is communication with the access point. | Integer getChannel() | setChannel(Integer channel) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example (as JSON)

```json
{
  "macAddress": "macAddress8",
  "signalStrength": 222,
  "signalToNoiseRatio": 164,
  "age": 30,
  "channel": 84,
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

