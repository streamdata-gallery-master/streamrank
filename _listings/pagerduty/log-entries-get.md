---
swagger: "2.0"
info:
  title: PagerDuty
  version: 1.0.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /log_entries:
    get:
      summary: List log entries
      description: List all of the incident log entries across the entire account
      operationId: list-all-of-the-incident-log-entries-across-the-entire-account
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - log entries
definitions: []
x-collection-name: PagerDuty
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