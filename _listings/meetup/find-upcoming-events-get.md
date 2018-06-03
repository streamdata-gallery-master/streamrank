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
  /find/upcoming_events:
    get:
      summary: Find Upcoming Events
      description: Returns a list of upcoming events
      operationId: events
      parameters:
      - in: query
        name: end_date_range
        description: Return events that start before this date
        type: string
      - in: query
        name: end_time_range
        description: Return events that start before this time
        type: string
      - in: query
        name: excluded_groups
        description: IDs for groups to exclude from the returned events
        type: string
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
        name: order
        description: The sort order of returned events
        type: string
      - in: query
        name: page
        description: A target minimum number of events to return in a single page
          of results
        type: string
      - in: query
        name: radius
        description: Radius in miles
        type: string
      - in: query
        name: self_groups
        description: set to 'include' or 'exclude' or 'only' get groups that the member
          belongs to
        type: string
      - in: query
        name: start_date_range
        description: Return events that start after this date
        type: string
      - in: query
        name: start_time_range
        description: Return events that start after this time
        type: string
      - in: query
        name: text
        description: Full text search query
        type: string
      - in: query
        name: topic_category
        description: Numeric topic category identifier for filtering recommendations
          by a topic category
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
  polling_total_time_average: "0.81"
  polling_size_download_average: "80842.11"
  streaming_total_time_average: "0.42"
  streaming_size_download_average: "40472.68"
  change_yes: "933"
  change_no: "1347"
  time_percentage: "48"
  size_percentage: "50"
  change_percentage: "41"
  last_run: "2018-05-12"
  days_run: "8"
  minute_run: "0"
---