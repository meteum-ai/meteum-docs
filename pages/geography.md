## Geography {#geo}

Meteum API provides weather data for anywhere in the world. To access data at a particular location, you need to pass the coordinates of that location (its latitude and longitude) to the GraphQL method `weatherByPoint` as the `request` parameter.

```graphql
weatherByPoint(request: { lat: 52.37125, lon: 4.89388 }) {
    # ...
}
```
As you can see in the example above, the coordinates are passed as a pair of named values – lat (latitude) and lon (longitude). Latitude values can vary from –90.0 to 90.0, and longitude values from –180 to 180. If the coordinate values are outside of these intervals, the API returns a geolocation error.
