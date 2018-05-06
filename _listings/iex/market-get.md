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
  /market:
    get:
      summary: Market
      description: This endpoint returns near real time traded volume on the markets
      operationId: market
      parameters:
      - in: query
        name: format
        description: ' Parameter is optional Value can only be csv When parameter
          is not present, format defaults to JSON'
      responses:
        200:
          description: OK
      tags:
      - market data
      - markets
definitions: []
x-collection-name: IEX
x-streamrank:
  polling_total_time_average: "0.15"
  polling_size_download_average: "2233"
  streaming_total_time_average: "0.08"
  streaming_size_download_average: "1116.8"
  change_yes: "2"
  change_no: "3747"
  time_percentage: "45"
  size_percentage: "50"
  change_percentage: "0"
  last_run: "2018-02-19"
  days_run: "3"
  minute_run: "0"
---