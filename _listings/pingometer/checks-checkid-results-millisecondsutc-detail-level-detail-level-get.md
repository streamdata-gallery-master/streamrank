---
swagger: "2.0"
info:
  title: Checks API
  description: The Checks API.
  version: 1.0.0
host: api.pingdom.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  '/checks/{checkId}/results/{millisecondsUtc}?detail_level={detail_level} ':
    get:
      summary: Checks {checkId} Results {millisecondsUtc}?detail_level={detail_level}
      description: Gets a specific check result by a numeric java timestamp
      operationId: getChecksCheckResultsMillisecondsutcDetailLevelDetailLevel
      responses:
        200:
          description: OK
      tags:
      - checks
definitions: []
x-collection-name: Pingometer
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