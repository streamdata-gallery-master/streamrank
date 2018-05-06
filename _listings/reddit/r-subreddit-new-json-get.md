---
swagger: "2.0"
info:
  title: Reddit
  description: The Reddit API allows you to access the user submitted and rated stories
    on reddit.com. It also provides advanced functionality, including user account
    information and sub-reddit moderation.
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
  '{/r/subreddit}/new.json':
    get:
      summary: Get Subreddit New
      description: This endpoint is a listing
      operationId: get&nbsp;RSubredditNew
      parameters:
      - in: path
        name: /r/subreddit
        description: the subreddit
        type: string
        format: string
      - in: query
        name: after
        description: fullname of a thing
        type: string
      - in: query
        name: before
        description: fullname of a thing
        type: string
      - in: query
        name: count
        description: 'a positive integer (default: 0)'
        type: string
      - in: query
        name: limit
        description: 'the maximum number of items desired (default: 25, maximum: 100)'
        type: string
      - in: query
        name: show
        description: (optional) the string all
        type: string
      - in: query
        name: sr_detail
        description: (optional) expand subreddits
        type: string
      responses:
        200:
          description: OK
      tags:
      - subreddit
      - new
definitions: []
x-collection-name: Reddit
x-streamrank:
  polling_total_time_average: "0.73"
  polling_size_download_average: "46436.48"
  streaming_total_time_average: "0.44"
  streaming_size_download_average: "23226.51"
  change_yes: "197"
  change_no: "0"
  time_percentage: "40"
  size_percentage: "50"
  change_percentage: "100"
  last_run: "2018-05-06"
  days_run: "1"
  minute_run: "0"
---