# Meteum API

## General information {#definitions}

- Meteum API is an HTTP interface that provides access to weather data.
- Meteum API returns request results in JSON format.
- You need to be [authorized](pages/auth.md) to receive data. You can access the API by passing a [key](pages/auth.md#auth-key) in the header of the HTTP request
- The main scenario for using the API is getting current weather information or a forecast for a specific [geographical location](pages/geography.md). To get weather data for a particular location, you need to pass its coordinates (its latitude and longitude) in the API request.
- Meteum API can provide quite a lot of information about the weather conditions at a particular location. Use the request parameters to explicitly specify what information you're looking for.
- The [GraphQL](https://graphql.org/) query language is used to set request parameters.
- The GraphQL schema also defines the response format. You can learn more about the schema and try making requests on the [Meteum API](https://meteum.ai/b2b/api#graphql) page.

### What's next {#what-next}
[How to get started](pages/how_to.md)
