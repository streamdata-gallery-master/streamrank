---
swagger: "2.0"
info:
  title: PredictHQ API
  description: 'TODO: Add Description'
  version: 1.0.0
host: api.predicthq.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v1/signals/:
    get:
      summary: Retrieve All Signals
      description: It's easy to get a list of all Signals that are associated with
        your account
      operationId: V1SignalsGet
      x-api-path-slug: v1signals-get
      responses:
        200:
          description: OK
      tags:
      - signals
definitions:
  CreateDataPointsrequest:
    properties:
      uid:
        description: This is a default description.
        type: get
      date:
        description: This is a default description.
        type: get
      latitude:
        description: This is a default description.
        type: get
      longitude:
        description: This is a default description.
        type: get
      initiated:
        description: This is a default description.
        type: get
      completed:
        description: This is a default description.
        type: get
  UpdateASignalrequest:
    properties:
      name:
        description: This is a default description.
        type: get
      country:
        description: This is a default description.
        type: get
      dimensions:
        description: This is a default description.
        type: get
  Dimension:
    properties:
      type:
        description: This is a default description.
        type: get
      name:
        description: This is a default description.
        type: get
  CreateASignalrequest:
    properties:
      name:
        description: This is a default description.
        type: get
      country:
        description: This is a default description.
        type: get
      dimensions:
        description: This is a default description.
        type: get
x-collection-name: PredictHQ
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