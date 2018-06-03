---
swagger: "2.0"
info:
  title: Summary API
  description: The Summary API.
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
  ? |2-

        /api/{version}/summary.outage/{checkid}
  : get:
      summary: Get List of Outages
      description: |2-

            Get a list of status changes for a specified check and time period
      operationId: get-list-of-outages
      parameters:
      - in: query
        name: from
        description: Start time of period
        type: <td>integer</td>
      - in: query
        name: order
        description: Sorting order of outages
        type: <td>string (asc,desc)</td>
      - in: query
        name: to
        description: End time of period
        type: <td>integer</td>
      responses:
        200:
          description: OK
      tags:
      - summary
definitions: []
x-collection-name: Pingdom
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