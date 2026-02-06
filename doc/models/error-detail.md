
# Error Detail

*This model accepts additional fields of type Object.*

## Structure

`ErrorDetail`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `MType` | `String` | Optional | The type of error. | String getMType() | setMType(String mType) |
| `Message` | `String` | Optional | A short description of the error. | String getMessage() | setMessage(String message) |
| `Reason` | `String` | Optional | A reason for the error. | String getReason() | setReason(String reason) |
| `Domain` | `String` | Optional | The domain in which the error occurred. | String getDomain() | setDomain(String domain) |
| `Metadata` | `Object` | Optional | Additional metadata about the error. | Object getMetadata() | setMetadata(Object metadata) |
| `FieldViolations` | [`List<FieldViolation>`](../../doc/models/field-violation.md) | Optional | A list of field violations. | List<FieldViolation> getFieldViolations() | setFieldViolations(List<FieldViolation> fieldViolations) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example (as JSON)

```json
{
  "message": "API key not valid. Please pass a valid API key.",
  "domain": "global",
  "reason": "badRequest",
  "@type": "@type6",
  "metadata": {
    "key1": "val1",
    "key2": "val2"
  },
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

