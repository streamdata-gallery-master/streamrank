swagger: "2.0"
x-collection-name: Blockchain
x-complete: 1
info:
  title: Blockchain
  version: 1.0.0
host: blockchain.info
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /latestblock:
    get:
      summary: Latest Block
      description: Gets the latest block.
      operationId: getLatestBlock
      x-api-path-slug: latestblock-get
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
      - Blockchain
      - Latest
  /stats:
    get:
      summary: Stats
      description: This method can be used to get the data behind Blockchain.info's
        stats.
      operationId: getStats
      x-api-path-slug: stats-get
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
      - Blockchain
      - Statistics