---
swagger: "2.0"
x-collection-name: GitHub
x-complete: 0
info:
  title: Github Get Orgs Org Events
  description: List public events for an organization.
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
  /orgs/{org}/events:
    get:
      summary: Get Orgs Org Events
      description: List public events for an organization.
      operationId: list-public-events-for-an-organization
      x-api-path-slug: orgsorgevents-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: org
        description: Name of organisation
      responses:
        200:
          description: OK
      tags:
      - Orgs
      - Org
      - Events
x-streamrank:
  polling_total_time_average: "0.2"
  polling_size_download_average: "34762.27"
  streaming_total_time_average: "0.11"
  streaming_size_download_average: "17390.83"
  change_yes: "1027"
  change_no: "1313"
  time_percentage: "44"
  size_percentage: "50"
  change_percentage: "44"
  last_run: "2018-05-12"
  days_run: "8"
  minute_run: "0"
---