---
swagger: "2.0"
x-collection-name: Pinboard
x-complete: 0
info:
  title: Pinboard Get Popular Tags
  description: Returns a list of popular tags and recommended tags for a given URL.
    Popular tags are tags used site-wide for the url; recommended tags are drawn from
    the user's own tags.
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
  /posts/suggest:
    get:
      summary: Get Popular Tags
      description: Returns a list of popular tags and recommended tags for a given
        URL. Popular tags are tags used site-wide for the url; recommended tags are
        drawn from the user's own tags.
      operationId: posts.suggest.get
      x-api-path-slug: postssuggest-get
      parameters:
      - in: query
        name: format
        description: the format to return
        type: string
        format: string
      - in: query
        name: url
        description: url to suggest from
        type: string
        format: string
      responses:
        200:
          description: OK
      tags:
      - Posts
      - Suggest
x-streamrank:
  polling_total_time_average: "0.42"
  polling_size_download_average: "248.8"
  streaming_total_time_average: "0.27"
  streaming_size_download_average: "143.6"
  change_yes: "4"
  change_no: "1"
  time_percentage: "35"
  size_percentage: "42"
  change_percentage: "80"
  last_run: "2018-05-05"
  days_run: "0"
  minute_run: "0"
---