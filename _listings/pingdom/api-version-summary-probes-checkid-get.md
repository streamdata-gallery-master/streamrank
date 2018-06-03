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

        /api/{version}/summary.probes/{checkid}
  : get:
      summary: Get Active Probes For A Period
      description: |2-

            Get a list of probes that performed tests for a specified check during a specified period
      operationId: get-active-probes-for-a-period
      parameters:
      - in: query
        name: from
        description: Start time of period
        type: <td>integer</td>
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