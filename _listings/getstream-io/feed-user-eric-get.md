---
swagger: "2.0"
info:
  title: Stream API
  description: '# How to use this collection1. Install the collection (done!)2. Check
    the ''general prerequisites'' section below for basic setup.3. Review the request
    folders and select a request to send.    - review the request description to check
    for any required parameters and/or request specific pre-requisites.4. Run the
    request.# General prerequisites - Create an app at Stream - Set postman environment
    variables for connectivity and authentication: **STREAM_APP_LOCATION**, **STREAM_API_KEY**,
    **STREAM_API_SECRET**# Collection overview: - Get Started: requests used in Stream''s
    getting started tutorial. - REST API Endpoints: examples of the documented [API
    endpoints](https://getstream.io/docs_rest/).'
  version: 1.0.0
host: eu-central-api.stream-io-api.com
basePath: /api/v1.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /feed/user/eric:
    get:
      summary: Retrieve a feed - ID filters and pagination
      description: Retrieves the activities within a feed with ID filtering on the
        activities to be returned
      operationId: FeedUserEricGet4
      parameters:
      - in: query
        name: api_key
      - in: query
        name: id_lt
      - in: header
        name: Stream-Auth-Type
      - in: header
        name: User-Agent
      responses:
        200:
          description: OK
      tags:
      - feed
      - user
      - eric
definitions:
  1.AddAnActivityToErics"user"Feedrequest:
    properties:
      actor:
        description: This is a default description.
        type: post
      tweet:
        description: This is a default description.
        type: post
      verb:
        description: This is a default description.
        type: post
      object:
        description: This is a default description.
        type: post
  1.Jessicas"timeline"FollowsErics"user"Feedrequest:
    properties:
      target:
        description: This is a default description.
        type: post
  2.AddAnActivityToErics"user"Feedrequest:
    properties:
      actor:
        description: This is a default description.
        type: post
      verb:
        description: This is a default description.
        type: post
      object:
        description: This is a default description.
        type: post
      youtube_id:
        description: This is a default description.
        type: post
      video_name:
        description: This is a default description.
        type: post
  1. jules "timelineAggregated" feed follows erics "user" feedrequest:
    properties:
      target:
        description: This is a default description.
        type: post
  UpdateActivitiesrequest:
    properties:
      activities:
        description: This is a default description.
        type: post
  Activity:
    properties:
      actor:
        description: This is a default description.
        type: post
      verb:
        description: This is a default description.
        type: post
      object:
        description: This is a default description.
        type: post
      time:
        description: This is a default description.
        type: post
      foreign_id:
        description: This is a default description.
        type: post
  Add an activity  basicrequest:
    properties:
      actor:
        description: This is a default description.
        type: post
      verb:
        description: This is a default description.
        type: post
      object:
        description: This is a default description.
        type: post
  Add an activity  custom fieldsrequest:
    properties:
      actor:
        description: This is a default description.
        type: post
      verb:
        description: This is a default description.
        type: post
      object:
        description: This is a default description.
        type: post
      message:
        description: This is a default description.
        type: post
  Add an activity - time and foreignIdrequest:
    properties:
      actor:
        description: This is a default description.
        type: post
      verb:
        description: This is a default description.
        type: post
      object:
        description: This is a default description.
        type: post
      foreign_id:
        description: This is a default description.
        type: post
      time:
        description: This is a default description.
        type: post
  Add an activity  to targettingrequest:
    properties:
      actor:
        description: This is a default description.
        type: post
      verb:
        description: This is a default description.
        type: post
      object:
        description: This is a default description.
        type: post
      to:
        description: This is a default description.
        type: post
  AddMultipleActivitiesrequest:
    properties:
      activities:
        description: This is a default description.
        type: post
  Activity12:
    properties:
      actor:
        description: This is a default description.
        type: post
      verb:
        description: This is a default description.
        type: post
      object:
        description: This is a default description.
        type: post
  CreateAFollowingRelationshiprequest:
    properties:
      target:
        description: This is a default description.
        type: post
  AddAnActivityToMultipleFeedsrequest:
    properties:
      feeds:
        description: This is a default description.
        type: post
  FollowMultipleFeedsrequest:
    properties:
      source:
        description: This is a default description.
        type: post
      target:
        description: This is a default description.
        type: post
x-collection-name: GetStream.io
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