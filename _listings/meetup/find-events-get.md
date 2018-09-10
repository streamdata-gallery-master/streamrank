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
  /find/events:
    get:
      summary: Find Events
      description: Returns list of upcoming events based on location
      operationId: deprecated
      parameters:
      - in: query
        name: fields
        description: A comma-delimited list of optional fields to populate in the
          response
        type: string
      - in: query
        name: lat
        description: Approximate target latitude
        type: string
      - in: query
        name: lon
        description: Approximate target longitude
        type: string
      - in: query
        name: radius
        description: Radius in miles
        type: string
      - in: query
        name: text
        description: Raw full text search query
        type: string
      responses:
        200:
          description: OK
      tags:
      - events
      - search
definitions: []
x-collection-name: Meetup
x-streamrank:
  polling_total_time_average: "0.64"
  polling_size_download_average: "125477.38"
  streaming_total_time_average: "0.33"
  streaming_size_download_average: "62772.42"
  change_yes: "50"
  change_no: "2231"
  time_percentage: "48"
  size_percentage: "50"
  change_percentage: "2"
  last_run: "2018-05-12"
  days_run: "8"
  minute_run: "0"
---