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
  /posts/recent:
    get:
      summary: Get Recent Posts
      description: Returns a list of the user's most recent posts, filtered by tag
      operationId: posts.recent.get
      x-api-path-slug: postsrecent-get
      parameters:
      - in: query
        name: count
        description: number of results to return
        type: string
        format: string
      - in: query
        name: tag
        description: filter by up to three tags
        type: string
        format: string
      responses:
        200:
          description: OK
      tags:
      - posts
      - recent
definitions: []
x-collection-name: Pinboard
x-streamrank:
  polling_total_time_average: "0.42"
  polling_size_download_average: "5038.91"
  streaming_total_time_average: "0.22"
  streaming_size_download_average: "2529.82"
  change_yes: "2"
  change_no: "243"
  time_percentage: "48"
  size_percentage: "50"
  change_percentage: "1"
  last_run: "2018-05-06"
  days_run: "1"
  minute_run: "0"
---