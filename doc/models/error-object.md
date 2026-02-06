
# Error Object

*This model accepts additional fields of type Object.*

## Structure

`ErrorObject`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Code` | `double` | Required | This is the same as the HTTP status of the response. | double getCode() | setCode(double code) |
| `Message` | `String` | Required | A short description of the error. | String getMessage() | setMessage(String message) |
| `Errors` | [`List<ErrorDetail>`](../../doc/models/error-detail.md) | Required | A list of errors which occurred. Each error contains an identifier for the type of error and a short description. | List<ErrorDetail> getErrors() | setErrors(List<ErrorDetail> errors) |
| `Status` | `String` | Optional | A status code that indicates the error type. | String getStatus() | setStatus(String status) |
| `Details` | [`List<ErrorDetail>`](../../doc/models/error-detail.md) | Optional | Additional details about the error. | List<ErrorDetail> getDetails() | setDetails(List<ErrorDetail> details) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example (as JSON)

```json
{
  "code": 250.76,
  "message": "message8",
  "errors": [
    {
      "message": "API key not valid. Please pass a valid API key.",
      "domain": "global",
      "reason": "badRequest",
      "@type": "@type2",
      "metadata": {
        "key1": "val1",
        "key2": "val2"
      },
      "exampleAdditionalProperty": {
        "key1": "val1",
        "key2": "val2"
      }
    }
  ],
  "status": "status0",
  "details": [
    {
      "@type": "@type2",
      "message": "message0",
      "reason": "reason6",
      "domain": "domain6",
      "metadata": {
        "key1": "val1",
        "key2": "val2"
      },
      "exampleAdditionalProperty": {
        "key1": "val1",
        "key2": "val2"
      }
    },
    {
      "@type": "@type2",
      "message": "message0",
      "reason": "reason6",
      "domain": "domain6",
      "metadata": {
        "key1": "val1",
        "key2": "val2"
      },
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
}
```

