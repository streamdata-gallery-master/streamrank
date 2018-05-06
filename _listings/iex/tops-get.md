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
  /tops:
    get:
      summary: TOPS
      description: Our eligible symbol reference is updated daily
      operationId: tops
      parameters:
      - in: query
        name: format
        description: ' Parameter is optional Value can only be csv When parameter
          is not present, format defaults to JSON'
      - in: query
        name: symbols
        description: ' Parameter is optional Value needs to be a comma-separated list
          of symbols (i'
      responses:
        200:
          description: OK
      tags:
      - market data
      - tops
definitions: []
x-collection-name: IEX
x-streamrank:
  polling_total_time_average: "0.16"
  polling_size_download_average: "4675.48"
  streaming_total_time_average: "0.09"
  streaming_size_download_average: "2337.81"
  change_yes: "200"
  change_no: "1590"
  time_percentage: "42"
  size_percentage: "50"
  change_percentage: "11"
  last_run: "2018-02-20"
  days_run: "4"
  minute_run: "0"
---