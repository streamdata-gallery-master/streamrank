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
  /push/stats:
    get:
      summary: Get Push Stats
      description: Returns hourly message counts for your application
      operationId: push.stats.get
      x-api-path-slug: pushstats-get
      parameters:
      - in: query
        name: end
        description: End date in UTC format
      - in: query
        name: format
        description: Response format
      - in: query
        name: start
        description: Start date in UTC format
      responses:
        200:
          description: OK
      tags:
      - push
      - stats
definitions: []
x-collection-name: Urban Airship
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