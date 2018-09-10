---
swagger: "2.0"
info:
  title: Pay Run.IO
  description: Open, scableable, transparent payroll API.
  version: 17.18.6.206
host: api.test.payrun.io
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /Employers:
    get:
      summary: Gets all employers
      description: Gets links to all employers contained under the authorised application
        scope
      operationId: GetEmployers
      parameters:
      - in: header
        name: Api-Version
        description: The version of the api to target
      - in: header
        name: Authorization
        description: The OAuth 1 authorization header
      responses:
        200:
          description: OK
      tags:
      - ""
      - employers
definitions:
  AEAssessment:
    properties:
      AEAssessment:
        description: This is a default description.
        type: post
  Commentary:
    properties:
      Commentary:
        description: This is a default description.
        type: post
  DpsJobInstruction:
    properties:
      DpsJobInstruction:
        description: This is a default description.
        type: post
  DpsMessage:
    properties:
      DpsMessage:
        description: This is a default description.
        type: post
  Employee:
    properties:
      Employee:
        description: This is a default description.
        type: post
  Employer:
    properties:
      Employer:
        description: This is a default description.
        type: post
  ErrorModel:
    properties:
      ErrorModel:
        description: This is a default description.
        type: post
  HealthCheck:
    properties:
      HealthCheck:
        description: This is a default description.
        type: post
  JobInfo:
    properties:
      JobInfo:
        description: This is a default description.
        type: post
  Link:
    properties:
      Link:
        description: This is a default description.
        type: post
  LinkCollection:
    properties:
      LinkCollection:
        description: This is a default description.
        type: post
  NominalCode:
    properties:
      NominalCode:
        description: This is a default description.
        type: post
  PayCode:
    properties:
      PayCode:
        description: This is a default description.
        type: post
  PayInstruction:
    properties:
      PayInstruction:
        description: This is a default description.
        type: post
  PayLine:
    properties:
      PayLine:
        description: This is a default description.
        type: post
  PayRun:
    properties:
      PayRun:
        description: This is a default description.
        type: post
  PayRunJobInstruction:
    properties:
      PayRunJobInstruction:
        description: This is a default description.
        type: post
  PaySchedule:
    properties:
      PaySchedule:
        description: This is a default description.
        type: post
  Pension:
    properties:
      Pension:
        description: This is a default description.
        type: post
  Query:
    properties:
      Query:
        description: This is a default description.
        type: post
  ReportDefinition:
    properties:
      ReportDefinition:
        description: This is a default description.
        type: post
  ReportLine:
    properties:
      ReportLine:
        description: This is a default description.
        type: post
  ReportingInstruction:
    properties:
      ReportingInstruction:
        description: This is a default description.
        type: post
  RtiJobInstruction:
    properties:
      RtiJobInstruction:
        description: This is a default description.
        type: post
  RtiTransactionBase:
    properties:
      RtiTransactionBase:
        description: This is a default description.
        type: post
  Tag:
    properties:
      Tag:
        description: This is a default description.
        type: post
  TransformDefinition:
    properties:
      TransformDefinition:
        description: This is a default description.
        type: post
x-collection-name: PayRun
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