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
  /api/search_reddit_names.json:
    get:
      summary: Get Search Reddit Names
      description: List subreddit names that begin with a query string
      operationId: get&nbsp;SearchRedditNames
      x-api-path-slug: apisearch-reddit-names-json-get
      parameters:
      - in: query
        name: exact
        description: boolean value
        type: string
      - in: query
        name: include_over_18
        description: boolean value
        type: string
      - in: query
        name: include_unadvertisable
        description: boolean value
        type: string
      - in: query
        name: query
        description: a string up to 50 characters long, consisting of printable characters
        type: string
      responses:
        200:
          description: OK
      tags:
      - search
      - reddit
      - names
definitions: []
x-collection-name: Reddit
x-streamrank:
  polling_total_time_average: "0.56"
  polling_size_download_average: "376.76"
  streaming_total_time_average: "0.36"
  streaming_size_download_average: "301.15"
  change_yes: "10"
  change_no: "195"
  time_percentage: "35"
  size_percentage: "20"
  change_percentage: "5"
  last_run: "2018-05-06"
  days_run: "1"
  minute_run: "0"
---