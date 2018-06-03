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
  /receivedShare/:
    get:
      summary: Retrieving Received Share Information
      description: To retrieve information about a received share (that is, a shared
        folder owned by another user and to whichnthis user has been granted access
        privileges by the owner), an application submits an HTTP GET request to the
        URLnthat represents the received share resource
      operationId: retrieving-received-share-information
      responses:
        200:
          description: OK
      tags:
      - receivedshare
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