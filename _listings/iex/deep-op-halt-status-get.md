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
  /deep/op-halt-status:
    get:
      summary: Operational Halt Status
      description: Subscribe to the ophaltstatus channel
      operationId: operational-halt-status
      parameters:
      - in: query
        name: symbols
        description: ' Parameter is required Value needs to be a comma-separated list
          of symbols (i'
      responses:
        200:
          description: OK
      tags:
      - market data
      - halt status
definitions: []
x-collection-name: IEX
x-streamrank:
  polling_total_time_average: "0.15"
  polling_size_download_average: "20.44"
  streaming_total_time_average: "0.09"
  streaming_size_download_average: "10.23"
  change_yes: "5"
  change_no: "1787"
  time_percentage: "42"
  size_percentage: "50"
  change_percentage: "0"
  last_run: "2018-02-20"
  days_run: "4"
  minute_run: "0"
---