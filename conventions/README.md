# Convention Details

Every convention must follow a specific schema, but most conventions adhering the following example will work.

```json
{
  "$id": "will-be-given-by-c2c-during-code-review",
  "name": "Antarctic FurCon",
  "slug": "antarctic-furcon",
  "popularKnown": ["AFC"],
  "officialLogo": "./logos/antarctic-furcon.png",
  "coordinates": {
    "lat": -74.69448824376582,
    "lng": 164.11305928819493
  },
  "moreInformation": [
    "https://en.wikifur.com/wiki/Antarctic_FurCon"
  ],
  "website": "https://example.com/antarctic-furcon",
  "country": "ATA",
  "address": "Zucchelli Station, Antarctica",
  "telephone": "+1 555-0126",
  "minimumAge": 21,
  "cadence": "Yearly",
  "isActive": true
}
```

|Property|Expected Information|
|--|--|
|`$id`|It's a `CUID2` string. You can [generate one here](https://www.uuid.lol/cuid2), or leave `null` and we will make one.|
|`name`|Convention name. For non-roman characters, add a parentheses, eg.: `A-FurCon (御绒聚)`|
|`slug`|Create a URL friendly slug, this will be  your **File Name** too. Using `A-FurCon (御绒聚)` above, the slug should be `a-furcon`, and your JSON file named `a-furcon.json`|
|`popularKnown`|An `Array` of names or acronyms this convention is also known. Eg.: `Midwest FurFest` could be `["MFF", "FurFest"]` - don't add acronyms if not used a lot.|
|`officialLogo`|Using your `slug` name, place a PNG, JPG or SVG inside `./logos/` subfolder. Eg.: `midwest-furfest.jpg` - your logo name **must** match your JSON name.|
|`coordinates`| If known, put the Latitude or Longitude of this event. Usually placed on the hotel or campsite it takes place, if not specific, the City is usually acceptable|
|`moreInformation`|Any supporting information like a WikiFur page and social networks links can be added here.|
|`website`|The official website for this event. Some smaller events have Facebook pages here.|
|`country`|The [**Alpha-3 ISO 3166** code](https://www.iban.com/country-codes) for the country hosting the convention. Eg.: `BRA` for Brazil, `USA` for United States or `TUV` for Tuvalu.|
|`address`|At least `<City>, <State/Province/District>, <Country>`. You can also put the complete address of the hotel.|
|`telephone`|If this convention has a dedicated line. Leave `null` if not.|
|`minimumAge`|If the convention is open to everyone, leave `null`, even if it gets restricted after a certain hour or some parts are. If the whole convention is age restricted, put the convention's minimum age to attend based on **their definition**.|
|`cadence`|Use `Yearly` if it happens only once a year, `Multiple per Year` if happens more. Add `Irregular` if the convention has no specific cadence.|
|`isActive`|Leave always `true`, except if the convention went defunct and stopped for good, then set this to `false`|