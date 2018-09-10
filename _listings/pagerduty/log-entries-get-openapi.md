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
      x-api-path-slug: log-entries-get
      responses:
        200:
          description: OK
      tags:
      - log entries
definitions: []
x-collection-name: PagerDuty
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