
# Fare

The total fare for the route.

```
{
  "currency" : "USD",
  "value" : 6,
  "text" : "$6.00"
}
```

*This model accepts additional fields of type Object.*

## Structure

`Fare`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Currency` | `String` | Required | An [ISO 4217 currency code](https://en.wikipedia.org/wiki/ISO_4217) indicating the currency that the amount is expressed in. | String getCurrency() | setCurrency(String currency) |
| `Value` | `double` | Required | The total fare amount, in the currency specified. | double getValue() | setValue(double value) |
| `Text` | `String` | Required | The total fare amount, formatted in the requested language. | String getText() | setText(String text) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example (as JSON)

```json
{
  "currency": "USD",
  "value": 233.4,
  "text": "$6.00",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

