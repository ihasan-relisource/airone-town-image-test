# Asset Naming
 
 `[COUNTRYCODE]-[STATECODE]-[county_name]-[town_name].[extension]`

Where,
- `[COUNTRYCODE]` is the ISO code for country in 2 characters using capital letters, example US.
- `[STATECODE]` is 2 characters state code using capital letters, example MA. When using Google Geolocation API, this is denoted by 'administrative_area_level_1' property in USA.
- `[county_name]` is the county name in all small letters included to avoid duplicate name of towns under same state. It will not contain any special characters like apostrophe ['] and spaces will be replaced with underscore [_]. When using Google Geolocation API, this is denoted by 'administrative_area_level_2' property in USA.
- `[town_name]` is the town name in all small letters. It will not contain any special characters like apostrophe ['] and spaces will be replaced with underscore [_].
- Each part is seperated by a small dash (minus) character [-]
- `[extension]` is the file extension. Please make sure all files have the same extension, for example all should have .jpg or .png extension whichever possible. Please make sure files do not have different extensions like some having `.jpg`, some `.jpeg`, some `.png`, some `.gif` etc. Also, please make sure extensions are all small letters (e.g. not `.JPG`). Since our server will not be a Windows server, there will be case senstivity issue while fetching assets.

For a complete example, the front-end will look for the image of this object in the server using the following asset name

Town object: 
```
{
  "_id": {
    "$oid": "5feb5119d228d528236eb77e"
  },
  "county": "Lake And Peninsula",
  "lat": "56.255556",
  "level": "City",
  "long": "-158.7625",
  "name": "Chignik Lake",
  "state": "Alaska",
  "state_code": "AK"
}
```

Asset name:

`US-AK-lake_and_peninsula-chignik_lake.jpg`

