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
  /2/rsvps:
    get:
      summary: RSVPs v2
      description: Query for Event RSVPs by event
      operationId: rsvps
      parameters:
      - in: query
        name: api_version
        description: "2"
        type: string
      - in: query
        name: callback
        description: Name of a function to be called with an array of RSVP notification
          objects
        type: string
      - in: query
        name: event_id
        description: Multiple alphanumeric ids may be separated with commas
        type: string
      - in: query
        name: event_id
        description: Limit notifications to a specific event id
        type: string
      - in: query
        name: fields
        description: Parameter for requesting optional response properties, set to
          other_services for a list of third party services
        type: string
      - in: query
        name: rsvp
        description: Filters response on RSVP status
        type: string
      - in: query
        name: since_count
        description: Request that some number of recent messages be sent immediately,
          if available
        type: string
      - in: query
        name: since_mtime
        description: Should be supplied for all but the first polling request, so
          that any missed notifications are can be sent in an immediate response
        type: string
      responses:
        200:
          description: OK
      tags:
      - events
definitions: []
x-collection-name: Meetup
x-streamrank:
  polling_total_time_average: "0.11"
  polling_size_download_average: "12284.58"
  streaming_total_time_average: "0.06"
  streaming_size_download_average: "6168.84"
  change_yes: "29"
  change_no: "2251"
  time_percentage: "44"
  size_percentage: "50"
  change_percentage: "1"
  last_run: "2018-05-12"
  days_run: "8"
  minute_run: "0"
---