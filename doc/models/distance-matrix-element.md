
# Distance Matrix Element

*This model accepts additional fields of type Object.*

## Structure

`DistanceMatrixElement`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Fare` | [`Fare`](../../doc/models/fare.md) | Optional | The total fare for the route.<br><br>```<br>{<br>  "currency" : "USD",<br>  "value" : 6,<br>  "text" : "$6.00"<br>}<br>``` | Fare getFare() | setFare(Fare fare) |
| `Distance` | [`TextValueObject`](../../doc/models/text-value-object.md) | Optional | An object containing a numeric value and its formatted text representation. | TextValueObject getDistance() | setDistance(TextValueObject distance) |
| `DurationInTraffic` | [`TextValueObject`](../../doc/models/text-value-object.md) | Optional | An object containing a numeric value and its formatted text representation. | TextValueObject getDurationInTraffic() | setDurationInTraffic(TextValueObject durationInTraffic) |
| `Duration` | [`TextValueObject`](../../doc/models/text-value-object.md) | Optional | An object containing a numeric value and its formatted text representation. | TextValueObject getDuration() | setDuration(TextValueObject duration) |
| `Status` | [`DistanceMatrixElementStatus`](../../doc/models/distance-matrix-element-status.md) | Required | - `OK` indicates the response contains a valid result.<br>- `NOT_FOUND` indicates that the origin and/or destination of this pairing could not be geocoded.<br>- `ZERO_RESULTS` indicates no route could be found between the origin and destination.<br>- `MAX_ROUTE_LENGTH_EXCEEDED` indicates the requested route is too long and cannot be processed. | DistanceMatrixElementStatus getStatus() | setStatus(DistanceMatrixElementStatus status) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example (as JSON)

```json
{
  "fare": {
    "currency": "currency0",
    "value": 12.62,
    "text": "text0",
    "exampleAdditionalProperty": {
      "key1": "val1",
      "key2": "val2"
    }
  },
  "distance": {
    "text": "text0",
    "value": 142.22,
    "exampleAdditionalProperty": {
      "key1": "val1",
      "key2": "val2"
    }
  },
  "duration_in_traffic": {
    "text": "text6",
    "value": 178.58,
    "exampleAdditionalProperty": {
      "key1": "val1",
      "key2": "val2"
    }
  },
  "duration": {
    "text": "text6",
    "value": 224.48,
    "exampleAdditionalProperty": {
      "key1": "val1",
      "key2": "val2"
    }
  },
  "status": "OK",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

