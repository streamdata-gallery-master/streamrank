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
  /categories/list.json:
    get:
      summary: Categories List
      description: "\n     Categories List "
      operationId: categories-list
      x-api-path-slug: categorieslist-json-get
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
      - categories
definitions: []
x-collection-name: Disqus
x-streamrank:
  polling_total_time_average: "0.1"
  polling_size_download_average: "89"
  streaming_total_time_average: "0.05"
  streaming_size_download_average: "48.5"
  change_yes: "2"
  change_no: "0"
  time_percentage: "49"
  size_percentage: "46"
  change_percentage: "100"
  last_run: "2018-05-04"
  days_run: "0"
  minute_run: "0"
---