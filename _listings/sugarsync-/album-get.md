---
swagger: "2.0"
info:
  title: Sugar Sync  API
  description: 'The SugarSync service presents a set of resources that your application
    can access through the Platform API. '
  version: "1"
host: api.sugarsync.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /album/:
    get:
      summary: Retrieving Album Information
      description: To retrieve information about an album, an application submits
        an HTTP GET request to then          album resource that represents the album
      operationId: retrieving-album-information
      parameters:
      - in: query
        name: max
        description: Positive integer
      - in: query
        name: order
        description: name, last_modified, size, or extension
      - in: query
        name: start
        description: 0 or positive integer
      responses:
        200:
          description: OK
      tags:
      - album
definitions: []
x-collection-name: SugarSync
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