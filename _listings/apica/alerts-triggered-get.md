---
swagger: "2.0"
info:
  title: Alerts API
  description: The Alerts API.
  version: 1.0.0
host: api.serverdensity.io.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /alerts/triggered:
    get:
      summary: Triggered alerts
      description: Get a list of all triggered alerts on your account, per subject
        (device or service) or per alert config
      operationId: triggered-alerts
      parameters:
      - in: query
        name: closed
        description: Whether to filter by closed or open alerts - unset = all alerts,
          false = open alerts, true = closed alerts
        type: string
      - in: query
        name: filter
        description: You can provide a JSON encoded hash filter for the search that
          will return items that match the filter
        type: string
      - in: query
        name: subjectType
        description: The type of the subject - device, service, deviceGroup or serviceGroup
          if you also specify the subjectId as part of the URL (see examples below)
        type: string
      - in: query
        name: token
        description: Your API token
        type: string
      responses:
        200:
          description: OK
      tags:
      - alerts
definitions: []
x-collection-name: Apica
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