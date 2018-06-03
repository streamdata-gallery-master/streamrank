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
  /posts/list.json:
    get:
      summary: Posts List
      description: "\n     Posts List "
      operationId: posts-list
      parameters:
      - in: query
        name: category
        description: Defaults to null                         Looks up a category
          by ID
        type: string
      - in: query
        name: cursor
        description: Defaults to null
        type: string
      - in: query
        name: end
        description: Defaults to null                         Unix timestamp (or ISO
          datetime standard)
        type: string
      - in: query
        name: filters
        description: 'Defaults to []                         Valid values are: 1:
          Is_Anonymous 2: Has_Link 3: Has_Low_Rep_Author 4: Has_Bad_Word 5: Is_Flagged
          6: No_Issue 7: Is_Toxic'
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
        name: limit
        description: Defaults to 25                         Maximum value of 100
        type: string
      - in: query
        name: offset
        description: 'Defaults to 0                         Deprecated: Please see
          documentation on cursors'
        type: string
      - in: query
        name: order
        description: 'Defaults to desc                         Choices: asc, desc'
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
        name: since
        description: Defaults to null                         Unix timestamp (or ISO
          datetime standard)
        type: string
      - in: query
        name: sortType
        description: 'Defaults to date                         Choices: date, priority'
        type: string
      - in: query
        name: start
        description: Defaults to null                         Unix timestamp (or ISO
          datetime standard)
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
  polling_total_time_average: "98.25"
  polling_size_download_average: "281.84"
  streaming_total_time_average: "49.25"
  streaming_size_download_average: "141.12"
  change_yes: "289"
  change_no: "912"
  time_percentage: "50"
  size_percentage: "50"
  change_percentage: "24"
  last_run: "2018-05-12"
  days_run: "8"
  minute_run: "0"
---