# City of Santa Monica public API for events
This is an example of how to use the events API from [data.smgov.net](https://data.smgov.net)

* [Example page](https://jimthoburn.github.io/santa-monica-events/)
* [Source code](https://github.com/jimthoburn/santa-monica-events/blob/master/index.html)

The example is using client-side JavaScript to fetch the API data, and present it on a web page.

## Example API requests

### All events
```https://data.smgov.net/resource/tu9m-76aw.json```

### Only locations and calendars
```https://data.smgov.net/resource/tu9m-76aw.json?$select=calendar,location&$order=calendar,location&$group=calendar,location```

## Example data
The data that comes back from the API is a JSON object, which looks like this…

```
{
…
}
```
