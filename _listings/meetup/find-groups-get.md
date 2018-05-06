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
  /find/groups:
    get:
      summary: Find Groups
      description: Text, location, category and friend-based group searches
      operationId: groups
      parameters:
      - in: query
        name: category
        description: Comma-delimited list of numeric category ids
        type: string
      - in: query
        name: country
        description: A valid two character country code, defaults to US
        type: string
      - in: query
        name: fallback_suggestions
        description: boolean indicator of whether or not to return a list of curated
          suggestions for groups if we can't find groups matching your criteria
        type: string
      - in: query
        name: fields
        description: Request that additional fields (separated by commas) be included
          in the output
        type: string
      - in: query
        name: filter
        description: Determines which groups are returned
        type: string
      - in: query
        name: lat
        description: Approximate latitude
        type: string
      - in: query
        name: location
        description: Raw text location query
        type: string
      - in: query
        name: lon
        description: Approximate longitude
        type: string
      - in: query
        name: radius
        description: Radius in miles
        type: string
      - in: query
        name: self_groups
        description: set to 'include' or 'exclude' Meetups the authorized member belongs
          to; default is 'include'
        type: string
      - in: query
        name: text
        description: Raw full text search query
        type: string
      - in: query
        name: topic_id
        description: Comma-delimited list of numeric topic ids
        type: string
      - in: query
        name: upcoming_events
        description: If true, filters text and category based searches on groups that
          have upcoming events
        type: string
      - in: query
        name: zip
        description: Zipcode of location to limit search to
        type: string
      responses:
        200:
          description: OK
      tags:
      - events
      - search
      - groups
definitions: []
x-collection-name: Meetup
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