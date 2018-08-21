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
  /stock/{symbol}/delayed-quote:
    get:
      summary: Delayed Quote
      description: This returns the 15 minute delayed market quote
      operationId: delayed-quote
      parameters:
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
  polling_total_time_average: "0.16"
  polling_size_download_average: "146.35"
  streaming_total_time_average: "0.1"
  streaming_size_download_average: "73.18"
  change_yes: "246"
  change_no: "1540"
  time_percentage: "41"
  size_percentage: "50"
  change_percentage: "14"
  last_run: "2018-02-20"
  days_run: "1"
  minute_run: "0"
---