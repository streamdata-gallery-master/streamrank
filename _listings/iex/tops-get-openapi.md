---
swagger: "2.0"
x-collection-name: IEX
x-complete: 0
info:
  title: IEX Trading API TOPS
  description: Our eligible symbol reference is updated daily. Use these symbols as
    values in your symbols parameter.
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
  /tops:
    get:
      summary: TOPS
      description: Our eligible symbol reference is updated daily. Use these symbols
        as values in your symbols parameter.
      operationId: tops
      x-api-path-slug: tops-get
      parameters:
      - in: query
        name: format
        description: Parameter is optional Value can only be csv When parameter is
          not present, format defaults to JSON
      - in: query
        name: symbols
        description: Parameter is optional Value needs to be a comma-separated list
          of symbols (i
      responses:
        200:
          description: OK
      tags:
      - Market Data
      - Tops
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