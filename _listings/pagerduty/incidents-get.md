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
  /incidents:
    get:
      summary: List incidents
      description: List existing incidents
      operationId: list-existing-incidents
      parameters:
      - in: query
        name: include[]
        description: Array of additional details to include
      - in: query
        name: sort_by
        description: Used to specify both the field you wish to sort the results on
          (incident_number/created_on/resolved_on/urgency), as well as the direction
          (asc/desc) of the results
      - in: query
        name: statuses[]
        description: Return only incidents with the given statuses
      responses:
        200:
          description: OK
      tags:
      - incidents
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