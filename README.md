# Switch2 Tech Interview Test

Create an API to extract data from the [UK Police Crime Data](https://data.police.uk/docs/) to show a stop & search outcome summary for a force on a given date.

Stop and search data by date can be accessed from the data API endpoint: ["Police stop and searches with no location"](https://data.police.uk/docs/method/stops-no-location/). Example parameters for testing: force: 'metropolitan', date: '2022-08'.

## Requirements:
 - Provide a GET endpoint which takes force and date parameters `~/stop-and-search/outcome?date=<YYYY-MM>&force=<force_name>`.
 - Validate all API requests.
 - For each request return a JSON body with the following data:

    From the data API call and produce a count for each instance of the `outcome` property, an example with only 2 outcomes is below:

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

Use any langauge and libraries you wish to to complete the solution. The completed solution should run on `http://localhost:8080/` or alternatively in the cloud.

## Submission
 - Please do not fork this repo.
 - Bring your code solution to the interview. We will use it as a basis for discussion around how you think about software.
