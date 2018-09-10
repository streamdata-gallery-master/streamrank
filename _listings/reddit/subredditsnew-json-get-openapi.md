---
swagger: "2.0"
x-collection-name: Reddit
x-complete: 0
info:
  title: Reddit Get New Subreddits
  description: Returns new subreddits.
  version: 1.0.0
host: www.reddit.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /subreddits/new.json:
    get:
      summary: Get New Subreddits
      description: Returns new subreddits.
      operationId: getNewSubreddit
      x-api-path-slug: subredditsnew-json-get
      parameters:
      - in: query
        name: query
        description: a string no longer than 50 characters
        type: string
      responses:
        200:
          description: OK
      tags:
      - Subreddits
      - New
x-streamrank:
  polling_total_time_average: "0.71"
  polling_size_download_average: "76327.46"
  streaming_total_time_average: "0.43"
  streaming_size_download_average: "38331.07"
  change_yes: "174"
  change_no: "28"
  time_percentage: "39"
  size_percentage: "50"
  change_percentage: "86"
  last_run: "2018-05-06"
  days_run: "1"
  minute_run: "0"
---