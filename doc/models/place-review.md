
# Place Review

A review of the place submitted by a user.

*This model accepts additional fields of type Object.*

## Structure

`PlaceReview`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AuthorName` | `String` | Required | The name of the user who submitted the review. Anonymous reviews are attributed to "A Google user". | String getAuthorName() | setAuthorName(String authorName) |
| `AuthorUrl` | `String` | Optional | The URL to the user's Google Maps Local Guides profile, if available. | String getAuthorUrl() | setAuthorUrl(String authorUrl) |
| `ProfilePhotoUrl` | `String` | Optional | The URL to the user's profile photo, if available. | String getProfilePhotoUrl() | setProfilePhotoUrl(String profilePhotoUrl) |
| `Language` | `String` | Optional | An IETF language code indicating the language of the returned review.<br>This field contains the main language tag only, and not the secondary tag indicating country or region. For example, all the English reviews are tagged as 'en', and not 'en-AU' or 'en-UK' and so on.<br>This field is empty if there is only a rating with no review text. | String getLanguage() | setLanguage(String language) |
| `OriginalLanguage` | `String` | Optional | An IETF language code indicating the original language of the review. If the review has been translated, then `original_language` != `language`.<br>This field contains the main language tag only, and not the secondary tag indicating country or region. For example, all the English reviews are tagged as 'en', and not 'en-AU' or 'en-UK' and so on.<br>This field is empty if there is only a rating with no review text. | String getOriginalLanguage() | setOriginalLanguage(String originalLanguage) |
| `Rating` | `double` | Required | The user's overall rating for this place. This is a whole number, ranging from 1 to 5. | double getRating() | setRating(double rating) |
| `RelativeTimeDescription` | `String` | Required | The time that the review was submitted in text, relative to the current time. | String getRelativeTimeDescription() | setRelativeTimeDescription(String relativeTimeDescription) |
| `Text` | `String` | Optional | The user's review. When reviewing a location with Google Places, text reviews are considered optional. Therefore, this field may be empty. Note that this field may include simple HTML markup. For example, the entity reference `&amp;` may represent an ampersand character. | String getText() | setText(String text) |
| `Time` | `double` | Required | The time that the review was submitted, measured in the number of seconds since since midnight, January 1, 1970 UTC. | double getTime() | setTime(double time) |
| `Translated` | `Boolean` | Optional | A boolean value indicating if the review was translated from the original language it was written in.<br>If a review has been translated, corresponding to a value of true, Google recommends that you indicate this to your users. For example, you can add the following string, “Translated by Google”, to the review. | Boolean getTranslated() | setTranslated(Boolean translated) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example (as JSON)

```json
{
  "author_name": "A Google User",
  "rating": 194.16,
  "relative_time_description": "relative_time_description2",
  "time": 252.02,
  "author_url": "author_url6",
  "profile_photo_url": "profile_photo_url8",
  "language": "language0",
  "original_language": "original_language6",
  "text": "text2",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

