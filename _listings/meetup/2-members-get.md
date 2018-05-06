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
  /2/members:
    get:
      summary: Members
      description: API method for accessing members of Meetup Groups
      operationId: members
      parameters:
      - in: query
        name: fields
        description: Request that additional fields (separated by commas) be included
          in the output
        type: string
      - in: query
        name: group_id
        description: Return members in groups with these ID numbers, separated by
          commas
        type: string
      - in: query
        name: group_urlname
        description: Return members for the group with the given custom URL path
        type: string
      - in: query
        name: member_id
        description: Return the member with this ID
        type: string
      - in: query
        name: service
        description: Match users by the external services they've linked to their
          member account, specified as "servicename:identifier"
        type: string
      - in: query
        name: topic,groupnum
        description: Return members for the group with given topic and number
        type: string
      responses:
        200:
          description: OK
      tags:
      - events
      - groups
      - member
definitions: []
x-collection-name: Meetup
x-streamrank:
  polling_total_time_average: "2.8"
  polling_size_download_average: "1137528.65"
  streaming_total_time_average: "1.66"
  streaming_size_download_average: "570134.85"
  change_yes: "4"
  change_no: "419"
  time_percentage: "41"
  size_percentage: "50"
  change_percentage: "1"
  last_run: "2018-05-06"
  days_run: "2"
  minute_run: "0"
---