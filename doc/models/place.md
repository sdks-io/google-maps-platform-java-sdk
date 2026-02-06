
# Place

Attributes describing a place. Not all attributes will be available for all place types.

*This model accepts additional fields of type Object.*

## Structure

`Place`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AddressComponents` | [`List<AddressComponent>`](../../doc/models/address-component.md) | Optional | An array containing the separate components applicable to this address. | List<AddressComponent> getAddressComponents() | setAddressComponents(List<AddressComponent> addressComponents) |
| `AdrAddress` | `String` | Optional | A representation of the place's address in the [adr microformat](http://microformats.org/wiki/adr). | String getAdrAddress() | setAdrAddress(String adrAddress) |
| `BusinessStatus` | [`BusinessStatus`](../../doc/models/business-status.md) | Optional | Indicates the operational status of the place, if it is a business. If no data exists, `business_status` is not returned. | BusinessStatus getBusinessStatus() | setBusinessStatus(BusinessStatus businessStatus) |
| `CurbsidePickup` | `Boolean` | Optional | Specifies if the business supports curbside pickup. | Boolean getCurbsidePickup() | setCurbsidePickup(Boolean curbsidePickup) |
| `CurrentOpeningHours` | [`PlaceOpeningHours`](../../doc/models/place-opening-hours.md) | Optional | An object describing the opening hours of a place. | PlaceOpeningHours getCurrentOpeningHours() | setCurrentOpeningHours(PlaceOpeningHours currentOpeningHours) |
| `Delivery` | `Boolean` | Optional | Specifies if the business supports delivery. | Boolean getDelivery() | setDelivery(Boolean delivery) |
| `DineIn` | `Boolean` | Optional | Specifies if the business supports indoor or outdoor seating options. | Boolean getDineIn() | setDineIn(Boolean dineIn) |
| `EditorialSummary` | [`PlaceEditorialSummary`](../../doc/models/place-editorial-summary.md) | Optional | Contains a summary of the place. A summary is comprised of a textual overview, and also includes the language code for these if applicable. Summary text must be presented as-is and can not be modified or altered. | PlaceEditorialSummary getEditorialSummary() | setEditorialSummary(PlaceEditorialSummary editorialSummary) |
| `FormattedAddress` | `String` | Optional | A string containing the human-readable address of this place.<br><br>Often this address is equivalent to the postal address. Note that some countries, such as the United Kingdom, do not allow distribution of true postal addresses due to licensing restrictions.<br><br>The formatted address is logically composed of one or more address components. For example, the address "111 8th Avenue, New York, NY" consists of the following components: "111" (the street number), "8th Avenue" (the route), "New York" (the city) and "NY" (the US state).<br><br>Do not parse the formatted address programmatically. Instead you should use the individual address components, which the API response includes in addition to the formatted address field. | String getFormattedAddress() | setFormattedAddress(String formattedAddress) |
| `FormattedPhoneNumber` | `String` | Optional | Contains the place's phone number in its [local format](http://en.wikipedia.org/wiki/Local_conventions_for_writing_telephone_numbers). | String getFormattedPhoneNumber() | setFormattedPhoneNumber(String formattedPhoneNumber) |
| `Geometry` | [`Geometry`](../../doc/models/geometry.md) | Optional | An object describing the location. | Geometry getGeometry() | setGeometry(Geometry geometry) |
| `Icon` | `String` | Optional | Contains the URL of a suggested icon which may be displayed to the user when indicating this result on a map. | String getIcon() | setIcon(String icon) |
| `IconBackgroundColor` | `String` | Optional | Contains the default HEX color code for the place's category. | String getIconBackgroundColor() | setIconBackgroundColor(String iconBackgroundColor) |
| `IconMaskBaseUri` | `String` | Optional | Contains the URL of a recommended icon, minus the `.svg` or `.png` file type extension. | String getIconMaskBaseUri() | setIconMaskBaseUri(String iconMaskBaseUri) |
| `InternationalPhoneNumber` | `String` | Optional | Contains the place's phone number in international format. International format includes the country code, and is prefixed with the plus, +, sign. For example, the international_phone_number for Google's Sydney, Australia office is `+61 2 9374 4000`. | String getInternationalPhoneNumber() | setInternationalPhoneNumber(String internationalPhoneNumber) |
| `Name` | `String` | Optional | Contains the human-readable name for the returned result. For `establishment` results, this is usually the canonicalized business name. | String getName() | setName(String name) |
| `OpeningHours` | [`PlaceOpeningHours`](../../doc/models/place-opening-hours.md) | Optional | An object describing the opening hours of a place. | PlaceOpeningHours getOpeningHours() | setOpeningHours(PlaceOpeningHours openingHours) |
| `PermanentlyClosed` | `Boolean` | Optional | Use `business_status` to get the operational status of businesses. | Boolean getPermanentlyClosed() | setPermanentlyClosed(Boolean permanentlyClosed) |
| `Photos` | [`List<PlacePhoto>`](../../doc/models/place-photo.md) | Optional | An array of photo objects, each containing a reference to an image. A request may return up to ten photos. More information about place photos and how you can use the images in your application can be found in the [Place Photos](https://developers.google.com/maps/documentation/places/web-service/photos) documentation. | List<PlacePhoto> getPhotos() | setPhotos(List<PlacePhoto> photos) |
| `PlaceId` | `String` | Optional | A textual identifier that uniquely identifies a place. To retrieve information about the place, pass this identifier in the `place_id` field of a Places API request. For more information about place IDs, see the [place ID overview](https://developers.google.com/maps/documentation/places/web-service/place-id). | String getPlaceId() | setPlaceId(String placeId) |
| `PlusCode` | [`PlusCode`](../../doc/models/plus-code.md) | Optional | An encoded location reference, derived from latitude and longitude coordinates, that represents an area, 1/8000th of a degree by 1/8000th of a degree (about 14m x 14m at the equator) or smaller. Plus codes can be used as a replacement for street addresses in places where they do not exist (where buildings are not numbered or streets are not named).<br><br>Site describing Plus Codes.: [https://plus.codes/](https://plus.codes/)<br><br>Site describing Plus Codes.: [https://plus.codes/](https://plus.codes/) | PlusCode getPlusCode() | setPlusCode(PlusCode plusCode) |
| `PriceLevel` | `Double` | Optional | The price level of the place, on a scale of 0 to 4. The exact amount indicated by a specific value will vary from region to region. Price levels are interpreted as follows:<br><br>- 0 Free<br>- 1 Inexpensive<br>- 2 Moderate<br>- 3 Expensive<br>- 4 Very Expensive | Double getPriceLevel() | setPriceLevel(Double priceLevel) |
| `Rating` | `Double` | Optional | Contains the place's rating, from 1.0 to 5.0, based on aggregated user reviews. | Double getRating() | setRating(Double rating) |
| `Reference` | `String` | Optional | - | String getReference() | setReference(String reference) |
| `Reservable` | `Boolean` | Optional | Specifies if the place supports reservations. | Boolean getReservable() | setReservable(Boolean reservable) |
| `Reviews` | [`List<PlaceReview>`](../../doc/models/place-review.md) | Optional | A JSON array of up to five reviews. By default, the reviews are sorted in order of relevance. Use the `reviews_sort` request parameter to control sorting.<br><br>- For `most_relevant` (default), reviews are sorted by relevance; the service will bias the results to return reviews originally written in the preferred language.<br>- For `newest`, reviews are sorted in chronological order; the preferred language does not affect the sort order.<br>  Google recommends indicating to users whether results are ordered by `most_relevant` or `newest`. | List<PlaceReview> getReviews() | setReviews(List<PlaceReview> reviews) |
| `ServesBeer` | `Boolean` | Optional | Specifies if the place serves beer. | Boolean getServesBeer() | setServesBeer(Boolean servesBeer) |
| `ServesBreakfast` | `Boolean` | Optional | Specifies if the place serves breakfast. | Boolean getServesBreakfast() | setServesBreakfast(Boolean servesBreakfast) |
| `ServesBrunch` | `Boolean` | Optional | Specifies if the place serves brunch. | Boolean getServesBrunch() | setServesBrunch(Boolean servesBrunch) |
| `ServesDinner` | `Boolean` | Optional | Specifies if the place serves dinner. | Boolean getServesDinner() | setServesDinner(Boolean servesDinner) |
| `ServesLunch` | `Boolean` | Optional | Specifies if the place serves lunch. | Boolean getServesLunch() | setServesLunch(Boolean servesLunch) |
| `ServesVegetarianFood` | `Boolean` | Optional | Specifies if the place serves vegetarian food. | Boolean getServesVegetarianFood() | setServesVegetarianFood(Boolean servesVegetarianFood) |
| `ServesWine` | `Boolean` | Optional | Specifies if the place serves wine. | Boolean getServesWine() | setServesWine(Boolean servesWine) |
| `Scope` | `String` | Optional | - | String getScope() | setScope(String scope) |
| `SecondaryOpeningHours` | [`List<PlaceOpeningHours>`](../../doc/models/place-opening-hours.md) | Optional | Contains an array of entries for the next seven days including information about secondary hours of a business. Secondary hours are different from a business's main hours. For example, a restaurant can specify drive through hours or delivery hours as its secondary hours. This field populates the `type` subfield, which draws from a predefined list of opening hours types (such as `DRIVE_THROUGH`, `PICKUP`, or `TAKEOUT`) based on the types of the place. This field includes the `special_days` subfield of all hours, set for dates that have exceptional hours. | List<PlaceOpeningHours> getSecondaryOpeningHours() | setSecondaryOpeningHours(List<PlaceOpeningHours> secondaryOpeningHours) |
| `Takeout` | `Boolean` | Optional | Specifies if the business supports takeout. | Boolean getTakeout() | setTakeout(Boolean takeout) |
| `Types` | `List<String>` | Optional | Contains an array of feature types describing the given result. See the list of [supported types](https://developers.google.com/maps/documentation/places/web-service/supported_types#table2). | List<String> getTypes() | setTypes(List<String> types) |
| `Url` | `String` | Optional | Contains the URL of the official Google page for this place. This will be the Google-owned page that contains the best available information about the place. Applications must link to or embed this page on any screen that shows detailed results about the place to the user. | String getUrl() | setUrl(String url) |
| `UserRatingsTotal` | `Double` | Optional | The total number of reviews, with or without text, for this place. | Double getUserRatingsTotal() | setUserRatingsTotal(Double userRatingsTotal) |
| `UtcOffset` | `Double` | Optional | Contains the number of minutes this place’s current timezone is offset from UTC. For example, for places in Sydney, Australia during daylight saving time this would be 660 (+11 hours from UTC), and for places in California outside of daylight saving time this would be -480 (-8 hours from UTC). | Double getUtcOffset() | setUtcOffset(Double utcOffset) |
| `Vicinity` | `String` | Optional | For establishment (`types:["establishment", ...])` results only, the `vicinity` field contains a simplified address for the place, including the street name, street number, and locality, but not the province/state, postal code, or country.<br><br>For all other results, the `vicinity` field contains the name of the narrowest political (`types:["political", ...]`) feature that is present in the address of the result.<br><br>This content is meant to be read as-is. Do not programmatically parse the formatted address. | String getVicinity() | setVicinity(String vicinity) |
| `Website` | `String` | Optional | The authoritative website for this place, such as a business' homepage. | String getWebsite() | setWebsite(String website) |
| `WheelchairAccessibleEntrance` | `Boolean` | Optional | Specifies if the place has an entrance that is wheelchair-accessible. | Boolean getWheelchairAccessibleEntrance() | setWheelchairAccessibleEntrance(Boolean wheelchairAccessibleEntrance) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example (as JSON)

```json
{
  "adr_address": "<span class=\"street-address\">48 Pirrama Rd</span>, <span class=\"locality\">Pyrmont</span> <span class=\"region\">NSW</span> <span class=\"postal-code\">2009</span>, <span class=\"country-name\">Australia</span>",
  "formatted_address": "48 Pirrama Rd, Pyrmont NSW 2009, Australia",
  "formatted_phone_number": "(02) 9374 4000",
  "icon": "https://maps.gstatic.com/mapfiles/place_api/icons/v1/png_71/generic_business-71.png",
  "international_phone_number": "+61 2 9374 4000",
  "name": "Google Workplace 6",
  "place_id": "ChIJN1t_tDeuEmsRUsoyG83frY4",
  "rating": 4.1,
  "types": [
    "point_of_interest",
    "establishment"
  ],
  "url": "https://maps.google.com/?cid=10281119596374313554",
  "user_ratings_total": 931,
  "utc_offset": 600,
  "vicinity": "48 Pirrama Road, Pyrmont",
  "website": "http://google.com",
  "address_components": [
    {
      "long_name": "long_name4",
      "short_name": "short_name0",
      "types": [
        "types7",
        "types8"
      ],
      "exampleAdditionalProperty": {
        "key1": "val1",
        "key2": "val2"
      }
    },
    {
      "long_name": "long_name4",
      "short_name": "short_name0",
      "types": [
        "types7",
        "types8"
      ],
      "exampleAdditionalProperty": {
        "key1": "val1",
        "key2": "val2"
      }
    }
  ],
  "business_status": "OPERATIONAL",
  "curbside_pickup": false,
  "current_opening_hours": {
    "open_now": false,
    "periods": [
      {
        "open": {
          "date": "date8",
          "day": 0.52,
          "time": "time4",
          "truncated": false,
          "exampleAdditionalProperty": {
            "key1": "val1",
            "key2": "val2"
          }
        },
        "close": {
          "date": "date4",
          "day": 26.5,
          "time": "time8",
          "truncated": false,
          "exampleAdditionalProperty": {
            "key1": "val1",
            "key2": "val2"
          }
        },
        "exampleAdditionalProperty": {
          "key1": "val1",
          "key2": "val2"
        }
      }
    ],
    "special_days": [
      {
        "date": "date4",
        "exceptional_hours": false,
        "exampleAdditionalProperty": {
          "key1": "val1",
          "key2": "val2"
        }
      },
      {
        "date": "date4",
        "exceptional_hours": false,
        "exampleAdditionalProperty": {
          "key1": "val1",
          "key2": "val2"
        }
      }
    ],
    "type": "type0",
    "weekday_text": [
      "weekday_text5",
      "weekday_text6",
      "weekday_text7"
    ],
    "exampleAdditionalProperty": {
      "key1": "val1",
      "key2": "val2"
    }
  },
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

