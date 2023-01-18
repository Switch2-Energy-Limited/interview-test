# Switch2 Tech Interview Test

Create an API to extract data from the [UK Police Crime Data](https://data.police.uk/docs/) to show a stop & search outcome summary for a force on a given date.

Stop and search data by date can be accessed from the data API endpoint: ["Police stop and searches with no location"](https://data.police.uk/docs/method/stops-no-location/). Example parameters for testing: force: 'metropolitan', date: '2022-08'.

## Requirements:
 - Provide a GET endpoint which takes force and date parameters `~/stop-and-search/outcome?date=<YYYY-MM>&force=<force_name>`.
 - Validate all API requests.
 - For each request return a JSON body with the following data:

    From the data API call and produce a count for each instance of the `outcome` property.

    ```json
    {
      "Arrest": 5,
      "A no further action disposal": 3
    }
    ```

    Return the above summary, along with a total count of all instances in the response. Complete response body example:

    ```json
    {
      "total": 8,
      "breakdown": {
        "Arrest": 5,
        "A no further action disposal": 3
      }
    }
    ```
 - Handle any rate limits applied to the data API requests: [API call limits](https://data.police.uk/docs/api-call-limits/)
 - Add unit tests to cover any code written.

## Solution

The above task can use any Javascript libraries that may help with the solution. The completed solution should be able to run locally on NodeJS (v16+) `http://localhost:8080/`

## Submission
 - Do not fork this repo.
 - Please do not commit your solution to a public repo.
 - Provide a zip file of your solution with instructions on how to run prior to the interview.
