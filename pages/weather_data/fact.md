## Actual weather and current weather data {#factual}

One of the most popular uses of weather data is getting information about the current weather at a specific location.

To request information about the **current** weather at a certain point, you need to include the `now` object in the request and list the fields you want to get in the response:

```graphql
{
  weatherByPoint(request: {lat: 52.37125, lon: 4.89388}) {
    now {
      temperature
      humidity
    }
  }
}
```

Meteum can provide data on:

 - Temperature – `temperature`
 - Air humidity – `humidity`
 - Atmospheric pressure – `pressure`
 - Precipitation type and intensity – `precType`, `precStrength`
 - Wind speed and direction – `windSpeed`, `windDirection`
 - Cloudiness – `cloudiness`
 - Other weather parameters

You can check a detailed list of available fields and their arguments at [https://meteum.ai/b2b/api#graphql](https://meteum.ai/b2b/api#graphql).
