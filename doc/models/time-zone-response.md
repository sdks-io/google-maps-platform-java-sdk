
# Time Zone Response

*This model accepts additional fields of type Object.*

## Structure

`TimeZoneResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DstOffset` | `Double` | Optional | The offset for daylight-savings time in seconds. This will be zero if the time zone is not in Daylight Savings Time during the specified `timestamp`. | Double getDstOffset() | setDstOffset(Double dstOffset) |
| `RawOffset` | `Double` | Optional | The offset from UTC (in seconds) for the given location. This does not take into effect daylight savings. | Double getRawOffset() | setRawOffset(Double rawOffset) |
| `TimeZoneId` | `String` | Optional | a string containing the ID of the time zone, such as "America/Los_Angeles" or "Australia/Sydney". These IDs are defined by [Unicode Common Locale Data Repository (CLDR) project](http://cldr.unicode.org/), and currently available in file timezone.xml. When a timezone has several IDs, the canonical one is returned. In xml responses, this is the first alias of each timezone. For example, "Asia/Calcutta" is returned, not "Asia/Kolkata". | String getTimeZoneId() | setTimeZoneId(String timeZoneId) |
| `TimeZoneName` | `String` | Optional | The long form name of the time zone. This field will be localized if the language parameter is set. eg. `Pacific Daylight Time` or `Australian Eastern Daylight Time`. | String getTimeZoneName() | setTimeZoneName(String timeZoneName) |
| `Status` | [`TimeZoneStatus`](../../doc/models/time-zone-status.md) | Required | The `status` field within the Time Zone response object contains the status of the request. The `status` field may contain the following values:<br><br>- `OK` indicates that the request was successful.<br><br>- `INVALID_REQUEST` indicates that the request was malformed.<br><br>- `OVER_DAILY_LIMIT` indicates any of the following:<br>  <br>  - The API key is missing or invalid.<br>  - Billing has not been enabled on your account.<br>  - A self-imposed usage cap has been exceeded.<br>  - The provided method of payment is no longer valid (for example, a credit card has expired).<br><br>- `OVER_QUERY_LIMIT` indicates the requestor has exceeded quota.<br><br>- `REQUEST_DENIED` indicates that the API did not complete the request. Confirm that the request was sent over HTTPS instead of HTTP.<br><br>- `UNKNOWN_ERROR` indicates an unknown error.<br><br>- `ZERO_RESULTS` indicates that no time zone data could be found for the specified position or time. Confirm that the request is for a location on land, and not over water. | TimeZoneStatus getStatus() | setStatus(TimeZoneStatus status) |
| `ErrorMessage` | `String` | Optional | Detailed information about the reasons behind the given status code. Included if status other than `Ok`. | String getErrorMessage() | setErrorMessage(String errorMessage) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example (as JSON)

```json
{
  "dstOffset": 160.82,
  "rawOffset": 75.7,
  "timeZoneId": "timeZoneId4",
  "timeZoneName": "timeZoneName6",
  "status": "OVER_QUERY_LIMIT",
  "errorMessage": "errorMessage6",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

