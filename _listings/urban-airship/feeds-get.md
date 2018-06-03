---
swagger: "2.0"
info:
  title: Urban Airship
  description: The Urban Airship's API powers mobile applications with push, rich
    push, in-app purchases and subscription services.
  version: v3
host: go.urbanairship.com
basePath: /api/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /feeds:
    get:
      summary: Get Feeds
      description: Gets a list of feeds
      operationId: feeds.get
      parameters:
      - in: query
        name: Content-Type
        description: Content type
      responses:
        200:
          description: OK
      tags:
      - feeds
definitions: []
x-collection-name: Urban Airship
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