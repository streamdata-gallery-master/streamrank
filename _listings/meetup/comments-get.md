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
  /comments:
    get:
      summary: Comments
      description: API method for accessing meetup group comments
      operationId: groups
      parameters:
      - in: query
        name: group_id
        description: Return comments in groups with these ID numbers [separated by
          commas]
        type: string
      - in: query
        name: group_urlname
        description: Return comments for the group with this custom URL path
        type: string
      - in: query
        name: topic, groupnum
        description: Return comments for the group with given topic and number
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