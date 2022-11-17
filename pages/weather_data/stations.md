## Weather station data {#stations-data}

The Meteum API allows you to get actual weather indicators from weather stations. To access the data, you need to specify a list of required fields in the GraphQL method `stations`. The coordinates of the area are passed as parameters of the method:

* `minLat` — minimal latitude.
* `maxLat` — maximum latitude.
* `minLon` — minimal longitude.
* `maxLon` — maximum longitude.

```graphql
{
  stations(maxLat: 53.51865768, minLat: 51.51865768, minLon: 12.37471867, maxLon: 14.37471867, language: EN) {
    id
    name
    time
    humidity
    prec
    temperature
  }
}
```

{% cut "Response" %}

```json
{
  "data": {
    "stations": [
      {
        "id": 12751,
        "name": "Berlin-Schoenefeld",
        "time": "2022-09-09T13:20:00+03:00",
        "humidity": 64,
        "prec": 0,
        "temperature": 21
      },
      {
        "id": 48025,
        "name": "Holzdorf",
        "time": "2022-09-09T11:00:00+03:00",
        "humidity": 80,
        "prec": 0,
        "temperature": 16
      },
      {
        "id": 14137,
        "name": "Holzdorf",
        "time": "2022-09-09T13:20:00+03:00",
        "humidity": 57,
        "prec": 0,
        "temperature": 22
      }
    ]
  }
}
```

{% endcut %}

The request will return the indicators of all stations that are located in the area bounded by coordinates:

* `id` — station ID.
* `name` — the name of the station.
* `time` — the time of receiving the last readings from the station.
* `humidity` — relative humidity.
* `prec` — the amount of precipitation (in millimeters).
* `temperature` — the temperature in the shade at a height of 2 meters from the ground surface.

### Station data for the period {#station-by-period}

To get the station readings for a certain period, you need to use the GraphQL method `stationsByTimeRange`. The following parameters are passed to the method:

* `request` — coordinates of the point as a pair of values `lat` (latitude of the point) and `lon` (longitude of the point).
* `timeRange` — a time interval in the form of a pair of values `from` (the beginning of the interval) and `to` (the end of the interval). The values are set in the [Unix-time](https://en.wikipedia.org/wiki/Unix_time) format.

Example:

```graphql
{
  stationsByTimeRange(request: {lat: 52.718706,  lon: 41.453126 },
                      timeRange: {from: "1662036585", to: "1662209385"}) {
    id
    time
    cloudiness
    humidity
    temperature
    prec
    windSpeed
  }
}
```

{% cut "Response" %}

```json
{
  "data": {
    "stationsByTimeRange": [
      {
        "id": 49539,
        "time": "2022-09-01T18:00:00+03:00",
        "cloudiness": "CLEAR",
        "humidity": 35,
        "temperature": 19,
        "prec": 0,
        "windSpeed": 5
      },
      {
        "id": 49539,
        "time": "2022-09-01T21:00:00+03:00",
        "cloudiness": "CLEAR",
        "humidity": 51,
        "temperature": 13,
        "prec": 0,
        "windSpeed": 2
      },
      {
        "id": 49539,
        "time": "2022-09-02T00:00:00+03:00",
        "cloudiness": "CLEAR",
        "humidity": 68,
        "temperature": 9,
        "prec": 0,
        "windSpeed": 1
      },
      {
        "id": 49539,
        "time": "2022-09-02T03:00:00+03:00",
        "cloudiness": "CLEAR",
        "humidity": 69,
        "temperature": 8,
        "prec": 0,
        "windSpeed": 1
      },
      {
        "id": 49539,
        "time": "2022-09-02T06:00:00+03:00",
        "cloudiness": "CLEAR",
        "humidity": 78,
        "temperature": 6,
        "prec": 0,
        "windSpeed": 1
      },
      {
        "id": 49539,
        "time": "2022-09-02T09:00:00+03:00",
        "cloudiness": "CLEAR",
        "humidity": 52,
        "temperature": 14,
        "prec": 0,
        "windSpeed": 6
      },
      {
        "id": 49539,
        "time": "2022-09-02T12:00:00+03:00",
        "cloudiness": "PARTLY",
        "humidity": 39,
        "temperature": 16,
        "prec": 0,
        "windSpeed": 6
      },
      {
        "id": 49539,
        "time": "2022-09-02T15:00:00+03:00",
        "cloudiness": "CLEAR",
        "humidity": 30,
        "temperature": 18,
        "prec": 0,
        "windSpeed": 7
      },
      {
        "id": 49539,
        "time": "2022-09-02T18:00:00+03:00",
        "cloudiness": "CLEAR",
        "humidity": 40,
        "temperature": 15,
        "prec": 0,
        "windSpeed": 7
      },
      {
        "id": 49539,
        "time": "2022-09-02T21:00:00+03:00",
        "cloudiness": "CLEAR",
        "humidity": 68,
        "temperature": 7,
        "prec": 0,
        "windSpeed": 1
      },
      {
        "id": 49539,
        "time": "2022-09-03T03:00:00+03:00",
        "cloudiness": "CLEAR",
        "humidity": 84,
        "temperature": 4,
        "prec": 0,
        "windSpeed": 1
      },
      {
        "id": 49539,
        "time": "2022-09-03T06:00:00+03:00",
        "cloudiness": "CLEAR",
        "humidity": 94,
        "temperature": 2,
        "prec": 0,
        "windSpeed": 1
      },
      {
        "id": 49539,
        "time": "2022-09-03T09:00:00+03:00",
        "cloudiness": "CLEAR",
        "humidity": 56,
        "temperature": 12,
        "prec": 0,
        "windSpeed": 1
      },
      {
        "id": 49539,
        "time": "2022-09-03T12:00:00+03:00",
        "cloudiness": "CLEAR",
        "humidity": 36,
        "temperature": 16,
        "prec": 0,
        "windSpeed": 2
      },
      {
        "id": 49539,
        "time": "2022-09-03T15:00:00+03:00",
        "cloudiness": "CLEAR",
        "humidity": 28,
        "temperature": 18,
        "prec": 0,
        "windSpeed": 3
      }
    ]
  }
}
```

{% endcut %}

The request will return the indicators of the station that is located closest to the specified point for the period from 01.09.2022 to 03.09.2022:

* `id` — station ID.
* `time` — the time of receiving readings from the station.
* `cloudiness` — cloud cover.
* `humidity` — relative humidity.
* `temperature` — the temperature in the shade at a height of 2 meters from the ground surface.
* `prec` — the amount of precipitation (in millimeters).
* `windSpeed` — wind speed.
