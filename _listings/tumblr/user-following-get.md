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
        description: "The number of results to return: 1\u201320, inclusive"
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