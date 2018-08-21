---
swagger: "2.0"
info:
  title: Spreaker API
  version: v1
host: api.spreaker.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /user/{user_id}/actions:
    get:
      summary: Get User Actions
      description: Retrieves the user actions settings
      operationId: getUserUserActions
      parameters:
      - in: query
        name: EPISODE_BROADCAST
        description: The user has published a new episode ( either live or podcast
          )
      - in: query
        name: FACEBOOK
        description: ' The user wants to share on facebook the specified action'
      - in: query
        name: RADIO_FOLLOW
        description: The user starts following a radio
      - in: query
        name: RADIO_MESSAGE
        description: The user has sent a message to a radio
      - in: query
        name: SHOW_FOLLOW
        description: ' The user starts following a show'
      - in: query
        name: SHOW_MESSAGE
        description: ' The user has sent a message to a show'
      - in: query
        name: TWITTER
        description: The user wants to share on twitter the specified action
      - in: query
        name: USER_FOLLOW
        description: The user starts following another user
      - in: query
        name: user_id
        description: The user id
      responses:
        200:
          description: OK
      tags:
      - user
      - actions
definitions: []
x-collection-name: Spreaker
x-streamrank:
  polling_total_time_average: "0"
  polling_size_download_average: "0"
  streaming_total_time_average: "0"
  streaming_size_download_average: "0"
  change_yes: "0"
  change_no: "0"
  time_percentage: "0"
  size_percentage: "0"
  change_percentage: "200"
  last_run: ~
  days_run: "0"
  minute_run: "0"
---