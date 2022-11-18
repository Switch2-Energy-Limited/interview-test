# Switch2 Tech Interview Test

Create suitable code to deploy in AWS Lambda which consumes a V1.0 [API Gateway Lambda Proxy event](https://docs.amazonaws.cn/en_us/apigateway/latest/developerguide/http-api-develop-integrations-lambda.html).

The API endpoint has a path parameter called `force` and an optional query string parameter called `date`.

Use these parameters to make an API call to the ["Police stop and searches with no location" API](https://data.police.uk/docs/method/stops-no-location/). Example parameters for testing: force: 'metropolitan', date: '2022-08'.

Extract the data from the API call and produce a count for each instance of the `outcome` property.

```json
{
  "Arrest": 5,
  "A no further action disposal": 3
}
```

Return this summary, along with a total count of all instances, back to API Gateway.

```json
{
  "total": 8,
  "breakdown": {
    "Arrest": 5,
    "A no further action disposal": 3
  }
}
```

Write tests, using the Jest framework, to prove:

- The code formats the URL correctly with a date provided
- The code formats the URL correctly with no date provided
- The code returns the correct object for a given data set, use the provided [mock data](./data/mockReturn.json)
