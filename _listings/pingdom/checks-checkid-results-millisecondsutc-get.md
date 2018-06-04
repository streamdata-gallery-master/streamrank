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
  /checks/{checkId}/results/{millisecondsUtc}:
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
x-collection-name: Pingdom
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