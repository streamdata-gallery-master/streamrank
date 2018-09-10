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
  /2/cities:
    get:
      summary: Cities
      description: Returns Meetup cities
      operationId: cities
      parameters:
      - in: query
        name: country
        description: A valid country code
        type: string
      - in: query
        name: lat
        description: Latitude to search
        type: string
      - in: query
        name: lon
        description: Longitude to search
        type: string
      - in: query
        name: query
        description: Search term and/or zip to look for (if this is specified, max
          result size limited to 10)
        type: string
      - in: query
        name: radius
        description: When searching by lat/lon only, specify a radius to search (default
          50 miles)
        type: string
      - in: query
        name: state
        description: A valid state code for the given country, if the country has
          states
        type: string
      responses:
        200:
          description: OK
      tags:
      - events
      - cities
definitions: []
x-collection-name: Meetup
x-streamrank:
  polling_total_time_average: "0.13"
  polling_size_download_average: "72268.59"
  streaming_total_time_average: "0.08"
  streaming_size_download_average: "36705.26"
  change_yes: "119"
  change_no: "2166"
  time_percentage: "43"
  size_percentage: "49"
  change_percentage: "5"
  last_run: "2018-05-12"
  days_run: "8"
  minute_run: "0"
---