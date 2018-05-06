---
swagger: "2.0"
info:
  title: Meetup
  description: 'The Meetup API provides simple RESTful HTTP and streaming interfaces
    for exploring and interacting Meetup platform from your own apps. The API is a
    set of core methods and a common request format. These are combined to form a
    URL that returns the information you want. '
  version: 1.0.0
host: api.meetup.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /find/locations:
    get:
      summary: Find locations
      description: Provides a query interface for finding known locations
      operationId: geo
      parameters:
      - in: query
        name: lat
        description: Search for locations based on location latitude
        type: string
      - in: query
        name: lon
        description: Search for locations based on location longitude
        type: string
      - in: query
        name: offset
        description: The current offset in the paginated set, represented as an incrementing
          value
        type: string
      - in: query
        name: page
        description: The desired number of locations to return in a single set of
          results
        type: string
      - in: query
        name: query
        description: Search for locations based on city name or zip code
        type: string
      responses:
        200:
          description: OK
      tags:
      - events
      - search
      - location
definitions: []
x-collection-name: Meetup
x-streamrank:
  polling_total_time_average: "0.1"
  polling_size_download_average: "31734.99"
  streaming_total_time_average: "0.05"
  streaming_size_download_average: "15943.87"
  change_yes: "3"
  change_no: "419"
  time_percentage: "44"
  size_percentage: "50"
  change_percentage: "1"
  last_run: "2018-05-06"
  days_run: "2"
  minute_run: "0"
---