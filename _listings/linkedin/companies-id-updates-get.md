---
swagger: "2.0"
info:
  title: LinkedIn
  description: Bring user profiles and professional networks to your apps.
  version: 1.0.0
host: api.linkedin.com
basePath: /v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /companies/{id}/updates:
    get:
      summary: Get Companies Updates
      description: Get companies  updates
      operationId: getCompaniesUpdates
      parameters:
      - in: query
        name: format
        description: The message format
        type: string
        format: string
      responses:
        200:
          description: OK
      tags:
      - companies
      - ""
      - updates
definitions: []
x-collection-name: LinkedIn
x-streamrank:
  polling_total_time_average: ~
  polling_size_download_average: ~
  streaming_total_time_average: ~
  streaming_size_download_average: ~
  change_yes: ~
  change_no: ~
  time_percentage: ~
  size_percentage: ~
  change_percentage: "200"
  last_run: ~
  days_run: ~
  minute_run: ~
---