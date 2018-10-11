# City of Santa Monica public API for events
This is an example of how to use the events API from [data.smgov.net](https://data.smgov.net)

* [Example page](https://jimthoburn.github.io/santa-monica-events/)
* [Source code](https://github.com/jimthoburn/santa-monica-events/blob/master/index.html)

The API is running on [Socrata](https://dev.socrata.com/docs/endpoints.html), which provides a [query language similar to SQL](https://dev.socrata.com/docs/queries/).

The example is using client-side JavaScript to fetch the API data, and present it on a web page.

## Example API requests

### All events
```https://data.smgov.net/resource/tu9m-76aw.json```

### Only locations and calendars
```https://data.smgov.net/resource/tu9m-76aw.json?$select=calendar,location&$order=calendar,location&$group=calendar,location```

### Events at the “Woodlawn Cemetery & Mausoleum”
https://data.smgov.net/resource/tu9m-76aw.json?location=Woodlawn%20Cemetery%20%26%20Mausoleum

### Events from the “parks” calendar
https://data.smgov.net/resource/tu9m-76aw.json?calendar=parks

### Events with a type of “Arts/Crafts, Class/Workshop, Discussion/Q&A”
https://data.smgov.net/resource/tu9m-76aw.json?event_types=Arts%2FCrafts%2C%20Class%2FWorkshop%2C%20Discussion%2FQ%26A

## Example data
The data that comes back from the API is a JSON object, which looks like this…

```
{
  {
    "address_address": "415 Pacific Coast Highway",
    "address_city": "Santa Monica",
    "address_state": "CA",
    "address_zip": "90402",
    "age_groups": "All Ages",
    "all_day": true,
    "calendar": "beaches",
    "description": "View Deck will be CLOSED for a private event.",
    "detail_url": "http://calendar.smgov.net/beaches/eventsignup.asp?ID=21799",
    "detail_url_description": "http://calendar.smgov.net/beaches/eventsignup.asp?ID=21799",
    "end_date": "2018-10-14T00:00:00.000",
    "event_id": "21799",
    "event_types": "Facility/Street Closures",
    "id": "beaches_21799",
    "is_cancelled": false,
    "location": "Annenberg Community Beach House",
    "signup_url": "http://calendar.smgov.net/beaches/eventsignup.asp?ID=21799",
    "signup_url_description": "http://calendar.smgov.net/beaches/eventsignup.asp?ID=21799",
    "start_date": "2018-10-14T00:00:00.000",
    "title": "View Deck will be CLOSED all day"
  },
  {
    "address_address": "415 Pacific Coast Highway",
    "address_city": "Santa Monica",
    "address_state": "CA",
    "address_zip": "90402",
    "age_groups": "All Ages",
    "all_day": true,
    "calendar": "beaches",
    "description": "View Deck will be CLOSED for a private event.",
    "detail_url": "http://calendar.smgov.net/beaches/eventsignup.asp?ID=21799",
    "detail_url_description": "http://calendar.smgov.net/beaches/eventsignup.asp?ID=21799",
    "end_date": "2018-10-14T00:00:00.000",
    "event_id": "21799",
    "event_types": "Facility/Street Closures",
    "id": "beaches_21799",
    "is_cancelled": false,
    "location": "Annenberg Community Beach House",
    "signup_url": "http://calendar.smgov.net/beaches/eventsignup.asp?ID=21799",
    "signup_url_description": "http://calendar.smgov.net/beaches/eventsignup.asp?ID=21799",
    "start_date": "2018-10-14T00:00:00.000",
    "title": "View Deck will be CLOSED all day"
  },
  {
    ":@computed_region_28yu_qtqf": "368",
    ":@computed_region_a96n_jaww": "15",
    "address": {
      "type": "Point",
      "coordinates": [-118.493556, 34.0185]
    },
    "address_address": "601 Santa Monica Boulevard",
    "address_city": "Santa Monica",
    "address_state": "CA",
    "address_zip": "90401",
    "age_groups": "Adults",
    "all_day": false,
    "calendar": "library",
    "contact_email": "nancy.bender@smgov.net",
    "contact_name": "Nancy Bender",
    "contact_phone": "310-458-8922",
    "description": "English as a Second Language (ESL), Multi Level HIGH<br />Santa Monica Public Library hosts an ongoing series of English as a Second Language (ESL) classes taught by Adult Education Center instructors. Classes are free and students must be <br />18 years or older to attend. Community parents and SMMUSD parents have priority enrollment. Learn more about California adult education at caladulted.org. Enrollment is through the Santa Monica-Malibu Unified School District Adult Education Center, located at 2510 Lincoln Blvd., Room 203, Santa Monica, 90405. Contact Olga Saucedo at (310) 664-6222, ext. 76203 to enroll.<br /> <br />Ingl?s como segundo idioma (ESL), ALTO NIVEL<br />Santa Monica Public Library presenta una serie continua de clases de Ingl?s como segundo idioma (ESL) que son ense?ada por los instructores del Centro de Educaci?n para Adultos. Las clases son gratuitas y los estudiantes deben ser mayores de 18 a?os. Los padres de la comunidad y los padres del distrito escolar de (SMMUSD) tendr?n prioridad para la matr?cula. Visita caladulted.org para aprender m?s de educaci?n para adultos en California. La matr?cula es a trav?s del Centro de Educaci?n para Adultos de SMMUSD, situado por la 2510 Lincoln Blvd., Cuarto 203, Santa M?nica, CA 90405. Comun?quese con Olga Saucedo al (310) 664-6222 ext. 76203 para matricularse.<br />",
    "detail_url": "http://calendar.smgov.net/library/eventsignup.asp?ID=27485",
    "detail_url_description": "http://calendar.smgov.net/library/eventsignup.asp?ID=27485",
    "end_date": "2019-03-07T14:45:00.000",
    "event_id": "27485",
    "event_types": "Life Long Learning",
    "id": "library_27485",
    "is_cancelled": false,
    "location": "Main Library",
    "signup_url": "http://calendar.smgov.net/library/eventsignup.asp?ID=27485",
    "signup_url_description": "http://calendar.smgov.net/library/eventsignup.asp?ID=27485",
    "start_date": "2019-03-07T11:45:00.000",
    "title": "ESL, Multi Level HIGH / ESL, ALTO NIVEL"
  },
  {
    ":@computed_region_28yu_qtqf": "363",
    ":@computed_region_a96n_jaww": "20",
    "address": {
      "type": "Point",
      "coordinates": [-118.463583, 34.014667]
    },
    "address_address": "2101 Ocean Park Boulevard",
    "address_city": "Santa Monica",
    "address_state": "CA",
    "address_zip": "90405",
    "age_groups": "Kids",
    "all_day": false,
    "calendar": "library",
    "description": "Use a free computer program called Tinkercad to create Minecraft-style glasses for 3D printing. No prior experience required. <br />GRADES 2 - 6<br />Space is limited; registration begins 11/1.",
    "detail_url": "http://calendar.smgov.net/library/eventsignup.asp?ID=28300",
    "detail_url_description": "http://calendar.smgov.net/library/eventsignup.asp?ID=28300",
    "end_date": "2018-11-17T12:00:00.000",
    "event_id": "28300",
    "event_types": "Class/Workshop, Computer Classes/Technology",
    "id": "library_28300",
    "is_cancelled": false,
    "location": "Fairview Branch Library",
    "signup_url": "http://calendar.smgov.net/library/eventsignup.asp?ID=28300",
    "signup_url_description": "http://calendar.smgov.net/library/eventsignup.asp?ID=28300",
    "start_date": "2018-11-17T10:30:00.000",
    "title": "Design in 3D: Minecraft Glasses"
  }
}
```
