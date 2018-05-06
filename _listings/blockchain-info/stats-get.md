---
swagger: "2.0"
info:
  title: Blockchain Info
  description: Use Blockchain's APIs at no cost to help you start building bitcoin
    apps.
  version: 1.0.0
host: blockchain.info
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /stats:
    get:
      summary: Stats
      description: This method can be used to get the data behind Blockchain
      operationId: getStats
      parameters:
      - in: query
        name: format
        description: The format to return (json,html)
        type: string
        format: string
      responses:
        200:
          description: OK
      tags:
      - blockchain
      - statistics
definitions: []
x-collection-name: Blockchain Info
x-streamrank:
  polling_total_time_average: "0.17"
  polling_size_download_average: "705.04"
  streaming_total_time_average: "0.11"
  streaming_size_download_average: "359.88"
  change_yes: "158"
  change_no: "1315"
  time_percentage: "38"
  size_percentage: "49"
  change_percentage: "11"
  last_run: "2018-02-21"
  days_run: "1"
  minute_run: "0"
---