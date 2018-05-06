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
  /stats/recent:
    get:
      summary: Recent
      description: This call will return a minimum of the last five trading days up
        to all trading days of the current month
      operationId: recent
      responses:
        200:
          description: OK
      tags:
      - market data
      - statistics
definitions: []
x-collection-name: IEX
x-streamrank:
  polling_total_time_average: "0.16"
  polling_size_download_average: "1555.36"
  streaming_total_time_average: "0.09"
  streaming_size_download_average: "781.12"
  change_yes: "50"
  change_no: "1743"
  time_percentage: "42"
  size_percentage: "50"
  change_percentage: "3"
  last_run: "2018-02-20"
  days_run: "4"
  minute_run: "0"
---