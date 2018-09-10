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
      x-api-path-slug: tagsget-get
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
  polling_total_time_average: "0.58"
  polling_size_download_average: "47830.41"
  streaming_total_time_average: "0.31"
  streaming_size_download_average: "24132.53"
  change_yes: "2"
  change_no: "243"
  time_percentage: "47"
  size_percentage: "50"
  change_percentage: "1"
  last_run: "2018-05-06"
  days_run: "1"
  minute_run: "0"
---