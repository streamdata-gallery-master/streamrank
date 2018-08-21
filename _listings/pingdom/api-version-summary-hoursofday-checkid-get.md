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

        /api/{version}/summary.hoursofday/{checkid}
  : get:
      summary: Get Response Time Averages For Each Hour Of The Day
      description: |2-

            Returns the average response time for each hour of the day (0-23) for a specific check over a selected time period
      operationId: get-response-time-averages-for-each-hour-of-the-day
      parameters:
      - in: query
        name: from
        description: Start time of period
        type: <td>integer</td>
      - in: query
        name: probes
        description: Filter to only use results from a list of probes
        type: <td>string</td>
      - in: query
        name: to
        description: End time of period
        type: <td>integer</td>
      - in: query
        name: uselocaltime
        description: If true, use the user's local time zone for results (from and
          to parameters should still be specified in UTC)
        type: <td>boolean</td>
      responses:
        200:
          description: OK
      tags:
      - summary
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