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
  /organizers/:
    post:
      summary: Add Organizers
      description: Makes a new organizer
      operationId: postOrganizers
      parameters:
      - in: query
        name: organizer.description.html
        description: The description of the organizer
        type: query
      - in: query
        name: organizer.facebook
        description: The Facebook URL ID for the organizer
        type: query
      - in: query
        name: organizer.instagram
        description: The Instagram numeric ID for the organizer
        type: query
      - in: query
        name: organizer.logo.id
        description: The logo id of the organizer
        type: query
      - in: query
        name: organizer.long_description.html
        description: The long description of the organizer
        type: query
      - in: query
        name: organizer.name
        description: The name of the organizer
        type: query
      - in: query
        name: organizer.twitter
        description: The Twitter handle for the organizer
        type: query
      - in: query
        name: organizer.website
        description: The website for the organizer
        type: query
      responses:
        200:
          description: OK
      tags:
      - organizers
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