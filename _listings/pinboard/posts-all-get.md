---
swagger: "2.0"
info:
  title: Pinboard
  description: Store, manage and share bookmarks on Pinboard
  version: 1.0.0
host: api.pinboard.in
basePath: /v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /posts/all:
    get:
      summary: Get All Posts
      description: Returns all bookmarks in the user's account
      operationId: posts.all.get
      parameters:
      - in: query
        name: fromdt
        description: return only bookmarks created after this time
        type: string
        format: string
      - in: query
        name: meta
        description: include a change detection signature for each bookmark
        type: string
        format: string
      - in: query
        name: results
        description: number of results to return
        type: string
        format: string
      - in: query
        name: start
        description: offset value (default is 0)
        type: string
        format: string
      - in: query
        name: tag
        description: filter by up to three tags
        type: string
        format: string
      - in: query
        name: todt
        description: eturn only bookmarks created before this time
        type: string
        format: string
      responses:
        200:
          description: OK
      tags:
      - posts
definitions: []
x-collection-name: Pinboard
x-streamrank:
  polling_total_time_average: "10.57"
  polling_size_download_average: "70441.2"
  streaming_total_time_average: "5.38"
  streaming_size_download_average: "61637.76"
  change_yes: "4"
  change_no: "246"
  time_percentage: "49"
  size_percentage: "12"
  change_percentage: "2"
  last_run: "2018-05-06"
  days_run: "1"
  minute_run: "0"
---