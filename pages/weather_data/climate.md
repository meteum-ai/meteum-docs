## Climate data {#climate-data}

Using the Meteum API, you can view the average statistics of climate data for the last 10 years. The data can be detailed by days, weeks or months.

To get climate data for the selected geographical point, it is necessary to specify the `climate` object in the request when calling the GraphQL method `weatherByPoint`:

```graphql
{
  weatherByPoint(request: { lat: 53.718706,  lon: 44.453126 }) {
    climate {
      ...
    }
  }
}
```

Inside the `climate` object, you must specify one of the objects to drill down the request with optional parameters `limit` and `offset`:

* `days' – by days.
* `weeks' – by week.
* `months' – by month.

The fields to be received in the response are specified inside these objects. By default, data is returned for the entire year from its beginning: the first day, week or month. Using the `limit` and `offset` parameters, you can set the desired period:

* `limit` defines the number of records to be returned.
* `offset` determines how many records to skip since the beginning of the year.

Example of a request for obtaining average climatic data at a point for the period from January 1st to January 10th:

```graphql
{
  weatherByPoint(request: { lat: 53.718706,  lon: 44.453126 }) {
    climate {
      days(limit: 10) {
        maxDayTemperature
        humidity
        pressure
        maxWindSpeed
        minWindSpeed
        prec
        precType
        precStrength
      }
    }
  }
}
```

{% cut "Response" %}

```json
{
  "data": {
    "weatherByPoint": {
      "climate": {
        "days": [
          {
            "maxDayTemperature": -5,
            "humidity": 89,
            "pressure": 736,
            "maxWindSpeed": 6,
            "minWindSpeed": 3,
            "prec": 2.2,
            "precType": "NO_TYPE",
            "precStrength": "ZERO"
          },
          {
            "maxDayTemperature": -5,
            "humidity": 91,
            "pressure": 735,
            "maxWindSpeed": 6.5,
            "minWindSpeed": 3.7,
            "prec": 2.5,
            "precType": "SNOW",
            "precStrength": "AVERAGE"
          },
          {
            "maxDayTemperature": -6,
            "humidity": 88,
            "pressure": 734,
            "maxWindSpeed": 6.3,
            "minWindSpeed": 3.5,
            "prec": 2,
            "precType": "SNOW",
            "precStrength": "AVERAGE"
          },
          {
            "maxDayTemperature": -8,
            "humidity": 87,
            "pressure": 734,
            "maxWindSpeed": 5.8,
            "minWindSpeed": 3.5,
            "prec": 2.2,
            "precType": "SNOW",
            "precStrength": "AVERAGE"
          },
          {
            "maxDayTemperature": -8,
            "humidity": 88,
            "pressure": 736,
            "maxWindSpeed": 5.5,
            "minWindSpeed": 3.4,
            "prec": 1.8,
            "precType": "SNOW",
            "precStrength": "AVERAGE"
          },
          {
            "maxDayTemperature": -9,
            "humidity": 87,
            "pressure": 739,
            "maxWindSpeed": 5.4,
            "minWindSpeed": 3.5,
            "prec": 1.2,
            "precType": "NO_TYPE",
            "precStrength": "ZERO"
          },
          {
            "maxDayTemperature": -10,
            "humidity": 87,
            "pressure": 741,
            "maxWindSpeed": 5.5,
            "minWindSpeed": 3.7,
            "prec": 1.7,
            "precType": "NO_TYPE",
            "precStrength": "ZERO"
          },
          {
            "maxDayTemperature": -10,
            "humidity": 87,
            "pressure": 741,
            "maxWindSpeed": 6.5,
            "minWindSpeed": 4,
            "prec": 1.7,
            "precType": "NO_TYPE",
            "precStrength": "ZERO"
          },
          {
            "maxDayTemperature": -8,
            "humidity": 88,
            "pressure": 738,
            "maxWindSpeed": 5,
            "minWindSpeed": 3,
            "prec": 1.8,
            "precType": "SNOW",
            "precStrength": "AVERAGE"
          },
          {
            "maxDayTemperature": -10,
            "humidity": 88,
            "pressure": 736,
            "maxWindSpeed": 5,
            "minWindSpeed": 2.9,
            "prec": 0.6,
            "precType": "NO_TYPE",
            "precStrength": "ZERO"
          }
        ]
      }
    }
  }
}
```

{% endcut %}

Example of a request for obtaining average climatic data at a point for the period from January 11th to January 20th:

```graphql
{
  weatherByPoint(request: { lat: 53.718706,  lon: 44.453126 }) {
    climate {
      days(limit: 10, offset: 10){
        maxDayTemperature
        humidity
        pressure
        maxWindSpeed
        minWindSpeed
        prec
        precType
        precStrength
      }
    }
  }
}
```

{% cut "Response" %}

```json
{
  "data": {
    "weatherByPoint": {
      "climate": {
        "days": [
          {
            "maxDayTemperature": -10,
            "humidity": 86,
            "pressure": 736,
            "maxWindSpeed": 5.4,
            "minWindSpeed": 3.4,
            "prec": 1.7,
            "precType": "NO_TYPE",
            "precStrength": "ZERO"
          },
          {
            "maxDayTemperature": -7,
            "humidity": 88,
            "pressure": 736,
            "maxWindSpeed": 6.5,
            "minWindSpeed": 3.5,
            "prec": 1,
            "precType": "NO_TYPE",
            "precStrength": "ZERO"
          },
          {
            "maxDayTemperature": -5,
            "humidity": 92,
            "pressure": 732,
            "maxWindSpeed": 7.5,
            "minWindSpeed": 4.5,
            "prec": 2.7,
            "precType": "SNOW",
            "precStrength": "AVERAGE"
          },
          {
            "maxDayTemperature": -4,
            "humidity": 93,
            "pressure": 734,
            "maxWindSpeed": 6.5,
            "minWindSpeed": 4.4,
            "prec": 1.6,
            "precType": "SNOW",
            "precStrength": "AVERAGE"
          },
          {
            "maxDayTemperature": -5,
            "humidity": 92,
            "pressure": 737,
            "maxWindSpeed": 5.5,
            "minWindSpeed": 3.2,
            "prec": 1.6,
            "precType": "NO_TYPE",
            "precStrength": "ZERO"
          },
          {
            "maxDayTemperature": -6,
            "humidity": 92,
            "pressure": 739,
            "maxWindSpeed": 5,
            "minWindSpeed": 2.5,
            "prec": 2.7,
            "precType": "SNOW",
            "precStrength": "AVERAGE"
          },
          {
            "maxDayTemperature": -7,
            "humidity": 89,
            "pressure": 741,
            "maxWindSpeed": 5.5,
            "minWindSpeed": 2.9,
            "prec": 1.7,
            "precType": "SNOW",
            "precStrength": "AVERAGE"
          },
          {
            "maxDayTemperature": -8,
            "humidity": 91,
            "pressure": 742,
            "maxWindSpeed": 5.4,
            "minWindSpeed": 3,
            "prec": 1.8,
            "precType": "SNOW",
            "precStrength": "AVERAGE"
          },
          {
            "maxDayTemperature": -9,
            "humidity": 89,
            "pressure": 740,
            "maxWindSpeed": 4.5,
            "minWindSpeed": 3,
            "prec": 1,
            "precType": "NO_TYPE",
            "precStrength": "ZERO"
          },
          {
            "maxDayTemperature": -8,
            "humidity": 88,
            "pressure": 739,
            "maxWindSpeed": 5,
            "minWindSpeed": 3.2,
            "prec": 1.2,
            "precType": "NO_TYPE",
            "precStrength": "ZERO"
          }
        ]
      }
    }
  }
}
```

{% endcut %}
