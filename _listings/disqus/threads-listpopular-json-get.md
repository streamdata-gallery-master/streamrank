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
  /threads/listPopular.json:
    get:
      summary: Threads ListPopular
      description: "\n     Threads ListPopular "
      operationId: threads-listpopular
      parameters:
      - in: query
        name: category
        description: Defaults to null                         Looks up a category
          by ID
        type: string
      - in: query
        name: forum
        description: Defaults to null                         Looks up a forum by
          ID (aka short name)
        type: string
      - in: query
        name: interval
        description: 'Defaults to 7d                         Choices: 1h, 6h, 12h,
          1d, 3d, 7d, 30d, 90d'
        type: string
      - in: query
        name: limit
        description: Defaults to 25                         Maximum value of 100
        type: string
      - in: query
        name: related
        description: Defaults to []                         You may specify relations
          to include with your response
        type: string
      - in: query
        name: with_top_post
        description: Defaults to false
        type: string
      responses:
        200:
          description: OK
      tags:
      - comments
      - threads
definitions: []
x-collection-name: Disqus
x-streamrank:
  polling_total_time_average: "0.29"
  polling_size_download_average: "23866.81"
  streaming_total_time_average: "0.15"
  streaming_size_download_average: "11983.84"
  change_yes: "34"
  change_no: "225"
  time_percentage: "48"
  size_percentage: "50"
  change_percentage: "13"
  last_run: "2018-05-06"
  days_run: "2"
  minute_run: "0"
---