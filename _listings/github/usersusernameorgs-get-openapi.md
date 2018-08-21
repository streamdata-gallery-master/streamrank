---
swagger: "2.0"
x-collection-name: GitHub
x-complete: 0
info:
  title: Github Get Users Username Orgs
  description: List all public organizations for a user.
  termsOfService: https://help.github.com/articles/github-terms-of-service/#b-api-terms
  version: 1.0.0
host: api.github.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /users/{username}/orgs:
    get:
      summary: Get Users Username Orgs
      description: List all public organizations for a user.
      operationId: list-all-public-organizations-for-a-user
      x-api-path-slug: usersusernameorgs-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: username
        description: Name of user
      responses:
        200:
          description: OK
      tags:
      - Users
      - Username
      - Orgs
x-streamrank:
  polling_total_time_average: "0.13"
  polling_size_download_average: "415"
  streaming_total_time_average: "0.07"
  streaming_size_download_average: "225.33"
  change_yes: "2"
  change_no: "1"
  time_percentage: "44"
  size_percentage: "46"
  change_percentage: "67"
  last_run: "2018-05-04"
  days_run: "0"
  minute_run: "0"
---