---
swagger: "2.0"
x-collection-name: IEX
x-complete: 0
info:
  title: IEX Trading API Quote
  description: Pulls a stock quote using any ticker symbol.
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
  /stock/{symbol}/delayed-quote:
    get:
      summary: Delayed Quote
      description: This returns the 15 minute delayed market quote.
      operationId: delayed-quote
      x-api-path-slug: stocksymboldelayedquote-get
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
      - Market Data
      - Quotes
  /stock/{symbol}/quote:
    get:
      summary: Quote
      description: Pulls a stock quote using any ticker symbol.
      operationId: quote
      x-api-path-slug: stocksymbolquote-get
      parameters:
      - in: query
        name: displayPercent
        description: 'Optional If set to true, all percentage values will be multiplied
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
      - Market Data
      - Quotes
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