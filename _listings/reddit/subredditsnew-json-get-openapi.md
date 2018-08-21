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
  '{/r/subreddit}/rising.json':
    get:
      summary: Get Subreddit Rising
      description: This endpoint is a listing.
      operationId: get&nbsp;RSubredditRising
      x-api-path-slug: rsubredditrising-json-get
      parameters:
      - in: path
        name: /r/subreddit
        description: The subreddit
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
      - Subreddit
      - Rising
  /best.json:
    get:
      summary: Get Best
      description: This endpoint is a listing.
      operationId: get&nbsp;Best
      x-api-path-slug: best-json-get
      parameters:
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
      - Best
  /subreddits/search.json:
    get:
      summary: Get Subreddits Search
      description: Search subreddits by title and description.
      operationId: get&nbsp;SubredditsSearch
      x-api-path-slug: subredditssearch-json-get
      parameters:
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
        name: q
        description: a search query
        type: string
      - in: query
        name: show
        description: (optional) the string all
        type: string
      - in: query
        name: sort
        description: one of (relevance, activity)
        type: string
      - in: query
        name: sr_detail
        description: (optional) expand subreddits
        type: string
      responses:
        200:
          description: OK
      tags:
      - Subreddits
      - Search
  /subreddits/popular.json:
    get:
      summary: Get Subreddits Where
      description: Get all subreddits.
      operationId: get&nbsp;SubredditsWhere
      x-api-path-slug: subredditspopular-json-get
      parameters:
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
      - Subreddits
      - Where
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