---
swagger: "2.0"
info:
  title: Intrinio
  description: Through our Intrinio Data Marketplace, we offer a wide selection of
    financial data feeds sourced by our own proprietary processes as well as from
    many data vendors. The primary application of the Intrinio API is for use in third-party
    applications and integrations or for end-users utilizing the Excel add-in and
    Google Sheets add-on. The Intrinio API uses HTTPS verbs and a RESTful endpoint
    structure, which makes it easy to request data from Intrinio. Basic Authentication
    is administered over HTTPS. Responses are delivered in JSON format.
  version: 1.0.0
host: api.intrinio.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /securities:
    get:
      summary: Securities
      description: Returns security list and information for all securities covered
        by Intrinio
      operationId: securities
      parameters:
      - in: query
        name: exch_symbol
        description: ' the Intrinio Stock Market Symbol, to specify the exchange for
          the list of securities: '
        type: string
      - in: query
        name: identifier
        description: ' the identifier for the legal entity or a security associated
          with the company: '
        type: string
      - in: query
        name: last_crsp_adj_date
        description: ' a date value that returns the list of securities that have
          had adjusted stock prices due to a corporate event after this date: YYYY'
        type: string
      - in: query
        name: page_number
        description: ' an integer greater than or equal to 1 for specifying the page
          number for the return values'
        type: string
      - in: query
        name: page_size
        description: ' an integer greater than 1 for specifying the number of results
          on each page'
        type: string
      - in: query
        name: query
        description: ' a string query search of security name or ticker symbol with
          the returned results being the relevant securities in compacted list format'
        type: string
      responses:
        200:
          description: OK
      tags:
      - market data
      - securities
definitions: []
x-collection-name: Intrinio
x-streamrank:
  polling_total_time_average: "0.94"
  polling_size_download_average: "29095.58"
  streaming_total_time_average: "0.5"
  streaming_size_download_average: "14559.58"
  change_yes: "19"
  change_no: "3726"
  time_percentage: "47"
  size_percentage: "50"
  change_percentage: "1"
  last_run: "2018-02-19"
  days_run: "3"
  minute_run: "0"
---