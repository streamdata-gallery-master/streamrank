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