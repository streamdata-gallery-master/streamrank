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
  /2/concierge:
    get:
      summary: Concierge
      description: Recommends upcoming meetups for the authorized member in a given
        location and in thier groups
      operationId: events
      x-api-path-slug: 2concierge-get
      parameters:
      - in: query
        name: category_id
        description: Comma delimited list of category ids to limit recommendations
          to
        type: string
      - in: query
        name: city
        description: A valid city
        type: string
      - in: query
        name: country
        description: A valid country code
        type: string
      - in: query
        name: fields
        description: Request that additional fields (separated by commas) be included
          in the output
        type: string
      - in: query
        name: lat
        description: A valid latitude, limits the returned group events to those within
          radius miles
        type: string
      - in: query
        name: lon
        description: A valid longitude, limits the returned group events to those
          within radius miles
        type: string
      - in: query
        name: page_token
        description: An opaque string used to page through results
        type: string
      - in: query
        name: radius
        description: Radius, in miles for geographic requests, defaults to the member's
          preferred radius or 0
        type: string
      - in: query
        name: self_groups
        description: set to "include" or "exclude" groups the authorized member belongs
          to
        type: string
      - in: query
        name: state
        description: If searching in a country with states, a valid 2 character state
          code
        type: string
      - in: query
        name: text_format
        description: Format of the description text, "html", "plain", or "simplehtml"
        type: string
      - in: query
        name: time
        description: Return events scheduled within the given time range, defined
          by two times separated with a single comma
        type: string
      - in: query
        name: topic_id
        description: Comma delimited list of topics to help inform recommendation
        type: string
      - in: query
        name: with_friends
        description: Boolean parameter
        type: string
      - in: query
        name: zip
        description: A valid US zip code, limits the returned groups to those within
          radius miles
        type: string
      responses:
        200:
          description: OK
      tags:
      - events
definitions: []
x-collection-name: Meetup
x-streamrank:
  polling_total_time_average: "0.46"
  polling_size_download_average: "54949.14"
  streaming_total_time_average: "0.25"
  streaming_size_download_average: "27825.76"
  change_yes: "1040"
  change_no: "1247"
  time_percentage: "46"
  size_percentage: "49"
  change_percentage: "45"
  last_run: "2018-05-12"
  days_run: "8"
  minute_run: "0"
---