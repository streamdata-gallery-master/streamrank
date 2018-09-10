---
swagger: "2.0"
info:
  title: Disqus
  description: Welcome to the Disqus Web API. The API enables developers to communicate
    with Disqus data from within their own applications.
  termsOfService: https://docs.disqus.com/kb/terms-and-policies/
  version: 1.0.0
host: disqus.com
basePath: api/3.0/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /forums/listFollowers.json:
    get:
      summary: Forums ListFollowers
      description: "\n     Forums ListFollowers "
      operationId: forums-listfollowers
      x-api-path-slug: forumslistfollowersjson-get
      parameters:
      - in: query
        name: cursor
        description: Defaults to null
        type: string
      - in: query
        name: forum
        description: Looks up a forum by ID (aka short name)
        type: string
      - in: query
        name: limit
        description: Defaults to 25                         Maximum value of 100
        type: string
      - in: query
        name: order
        description: 'Defaults to asc                         Choices: asc, desc'
        type: string
      - in: query
        name: since_id
        description: Defaults to null
        type: string
      responses:
        200:
          description: OK
      tags:
      - comments
      - lists
definitions: []
x-collection-name: Disqus
x-streamrank:
  polling_total_time_average: "0.42"
  polling_size_download_average: "24669.39"
  streaming_total_time_average: "0.21"
  streaming_size_download_average: "12365.57"
  change_yes: "184"
  change_no: "1029"
  time_percentage: "49"
  size_percentage: "50"
  change_percentage: "15"
  last_run: "2018-05-12"
  days_run: "8"
  minute_run: "0"
---