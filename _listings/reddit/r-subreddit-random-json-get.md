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
  '{/r/subreddit}/random.json':
    get:
      summary: Get Subreddit Random
      description: The Serendipity button
      operationId: get&nbsp;RSubredditRandom
      parameters:
      - in: path
        name: /r/subreddit
        description: The subreddit
        type: string
        format: string
      responses:
        200:
          description: OK
      tags:
      - subreddit
      - random
definitions: []
x-collection-name: Reddit
x-streamrank:
  polling_total_time_average: ~
  polling_size_download_average: ~
  streaming_total_time_average: ~
  streaming_size_download_average: ~
  change_yes: ~
  change_no: ~
  time_percentage: ~
  size_percentage: ~
  change_percentage: ~
  last_run: ~
  days_run: ~
  minute_run: ~
---