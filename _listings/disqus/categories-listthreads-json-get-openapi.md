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
  /categories/listThreads.json:
    get:
      summary: Categories ListThreads
      description: "\n     Categories ListThreads "
      operationId: categories-listthreads
      x-api-path-slug: categorieslistthreads-json-get
      parameters:
      - in: query
        name: category
        description: Looks up a category by ID
        type: string
      - in: query
        name: cursor
        description: Defaults to null
        type: string
      - in: query
        name: limit
        description: Defaults to 25                         Maximum value of 100
        type: string
      - in: query
        name: order
        description: 'Defaults to desc                         Choices: asc, desc'
        type: string
      - in: query
        name: related
        description: Defaults to []                         You may specify relations
          to include with your response
        type: string
      - in: query
        name: since
        description: Defaults to null                         Unix timestamp (or ISO
          datetime standard)
        type: string
      responses:
        200:
          description: OK
      tags:
      - comments
      - categories
definitions: []
x-collection-name: Disqus
x-streamrank:
  polling_total_time_average: "0.25"
  polling_size_download_average: "3024.78"
  streaming_total_time_average: "0.14"
  streaming_size_download_average: "1512.5"
  change_yes: "7"
  change_no: "1308"
  time_percentage: "46"
  size_percentage: "50"
  change_percentage: "1"
  last_run: "2018-05-12"
  days_run: "8"
  minute_run: "0"
---