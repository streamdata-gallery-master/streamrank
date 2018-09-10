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
  /posts/listPopular.json:
    get:
      summary: Posts ListPopular
      description: "\n     Posts ListPopular "
      operationId: posts-listpopular
      x-api-path-slug: postslistpopular-json-get
      parameters:
      - in: query
        name: category
        description: Defaults to null
        type: string
      - in: query
        name: forum
        description: Defaults to null                         Defaults to all forums
          you moderate
        type: string
      - in: query
        name: include
        description: 'Defaults to [  approved]                         Choices: unapproved,
          approved, spam, deleted, flagged, highlighted'
        type: string
      - in: query
        name: interval
        description: 'Defaults to 7d                         Choices: 1h, 6h, 12h,
          1d, 3d, 7d, 30d, 60d, 90d'
        type: string
      - in: query
        name: limit
        description: Defaults to 25                         Maximum value of 100
        type: string
      - in: query
        name: offset
        description: Defaults to 0
        type: string
      - in: query
        name: order
        description: 'Defaults to popular                         Choices: popular,
          best'
        type: string
      - in: query
        name: organization
        description: Defaults to null                         Looks up an organization
          by ID
        type: string
      - in: query
        name: query
        description: Defaults to null
        type: string
      - in: query
        name: related
        description: Defaults to []                         You may specify relations
          to include with your response
        type: string
      - in: query
        name: thread
        description: Defaults to null                         Looks up a thread by
          ID
        type: string
      responses:
        200:
          description: OK
      tags:
      - comments
      - posts
definitions: []
x-collection-name: Disqus
x-streamrank:
  polling_total_time_average: "0.36"
  polling_size_download_average: "10894.43"
  streaming_total_time_average: "0.19"
  streaming_size_download_average: "5455.06"
  change_yes: "15"
  change_no: "1189"
  time_percentage: "47"
  size_percentage: "50"
  change_percentage: "1"
  last_run: "2018-05-12"
  days_run: "8"
  minute_run: "0"
---