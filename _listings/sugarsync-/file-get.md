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
  /file:
    get:
      summary: Retrieving File Data
      description: To retrieve file data, an application submits an HTTP GET request
        to then          file data resource that represents the data for the file
      operationId: retrieving-file-data
      responses:
        200:
          description: OK
      tags:
      - file
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