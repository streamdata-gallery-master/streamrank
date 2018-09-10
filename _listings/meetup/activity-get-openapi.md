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
  /activity:
    get:
      summary: ActivityFeed
      description: API method for retrieving the activity feed for a member's groups
      operationId: feeds
      x-api-path-slug: activity-get
      parameters:
      - in: query
        name: member_id
        description: Returns activity from this member's groups
        type: string
      - in: query
        name: page_start
        description: Starting timestamp for item to return
        type: string
      responses:
        200:
          description: OK
      tags:
      - events
      - activity
      - feeds
definitions: []
x-collection-name: Meetup
x-streamrank:
  polling_total_time_average: "0.19"
  polling_size_download_average: "27661.69"
  streaming_total_time_average: "0.11"
  streaming_size_download_average: "14002.68"
  change_yes: "382"
  change_no: "1898"
  time_percentage: "44"
  size_percentage: "49"
  change_percentage: "17"
  last_run: "2018-05-12"
  days_run: "8"
  minute_run: "0"
---