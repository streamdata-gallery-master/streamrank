---
swagger: "2.0"
info:
  title: IEX
  description: The IEX API is a set of services designed for developers and engineers.
    It can be used to build high-quality apps and services. We&rsquo;re always working
    to improve the IEX API. Please check back for enhancements and improvements.
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
  /stock/{symbol}/quote:
    get:
      summary: Quote
      description: Pulls a stock quote using any ticker symbol
      operationId: quote
      parameters:
      - in: query
        name: displayPercent
        description: ' Optional If set to true, all percentage values will be multiplied
          by a factor of 100 (Ex: /stock/aapl/quote?displayPercent=true)'
      - in: path
        name: symbol
        description: Stock ticker symbol
        type: string
        format: string
      responses:
        200:
          description: OK
      tags:
      - market data
      - quotes
definitions: []
x-collection-name: IEX
x-streamrank:
  polling_total_time_average: "0.27"
  polling_size_download_average: "807.69"
  streaming_total_time_average: "0.16"
  streaming_size_download_average: "404.47"
  change_yes: "538"
  change_no: "731"
  time_percentage: "38"
  size_percentage: "50"
  change_percentage: "42"
  last_run: "2018-02-15"
  days_run: "1"
  minute_run: "0"
---