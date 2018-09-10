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
  /2/event_comments:
    get:
      summary: Comments v2
      description: This method returns messages that appear under Talk about this
        Meetup
      operationId: events
      parameters:
      - in: query
        name: api_version
        description: "2"
        type: string
      - in: query
        name: callback
        description: Name of a function to be called with an array of Event Comment
          notification objects
        type: string
      - in: query
        name: comment_id
        description: Return comments for a given set of comment IDs, separated by
          commas
        type: string
      - in: query
        name: event_id
        description: Limit notifications to a specific event id
        type: string
      - in: query
        name: event_id
        description: Return comments on these events, separated by commas
        type: string
      - in: query
        name: fields
        description: Optionally accepts the value "member_photo" or "notifications"
        type: string
      - in: query
        name: group_id
        description: Return comments in groups with these ID numbers, separated by
          commas
        type: string
      - in: query
        name: member_id
        description: Return comments for the given member_ids, separated by commas
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
      - comments
definitions: []
x-collection-name: Meetup
x-streamrank:
  polling_total_time_average: "0.36"
  polling_size_download_average: "72163.83"
  streaming_total_time_average: "0.21"
  streaming_size_download_average: "36520.91"
  change_yes: "101"
  change_no: "2185"
  time_percentage: "43"
  size_percentage: "49"
  change_percentage: "4"
  last_run: "2018-05-12"
  days_run: "8"
  minute_run: "0"
---