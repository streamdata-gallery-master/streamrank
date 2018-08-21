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
  /press_releases:
    get:
      summary: Press Releases
      description: Returns the most recent press releases by Nasdaq GlobeNewsire for
        a company
      operationId: press-releases
      parameters:
      - in: query
        name: identifier
        description: ' the stock market ticker symbol associated with the company&rsquo;s
          common stock'
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
        name: related
        description: ' filter whether the list returned includes all press releases
          where a company is the subject or only press releases issued by the company:
          all | false | true'
        type: string
      responses:
        200:
          description: OK
      tags:
      - market data
      - press releases
definitions: []
x-collection-name: Intrinio
x-streamrank:
  polling_total_time_average: "0.16"
  polling_size_download_average: "30806.53"
  streaming_total_time_average: "0.1"
  streaming_size_download_average: "15431.26"
  change_yes: "52"
  change_no: "3691"
  time_percentage: "39"
  size_percentage: "50"
  change_percentage: "1"
  last_run: "2018-02-19"
  days_run: "3"
  minute_run: "0"
---