## Getting access {#auth}
To get access to Meteum API, you need to log in to the [Meteum developer portal](https://meteum.ai/b2b/console) using one of your accounts (Google, Slack, or another), or create a new Meteum account.
After logging in to the portal, you need to choose one of the [API access plans](plans.md) that best suits your needs. After choosing a plan and making the payment (if it's a paid plan), you'll find a new key in your account. The key activates a few minutes after it's created.

### Authorizing requests with a key {#auth-key}
You can use the obtained key to access the API. For it to work, you need each API request to pass this key in the form of an HTTP request header. The header is called `X-Meteum-API-Key`.

To check if the key works via the terminal command line, use this example:
```bash
curl 'https://api.meteum.ai/graphql/query' -H 'X-Meteum-API-Key: <Key>' -H 'Content-Type: application/json' --data-binary '{"query":"{\n  weatherByPoint(request: { lat: 52.37125, lon: 4.89388 })\n  {\n    now {\n      temperature\n    }\n  }\n}\n"}' --compressed
```

To learn more about authorization and executing requests in Python, see [Quick start](how_to.md#fast-start).
