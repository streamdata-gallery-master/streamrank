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
  /blocks/{pool_name}:
    get:
      summary: Blocks by Pool
      description: Returns the blocks for one pool
      operationId: getPoolBlocks
      parameters:
      - in: query
        name: format
        description: The format to return (json,html)
        type: string
        format: string
      - in: path
        name: pool_name
        description: The pool name
        type: string
        format: string
      responses:
        200:
          description: OK
      tags:
      - blockchain
      - pools
definitions: []
x-collection-name: Blockchain Info
x-streamrank:
  polling_total_time_average: "0.24"
  polling_size_download_average: "6836.34"
  streaming_total_time_average: "0.16"
  streaming_size_download_average: "3433.94"
  change_yes: "80"
  change_no: "1399"
  time_percentage: "34"
  size_percentage: "50"
  change_percentage: "5"
  last_run: "2018-02-21"
  days_run: "1"
  minute_run: "0"
---