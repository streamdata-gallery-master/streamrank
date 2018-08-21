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
  /convert:
    get:
      summary: Currency Conversion API
      description: Converts between to types of currency and returns the current results
      operationId: convertCurrency
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
      - in: query
        name: from
        description: Currency to convert from
        type: string
        format: string
      - in: query
        name: quantity
        description: The amount to convert
        type: string
        format: string
      - in: query
        name: to
        description: Currency to convert to
        type: string
        format: string
      responses:
        200:
          description: OK
      tags:
      - currency
      - conversion
definitions: []
x-collection-name: 1Forge
x-streamrank:
  polling_total_time_average: "0.59"
  polling_size_download_average: "150.66"
  streaming_total_time_average: "0.42"
  streaming_size_download_average: "75.35"
  change_yes: "32"
  change_no: "1641"
  time_percentage: "29"
  size_percentage: "50"
  change_percentage: "2"
  last_run: "2018-02-20"
  days_run: "1"
  minute_run: "0"
---