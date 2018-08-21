---
swagger: "2.0"
x-collection-name: IEX
x-complete: 0
info:
  title: IEX Trading API Batch Requests
  description: Returns batch stock quotes.
  termsOfService: https://iextrading.com/api-terms/
  version: 1.0.0
host: api.iextrading.com
basePath: /1.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /stock/market/batch:
    get:
      summary: Batch Requests
      description: Returns batch stock quotes.
      operationId: batch-requests
      x-api-path-slug: stockmarketbatch-get
      parameters:
      - ~
      - in: query
        name: range
        description: Optional  Used to specify a chart range if chart is used in types
          parameter
      - in: query
        name: symbols
        description: Optional  Comma delimited list of symbols limited to 100
      - in: query
        name: types
        description: Required  Comma delimited list of endpoints to call
      responses:
        200:
          description: OK
      tags:
      - Market Data
      - Quotes
      - Batch
x-streamrank:
  polling_total_time_average: "0.18"
  polling_size_download_average: "20752.94"
  streaming_total_time_average: "0.1"
  streaming_size_download_average: "10382.16"
  change_yes: "306"
  change_no: "1485"
  time_percentage: "43"
  size_percentage: "50"
  change_percentage: "17"
  last_run: "2018-02-20"
  days_run: "1"
  minute_run: "0"
---