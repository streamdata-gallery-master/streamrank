---
swagger: "2.0"
info:
  title: 1Forge
  description: 1Forge provides real-time quote data (bid &amp; ask) for 240+ pairs.
    To see a full list of supported currency pairs, please see the full currency pair
    list. At this time, we do not offer historical data, however, clients are more
    than welcome to archive our quotes locally for internal use.
  version: 1.0.0
host: forex.1forge.com
basePath: 1.0.3/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /symbols:
    get:
      summary: Get Currency Symbols API
      description: Get a list of currency symbols to use when making calls to the
        other APIs
      operationId: getSymbols
      parameters:
      - in: query
        name: api_key
        description: The api key
        type: string
        format: string
      - in: query
        name: format
        description: The format to return
        type: string
        format: string
      responses:
        200:
          description: OK
      tags:
      - symbols
definitions: []
x-collection-name: 1Forge
x-streamrank:
  polling_total_time_average: "0.58"
  polling_size_download_average: "312.37"
  streaming_total_time_average: "0.4"
  streaming_size_download_average: "161.9"
  change_yes: "2"
  change_no: "187"
  time_percentage: "31"
  size_percentage: "48"
  change_percentage: "1"
  last_run: "2018-02-19"
  days_run: "0"
  minute_run: "0"
---