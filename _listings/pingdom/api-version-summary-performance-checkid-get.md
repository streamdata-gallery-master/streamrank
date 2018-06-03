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

        /api/{version}/summary.performance/{checkid}
  : get:
      summary: Get Intervals of Average Response Time and Uptime During a Given Interval
      description: |2-

            For a given interval in time, return a list of sub intervals with the given resolution
      operationId: get-intervals-of-average-response-time-and-uptime-during-a-given-interval
      parameters:
      - in: query
        name: from
        description: Start time of period
        type: <td>integer</td>
      - in: query
        name: includeuptime
        description: Include uptime information
        type: <td>boolean</td>
      - in: query
        name: order
        description: Sorting order of sub intervals
        type: <td>string (asc,desc)</td>
      - in: query
        name: probes
        description: Filter to only use results from a list of probes
        type: <td>string</td>
      - in: query
        name: resolution
        description: Interval size
        type: <td>string (hour, day, week)</td>
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