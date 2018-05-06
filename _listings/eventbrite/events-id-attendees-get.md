---
swagger: "2.0"
info:
  title: Eventbrite
  description: The Eventbrite API is the best way to integrate and extend Eventbrite
    for your event or organising needs. Version 3 of the API brings you faster responses,
    consistent data types, more endpoints, and easier debugging and testing.
  version: 1.0.0
host: www.eventbriteapi.com
basePath: /v3
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /events/{id}/attendees/:
    get:
      summary: Get Events  Attendees
      description: Returns a paginated response with a key of attendees, containing
        a list of attendee
      operationId: getEventsAttendees
      parameters:
      - in: query
        name: attendee_ids
        description: Only return attendees whose ids are in this list
        type: query
      - in: query
        name: changed_since
        description: Only return attendees changed on or after the time given
        type: query
      - in: path
        name: id
        description: The unique event id
        type: string
        format: string
      - in: query
        name: last_item_seen
        description: Only return attendees changed on or after the time given and
          with an id bigger than last item seen
        type: query
      - in: query
        name: status
        description: Limits results to either confirmed attendees or cancelled/refunded/etc
        type: query
      responses:
        200:
          description: OK
      tags:
      - events
      - ""
      - attendees
definitions: []
x-collection-name: Eventbrite
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