---
swagger: "2.0"
info:
  title: Pinboard
  description: Store, manage and share bookmarks on Pinboard
  version: 1.0.0
host: api.pinboard.in
basePath: /v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /tags/get:
    get:
      summary: Get Tags
      description: Returns a full list of the user's tags along with the number of
        times they were used
      operationId: tags.get.get
      parameters:
      - in: query
        name: format
        description: the format to return
        type: string
        format: string
      responses:
        200:
          description: OK
      tags:
      - tags
definitions: []
x-collection-name: Pinboard
x-streamrank:
  polling_total_time_average: ~
  polling_size_download_average: ~
  streaming_total_time_average: ~
  streaming_size_download_average: ~
  change_yes: ~
  change_no: ~
  time_percentage: ~
  size_percentage: ~
  change_percentage: ~
  last_run: ~
  days_run: ~
  minute_run: ~
---