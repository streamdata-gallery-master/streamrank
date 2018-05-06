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
  /subreddits/new.json:
    get:
      summary: Get New Subreddits
      description: Returns new subreddits
      operationId: getNewSubreddit
      parameters:
      - in: query
        name: query
        description: a string no longer than 50 characters
        type: string
      responses:
        200:
          description: OK
      tags:
      - subreddits
      - new
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