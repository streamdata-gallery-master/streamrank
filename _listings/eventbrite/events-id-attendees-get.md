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
  polling_total_time_average: "0.16"
  polling_size_download_average: "136"
  streaming_total_time_average: "0.16"
  streaming_size_download_average: "136"
  change_yes: "1"
  change_no: "0"
  time_percentage: "0"
  size_percentage: "0"
  change_percentage: "100"
  last_run: "2018-05-04"
  days_run: "0"
  minute_run: "0"
---