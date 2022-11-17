## Forecast {#forecast}

The Meteum API can provide weather forecast data both with hourly details and aggregated by parts of the day. A detailed hourly forecast is well suited for drawing a graph of changes in a weather parameter, for detecting important changes, and for analyzing weather data. At the same time, an aggregated forecast for parts of the day is perfect for displaying in the interface or a quick assessment of the overall picture of the day.

To get the weather forecast for the selected geographical point, the `forecast` object must be specified in the request:

```graphql
{
  weatherByPoint(request: {lat: 52.37125, lon: 4.89388}) {
    forecast {
      ...
    }
  }
}
```

### Hourly forecast {#forecast_hours}

To get an hourly forecast in a request to the Meteum API inside the `forecast` object, you must specify the `hours` object with the required `first` parameter (how many hours ahead the forecast is).

The Steam API provides the possibility of [paginated output](https://graphql.org/learn/pagination/#pagination-and-edges). To specify the necessary fields in the response, you will also need nested objects `edges` and `node`.

Example:

```graphql
{
  weatherByPoint(request: { lat: 52.37125, lon: 4.89388 }) {
    forecast {
      hours(first: 4) {  # first 4 hours only
        edges {
          node {
            temperature
            time
          }
        }
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
      "forecast": {
        "hours": {
          "edges": [
            {
              "node": {
                "temperature": 26,
                "time": "2022-09-06T14:00:00+02:00"
              }
            },
            {
              "node": {
                "temperature": 26,
                "time": "2022-09-06T15:00:00+02:00"
              }
            },
            {
              "node": {
                "temperature": 25,
                "time": "2022-09-06T16:00:00+02:00"
              }
            },
            {
              "node": {
                "temperature": 23,
                "time": "2022-09-06T17:00:00+02:00"
              }
            }
          ]
        }
      }
    }
  }
}
```

{% endcut %}

### Forecast by parts of the day {#forecast_day_parts}

To get a forecast aggregated by days, you must specify the `days` object in the `forecast` object (in the optional `limit` parameter, you can specify how many days ahead the forecast is needed).
Inside the `days` object, you can request data related to the entire day. For example, the time of sunrise and sunset, as well as separate data for parts of the day:
- `morning` – aggregated forecast for the morning
- `day` – aggregated forecast for the day
- `evening` – aggregated forecast for the evening
- `night` – aggregated forecast for the night
Just as before, inside the objects defining the requested part of the day, you need to specify which weather parameters are needed.

Example:

```graphql
{
  weatherByPoint(request: { lat: 52.37125, lon: 4.89388 }) {
    forecast {
      days(limit: 2) {
        time
        sunrise
        sunset
        parts {
          morning {
            avgTemperature
          }
          day {
            avgTemperature
          }
          evening {
            avgTemperature
          }
          night {
            avgTemperature
          }
        }
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
      "forecast": {
        "days": [
          {
            "time": "2022-09-06T00:00:00+02:00",
            "sunrise": "06:59",
            "sunset": "20:18",
            "parts": {
              "morning": {
                "avgTemperature": 19
              },
              "day": {
                "avgTemperature": 25
              },
              "evening": {
                "avgTemperature": 22
              },
              "night": {
                "avgTemperature": 19
              }
            }
          },
          {
            "time": "2022-09-07T00:00:00+02:00",
            "sunrise": "07:00",
            "sunset": "20:16",
            "parts": {
              "morning": {
                "avgTemperature": 17
              },
              "day": {
                "avgTemperature": 23
              },
              "evening": {
                "avgTemperature": 20
              },
              "night": {
                "avgTemperature": 18
              }
            }
          }
        ]
      }
    }
  }
}
```

{% endcut %}

### Forecast for multiple points {#forecast_multi_points}

In the Steam API, it is possible to get a forecast for several points at once. To do this, you need to create a [fragment](https://graphql.org/learn/queries/#fragments) with the `forecast` object in which to request the necessary data. The created fragment is specified in the `weatherByPoint` method call for each point.

For example, for the points `London`, `Warsaw` and `Berlin`, you can get an aggregated daily (`day`) and night (`night`) forecast for 3 days ahead for the following parameters:

* `cloudiness` — cloudiness
* `humidity` — relative humidity of the air
* `avgTemperature` — average temperature
* `prec` — amount of precipitation (in millimeters)
* `precType` — precipitation type
* `precStrength` — precipitation intensity
* `windSpeed` — wind speed
* `windDirection` — wind direction

Example:

```graphql
{
  London: weatherByPoint(request: { lat: 51.50730, lon: -0.12769 }) {
    ... WeatherData
  }
  Warsaw: weatherByPoint(request: { lat: 52.23209, lon: 21.00714 }) {
    ... WeatherData
  }
  Berlin: weatherByPoint(request: { lat: 52.51865, lon: 13.37471 }) {
    ... WeatherData
  }
}

fragment WeatherData on Weather {
  forecast {
    days(limit: 3) {
      summary {
        day {
          cloudiness
          humidity
          avgTemperature
          prec
          precType
          precStrength
          windSpeed
          windDirection
        }
        night {
          cloudiness
          humidity
          avgTemperature
          prec
          precType
          precStrength
          windSpeed
          windDirection
        }
      }
    }
  }
}
```

{% cut "Response" %}

```json
{
  "data": {
    "London": {
      "forecast": {
        "days": [
          {
            "summary": {
              "day": {
                "cloudiness": "OVERCAST",
                "humidity": 87,
                "avgTemperature": 16,
                "prec": 40.4,
                "precType": "RAIN",
                "precStrength": "VERY_STRONG",
                "windSpeed": 3.4,
                "windDirection": "WEST"
              },
              "night": {
                "cloudiness": "OVERCAST",
                "humidity": 95,
                "avgTemperature": 14,
                "prec": 0.5,
                "precType": "RAIN",
                "precStrength": "WEAK",
                "windSpeed": 1.7,
                "windDirection": "SOUTH_WEST"
              }
            }
          },
          {
            "summary": {
              "day": {
                "cloudiness": "SIGNIFICANT",
                "humidity": 80,
                "avgTemperature": 17,
                "prec": 0,
                "precType": "NO_TYPE",
                "precStrength": "ZERO",
                "windSpeed": 2.5,
                "windDirection": "NORTH_WEST"
              },
              "night": {
                "cloudiness": "SIGNIFICANT",
                "humidity": 96,
                "avgTemperature": 14,
                "prec": 0,
                "precType": "NO_TYPE",
                "precStrength": "ZERO",
                "windSpeed": 1.7,
                "windDirection": "WEST"
              }
            }
          },
          {
            "summary": {
              "day": {
                "cloudiness": "OVERCAST",
                "humidity": 80,
                "avgTemperature": 18,
                "prec": 0,
                "precType": "NO_TYPE",
                "precStrength": "ZERO",
                "windSpeed": 2,
                "windDirection": "SOUTH"
              },
              "night": {
                "cloudiness": "CLEAR",
                "humidity": 93,
                "avgTemperature": 13,
                "prec": 0,
                "precType": "NO_TYPE",
                "precStrength": "ZERO",
                "windSpeed": 1.2,
                "windDirection": "NORTH_WEST"
              }
            }
          }
        ]
      }
    },
    "Warsaw": {
      "forecast": {
        "days": [
          {
            "summary": {
              "day": {
                "cloudiness": "OVERCAST",
                "humidity": 87,
                "avgTemperature": 14,
                "prec": 0.2,
                "precType": "RAIN",
                "precStrength": "WEAK",
                "windSpeed": 3.3,
                "windDirection": "EAST"
              },
              "night": {
                "cloudiness": "OVERCAST",
                "humidity": 81,
                "avgTemperature": 14,
                "prec": 0.4,
                "precType": "RAIN",
                "precStrength": "WEAK",
                "windSpeed": 4.5,
                "windDirection": "SOUTH_EAST"
              }
            }
          },
          {
            "summary": {
              "day": {
                "cloudiness": "OVERCAST",
                "humidity": 81,
                "avgTemperature": 15,
                "prec": 0.8,
                "precType": "RAIN",
                "precStrength": "WEAK",
                "windSpeed": 2.4,
                "windDirection": "NORTH_EAST"
              },
              "night": {
                "cloudiness": "CLOUDY",
                "humidity": 95,
                "avgTemperature": 12,
                "prec": 0,
                "precType": "NO_TYPE",
                "precStrength": "ZERO",
                "windSpeed": 1.8,
                "windDirection": "EAST"
              }
            }
          },
          {
            "summary": {
              "day": {
                "cloudiness": "OVERCAST",
                "humidity": 87,
                "avgTemperature": 13,
                "prec": 1.6,
                "precType": "RAIN",
                "precStrength": "WEAK",
                "windSpeed": 3,
                "windDirection": "NORTH_WEST"
              },
              "night": {
                "cloudiness": "OVERCAST",
                "humidity": 92,
                "avgTemperature": 13,
                "prec": 0.7,
                "precType": "RAIN",
                "precStrength": "WEAK",
                "windSpeed": 1.6,
                "windDirection": "NORTH_WEST"
              }
            }
          }
        ]
      }
    },
    "Berlin": {
      "forecast": {
        "days": [
          {
            "summary": {
              "day": {
                "cloudiness": "SIGNIFICANT",
                "humidity": 77,
                "avgTemperature": 18,
                "prec": 0.4,
                "precType": "RAIN",
                "precStrength": "WEAK",
                "windSpeed": 2.6,
                "windDirection": "EAST"
              },
              "night": {
                "cloudiness": "CLEAR",
                "humidity": 95,
                "avgTemperature": 14,
                "prec": 0,
                "precType": "NO_TYPE",
                "precStrength": "ZERO",
                "windSpeed": 2.1,
                "windDirection": "SOUTH"
              }
            }
          },
          {
            "summary": {
              "day": {
                "cloudiness": "SIGNIFICANT",
                "humidity": 79,
                "avgTemperature": 17,
                "prec": 0.2,
                "precType": "RAIN",
                "precStrength": "WEAK",
                "windSpeed": 2,
                "windDirection": "SOUTH_WEST"
              },
              "night": {
                "cloudiness": "CLEAR",
                "humidity": 93,
                "avgTemperature": 14,
                "prec": 0,
                "precType": "NO_TYPE",
                "precStrength": "ZERO",
                "windSpeed": 1.7,
                "windDirection": "SOUTH_EAST"
              }
            }
          },
          {
            "summary": {
              "day": {
                "cloudiness": "CLOUDY",
                "humidity": 85,
                "avgTemperature": 17,
                "prec": 0,
                "precType": "NO_TYPE",
                "precStrength": "ZERO",
                "windSpeed": 3.3,
                "windDirection": "NORTH_WEST"
              },
              "night": {
                "cloudiness": "CLOUDY",
                "humidity": 93,
                "avgTemperature": 14,
                "prec": 0,
                "precType": "NO_TYPE",
                "precStrength": "ZERO",
                "windSpeed": 1.3,
                "windDirection": "NORTH_WEST"
              }
            }
          }
        ]
      }
    }
  }
}
```

{% endcut %}
