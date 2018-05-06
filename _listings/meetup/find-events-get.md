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
  polling_size_download_average: "130123.5"
  streaming_total_time_average: "0.33"
  streaming_size_download_average: "65273.82"
  change_yes: "10"
  change_no: "413"
  time_percentage: "49"
  size_percentage: "50"
  change_percentage: "2"
  last_run: "2018-05-06"
  days_run: "2"
  minute_run: "0"
---