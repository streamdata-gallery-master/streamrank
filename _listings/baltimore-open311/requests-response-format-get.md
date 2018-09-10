---
swagger: "2.0"
info:
  title: Open311 GeoReport API
  description: Open311 allows you to get/post civic information of cities via a unified
    interface. The GeoReport part allows you to submit and view issues at the public
    local space
  termsOfService: (depends on server instance for example NYC http://dev.cityofchicago.org/docs/api/tos)
  contact:
    name: Open311 community
    url: http://wiki.open311.org/GeoReport_v2/
    email: discuss@lists.open311.org
  version: 1.0.0
host: 311.baltimorecity.gov
basePath: /open311/v2/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /requests.{response_format}:
    get:
      summary: Requests
      description: Query the current status of multiple requests
      operationId: query-the-current-status-of-multiple-requests
      x-api-path-slug: requestsresponse-format-get
      parameters:
      - in: query
        name: end_date
        description: Latest datetime to include in search
      - in: path
        name: response_format
        description: Response in XML or JSON
        type: string
        format: string
      - in: query
        name: service_code
        description: Specify the service type by calling the unique ID of the service_code
      - in: query
        name: service_request_id
        description: To call multiple Service Requests at once, multiple service_request_id
          can be declared; comma delimited
      - in: query
        name: start_date
        description: Earliest datetime to include in search
      - in: query
        name: status
        description: Allows one to search for requests which have a specific status
      responses:
        200:
          description: OK
      tags:
      - "311"
      - requests
definitions:
  Service:
    properties:
      service_code:
        description: This is a default description.
        type: get
      service_name:
        description: This is a default description.
        type: get
      description:
        description: This is a default description.
        type: get
      metadata:
        description: This is a default description.
        type: get
      type:
        description: This is a default description.
        type: get
      keywords:
        description: This is a default description.
        type: get
      group:
        description: This is a default description.
        type: get
  ServiceDefinition:
    properties:
      service_code:
        description: This is a default description.
        type: get
      attributes:
        description: This is a default description.
        type: get
  ServiceAttribute:
    properties:
      variable:
        description: This is a default description.
        type: get
      code:
        description: This is a default description.
        type: get
      datatype:
        description: This is a default description.
        type: get
      required:
        description: This is a default description.
        type: get
      datatype_description:
        description: This is a default description.
        type: get
      order:
        description: This is a default description.
        type: get
      description:
        description: This is a default description.
        type: get
      values:
        description: This is a default description.
        type: get
  AttributeValue:
    properties:
      key:
        description: This is a default description.
        type: get
      name:
        description: This is a default description.
        type: get
  Request:
    properties:
      service_request_id:
        description: This is a default description.
        type: get
      status:
        description: This is a default description.
        type: get
      status_notes:
        description: This is a default description.
        type: get
      service_name:
        description: This is a default description.
        type: get
      service_code:
        description: This is a default description.
        type: get
      description:
        description: This is a default description.
        type: get
      agency_responsible:
        description: This is a default description.
        type: get
      service_notice:
        description: This is a default description.
        type: get
      requested_datetime:
        description: This is a default description.
        type: get
      updated_datetime:
        description: This is a default description.
        type: get
  RequestResponse:
    properties:
      service_request_id:
        description: This is a default description.
        type: get
      token:
        description: This is a default description.
        type: get
      service_notice:
        description: This is a default description.
        type: get
      account_id:
        description: This is a default description.
        type: get
  TokenResponse:
    properties:
      service_request_id:
        description: This is a default description.
        type: get
      token:
        description: This is a default description.
        type: get
x-collection-name: Baltimore Open311
x-streamrank:
  polling_total_time_average: "27.4"
  polling_size_download_average: "10739.6"
  streaming_total_time_average: "26.79"
  streaming_size_download_average: "5369.8"
  change_yes: "3"
  change_no: "2"
  time_percentage: "2"
  size_percentage: "50"
  change_percentage: "60"
  last_run: "2018-09-09"
  days_run: "0"
  minute_run: "0"
---