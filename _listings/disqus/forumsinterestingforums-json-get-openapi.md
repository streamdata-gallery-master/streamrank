---
swagger: "2.0"
x-collection-name: Disqus
x-complete: 0
info:
  title: Disqus Forums InterestingForums
  description: Forums InterestingForums
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
      description: Categories List
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
      - Comments
      - Categories
  /forums/interestingForums.json:
    get:
      summary: Forums InterestingForums
      description: Forums InterestingForums
      operationId: forums-interestingforums
      x-api-path-slug: forumsinterestingforums-json-get
      parameters:
      - in: query
        name: limit
        description: Defaults to 5                         Maximum value of 100
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Forums
x-streamrank:
  polling_total_time_average: "0.18"
  polling_size_download_average: "11963.57"
  streaming_total_time_average: "0.09"
  streaming_size_download_average: "5995.39"
  change_yes: "1279"
  change_no: "53"
  time_percentage: "49"
  size_percentage: "50"
  change_percentage: "96"
  last_run: "2018-05-12"
  days_run: "8"
  minute_run: "0"
---