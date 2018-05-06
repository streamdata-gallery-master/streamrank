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
  polling_total_time_average: "0.16"
  polling_size_download_average: "27473.95"
  streaming_total_time_average: "0.09"
  streaming_size_download_average: "13770.91"
  change_yes: "31"
  change_no: "390"
  time_percentage: "45"
  size_percentage: "50"
  change_percentage: "7"
  last_run: "2018-05-06"
  days_run: "2"
  minute_run: "0"
---