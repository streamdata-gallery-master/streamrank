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
  /partner/apps:
    get:
      summary: Get Partner Apps
      description: List applications
      operationId: partner.apps.get
      parameters:
      - in: query
        name: device_token
        description: A specific device token
      - in: query
        name: tag
        description: Tags can be of any format you wish, but we recommend that they
          be URL-safe in order to make less work for you
      responses:
        200:
          description: OK
      tags:
      - partner
      - apps
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