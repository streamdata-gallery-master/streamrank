---
swagger: "2.0"
info:
  title: EBay Finding API
  description: Search eBay; build search and browse experiences.
  version: 1.0.0
host: svcs.ebay.com
basePath: /services/search/FindingService/v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  ?OPERATION-NAME=findItemsByKeywords:
    get:
      summary: Find Item By Keywords
      description: This call searches for items on eBay by a keyword query (keywords)
      operationId: findItemsByKeywords
      x-api-path-slug: operationnamefinditemsbykeywords-get
      parameters:
      - in: query
        name: keywords
        description: The key word or phrase to search by
        type: string
        format: string
      - in: query
        name: RESPONSE-DATA-FORMAT
        description: Response in either XML or JSON
        type: string
        format: string
      - in: query
        name: SERVICE-VERSION
        description: The service version
        type: string
        format: string
      responses:
        200:
          description: OK
      tags:
      - search
      - products
      - auction
      - commerce
definitions: []
x-collection-name: eBay
x-streamrank:
  polling_total_time_average: "0"
  polling_size_download_average: "0"
  streaming_total_time_average: "0"
  streaming_size_download_average: "0"
  change_yes: "0"
  change_no: "0"
  time_percentage: "0"
  size_percentage: "0"
  change_percentage: "200"
  last_run: ~
  days_run: "0"
  minute_run: "0"
---