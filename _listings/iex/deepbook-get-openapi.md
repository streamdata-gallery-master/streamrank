---
swagger: "2.0"
x-collection-name: IEX
x-complete: 0
info:
  title: IEX Trading API Book
  description: Subscribe to the book channel.
  termsOfService: https://iextrading.com/api-terms/
  version: 1.0.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
host: api.iextrading.com
basePath: /1.0
paths:
  /deep/book:
    get:
      summary: Book
      description: Subscribe to the book channel.
      operationId: book
      x-api-path-slug: deepbook-get
      parameters:
      - in: query
        name: symbols
        description: Parameter is required Value needs to be a comma-separated list
          of symbols (i
      responses:
        200:
          description: OK
      tags:
      - Market Data
      - Book
x-streamrank:
  polling_total_time_average: "0.16"
  polling_size_download_average: "115.4"
  streaming_total_time_average: "0.1"
  streaming_size_download_average: "58.14"
  change_yes: "247"
  change_no: "1546"
  time_percentage: "41"
  size_percentage: "50"
  change_percentage: "14"
  last_run: "2018-02-20"
  days_run: "4"
  minute_run: "0"
---