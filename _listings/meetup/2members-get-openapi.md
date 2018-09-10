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
      x-api-path-slug: 2members-get
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
  polling_total_time_average: "3.06"
  polling_size_download_average: "1128452.03"
  streaming_total_time_average: "1.8"
  streaming_size_download_average: "570303.18"
  change_yes: "94"
  change_no: "2190"
  time_percentage: "41"
  size_percentage: "49"
  change_percentage: "4"
  last_run: "2018-05-12"
  days_run: "8"
  minute_run: "0"
---