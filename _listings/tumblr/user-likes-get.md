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
  /user/likes:
    get:
      summary: Get User Likes
      description: Use this method to retrieve the liked posts that match the OAuth
        credentials submitted with the request
      operationId: user.likes.get
      parameters:
      - in: query
        name: limit
        description: "The number of results to return: 1\u201320, inclusive"
      - in: query
        name: offset
        description: Liked post number to start at
      responses:
        200:
          description: OK
      tags:
      - user
      - likes
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