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
  /2/events:
    get:
      summary: Events
      description: Access Meetup events using a group, member, or event id
      operationId: events
      parameters:
      - in: query
        name: event_id
        description: Multiple ids may be separated with commas
        type: string
      - in: query
        name: fields
        description: Request that additional fields (separated by commas) be included
          in the output
        type: string
      - in: query
        name: group_domain
        description: Group custom domain
        type: string
      - in: query
        name: group_id
        description: Multiple ids may be separated with commas
        type: string
      - in: query
        name: group_urlname
        description: Path to group from meetup
        type: string
      - in: query
        name: limited_events
        description: Include limited event information for private groups that wish
          to expose only a small amount of information about their events
        type: string
      - in: query
        name: member_id
        description: Single member id, to find events in this member's groups
        type: string
      - in: query
        name: rsvp
        description: Filters events by the currently authenticated member's RSVP status
        type: string
      - in: query
        name: status
        description: Status may be "upcoming", "past", "proposed", "suggested", "cancelled",
          "draft" or multiple separated by a comma
        type: string
      - in: query
        name: text_format
        description: Format of the description text, "html" or "plain"
        type: string
      - in: query
        name: time
        description: Return events scheduled within the given time range, defined
          by two times separated with a single comma
        type: string
      - in: query
        name: venue_id
        description: Multiple ids may be separated with commas
        type: string
      responses:
        200:
          description: OK
      tags:
      - events
definitions: []
x-collection-name: Meetup
x-streamrank:
  polling_total_time_average: "0.09"
  polling_size_download_average: "808.33"
  streaming_total_time_average: "0.07"
  streaming_size_download_average: "736.67"
  change_yes: "2"
  change_no: "1"
  time_percentage: "14"
  size_percentage: "9"
  change_percentage: "67"
  last_run: "2018-05-06"
  days_run: "2"
  minute_run: "0"
---