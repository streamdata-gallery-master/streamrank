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
  /notifications:
    get:
      summary: Notifications
      description: Returns all recent Meetup notifications for the authorized member
      operationId: notifications
      x-api-path-slug: notifications-get
      parameters:
      - in: query
        name: fields
        description: Request that additional fields (separated by commas) be included
          in the output
        type: string
      responses:
        200:
          description: OK
      tags:
      - events
      - notifications
definitions: []
x-collection-name: Meetup
x-streamrank:
  polling_total_time_average: "2.78"
  polling_size_download_average: "27690.84"
  streaming_total_time_average: "1.48"
  streaming_size_download_average: "13848"
  change_yes: "45"
  change_no: "2236"
  time_percentage: "47"
  size_percentage: "50"
  change_percentage: "2"
  last_run: "2018-05-12"
  days_run: "8"
  minute_run: "0"
---