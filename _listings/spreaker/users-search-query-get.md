---
swagger: "2.0"
info:
  title: Spreaker API
  version: v1
host: api.spreaker.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /users/search/{query}:
    get:
      summary: Search Users
      description: This API allows to find users
      operationId: getUsersSearchQuery
      parameters:
      - in: path
        name: query
        description: Search query
      responses:
        200:
          description: OK
      tags:
      - search
      - users
definitions: []
x-collection-name: Spreaker
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