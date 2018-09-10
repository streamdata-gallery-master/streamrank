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
  /user/dashboard:
    get:
      summary: Get User Dashboard
      description: Use this method to retrieve the dashboard that matches the OAuth
        credentials submitted with the request
      operationId: user.dashboard.get
      parameters:
      - in: query
        name: limit
        description: 'The number of results to return: 1???20, inclusive'
      - in: query
        name: offset
        description: Post number to start at
      - in: query
        name: since_id
        description: Return posts that have appeared after this ID
      - in: query
        name: type
        description: The type of post to return
      responses:
        200:
          description: OK
      tags:
      - user
      - dashboard
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