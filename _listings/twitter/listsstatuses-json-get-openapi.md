---
swagger: "2.0"
x-collection-name: Twitter
x-complete: 0
info:
  title: Twitter List Statuses
  description: Returns a timeline of tweets authored by memebers of the specified
    list
  version: "1.1"
host: api.twitter.com
basePath: /1.1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /search/tweets.json:
    get:
      summary: Search Tweets
      description: returns collection of relevant Tweets matching query
      operationId: returns-collection-of-relevant-tweets-matching-query
      x-api-path-slug: searchtweets-json-get
      parameters:
      - in: query
        name: callback
        description: response will use the callback with given name
      - in: query
        name: count
        description: number of tweets to return
      - in: query
        name: geocode
        description: returns tweets by users located within given radius
      - in: query
        name: include_entities
        description: whether or not to include entities
      - in: query
        name: lang
        description: restricts tweets to a given language
      - in: query
        name: locale
        description: language of query you are sending
      - in: query
        name: max_id
        description: returns results with an ID less than/equal to specified ID
      - in: query
        name: q
        description: URL-encoded search query of 500 characters max
      - in: query
        name: result_type
        description: specifies type of search results you prefer
      - in: query
        name: since_id
        description: return results with ID greater than specified
      - in: query
        name: until
        description: returns tweets created before given date
      responses:
        200:
          description: OK
      tags:
      - Social
      - Statuses
  /lists/statuses.json:
    get:
      summary: List Statuses
      description: Returns a timeline of tweets authored by memebers of the specified
        list
      operationId: returns-a-timeline-of-tweets-authored-by-memebers-of-the-specified-list
      x-api-path-slug: listsstatuses-json-get
      parameters:
      - in: query
        name: count
        description: Specifies the number of results to retrieve per page
      - in: query
        name: include_entities
        description: Entities are ON by default
      - in: query
        name: include_rts
        description: When set to either true, t or 1, the list timeline will contain
          native retweets in addition to the standard stream of tweets
      - in: query
        name: list_id
        description: The numerical id of the list
      - in: query
        name: max_id
        description: Returns results with an ID less than or equal to the specified
          ID
      - in: query
        name: owner_id
        description: The user ID of the user who owns the list being requested by
          a slug
      - in: query
        name: owner_screen_name
        description: The screen name of the user who owns the list being requested
          by a slug
      - in: query
        name: since_id
        description: Returns results with an ID greater than the sepcified ID
      - in: query
        name: slug
        description: You can identify a list by its slug instead of its numerical
          id
      responses:
        200:
          description: OK
      tags:
      - Social
      - Lists
x-streamrank:
  polling_total_time_average: "0.27"
  polling_size_download_average: "93997.71"
  streaming_total_time_average: "0.14"
  streaming_size_download_average: "47148.86"
  change_yes: "100"
  change_no: "67"
  time_percentage: "46"
  size_percentage: "50"
  change_percentage: "60"
  last_run: "2018-05-06"
  days_run: "1"
  minute_run: "0"
---