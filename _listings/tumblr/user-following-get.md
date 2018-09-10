---
swagger: "2.0"
info:
  title: Tumblr
  description: 'ntShare photos, mobile apps, and social network using Tumblr''s API''s.n    '
  version: 1.0.0
host: api.tumblr.com
basePath: /v2/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /user/following:
    get:
      summary: Get User Following
      description: Use this method to retrieve the blogs followed by the user whose
        OAuth credentials are submitted with the request
      operationId: user.following.get
      parameters:
      - in: query
        name: limit
        description: 'The number of results to return: 1???20, inclusive'
      - in: query
        name: offset
        description: Result number to start at
      responses:
        200:
          description: OK
      tags:
      - user
      - following
definitions: []
x-collection-name: Tumblr
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