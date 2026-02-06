
# Place Photo

A photo of a Place. The photo can be accesed via the [Place Photo](https://developers.google.com/places/web-service/photos) API using an url in the following pattern:

```
https://maps.googleapis.com/maps/api/place/photo?maxwidth=400&photo_reference=photo_reference&key=YOUR_API_KEY
```

See [Place Photos](https://developers.google.com/places/web-service/photos) for more information.

*This model accepts additional fields of type Object.*

## Structure

`PlacePhoto`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Height` | `double` | Required | The height of the photo. | double getHeight() | setHeight(double height) |
| `Width` | `double` | Required | The width of the photo. | double getWidth() | setWidth(double width) |
| `HtmlAttributions` | `List<String>` | Required | The HTML attributions for the photo. | List<String> getHtmlAttributions() | setHtmlAttributions(List<String> htmlAttributions) |
| `PhotoReference` | `String` | Required | A string used to identify the photo when you perform a Photo request. | String getPhotoReference() | setPhotoReference(String photoReference) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example (as JSON)

```json
{
  "height": 43.48,
  "width": 134.64,
  "html_attributions": [
    "html_attributions9"
  ],
  "photo_reference": "Aap_uEDY1GahdnFHaMArH3g6W4bELCIn9yaZ0XGqh1-G2lX3OwzTExM6g-_0U8qedk5o3R1SmtMK-NMt34dDMcCNnc4DWREX0vQEH9DjvfF70ZPHo3IFbT-TU_oCNCCB3kxe36EsdXeoKEtRH74NueUIeslebZuVeteDpKvpwVqxRpZFVSjS",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

