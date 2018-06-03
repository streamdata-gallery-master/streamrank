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
  /v1/signals/{signal_id}/dimensions/:
    get:
      summary: Retrieve All Dimensions
      description: This action returns a summary for each dimension of your Signal
      operationId: V1SignalsDimensionsBySignalIdGet
      parameters:
      - in: path
        name: signal_id
      responses:
        200:
          description: OK
      tags:
      - signals
      - signal
      - dimensions
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