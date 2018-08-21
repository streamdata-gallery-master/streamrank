---
swagger: "2.0"
x-collection-name: Twitter
x-complete: 0
info:
  title: Twitter Search Tweets
  description: returns collection of relevant Tweets matching query
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
x-streamrank:
  polling_total_time_average: "0.25"
  polling_size_download_average: "75800.73"
  streaming_total_time_average: "0.14"
  streaming_size_download_average: "39495.85"
  change_yes: "171"
  change_no: "1"
  time_percentage: "46"
  size_percentage: "48"
  change_percentage: "99"
  last_run: "2018-05-06"
  days_run: "1"
  minute_run: "0"
---