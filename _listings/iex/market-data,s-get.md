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
  Market Data,s:
    get:
      summary: Chart
      description: The above example will return JSON with the following keys
      operationId: chart
      parameters:
      - in: query
        name: chartInterval
        description: ' Optional number'
      - in: query
        name: chartReset
        description: ' Optional boolean'
      - in: query
        name: chartSimplify
        description: ' Optional boolean'
      - in: path
        name: range
        description: The date range
        type: string
        format: string
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
      - charts
definitions: []
x-collection-name: IEX
x-streamrank:
  polling_total_time_average: "0.17"
  polling_size_download_average: "4682.81"
  streaming_total_time_average: "0.1"
  streaming_size_download_average: "2341.47"
  change_yes: "4"
  change_no: "1782"
  time_percentage: "40"
  size_percentage: "50"
  change_percentage: "0"
  last_run: "2018-02-20"
  days_run: "1"
  minute_run: "0"
---