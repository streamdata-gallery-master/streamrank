---
swagger: "2.0"
info:
  title: Columbus Indiana 311 GeoReport API
  description: Open311 allows you to get/post civic information of cities via a unified
    interface. The GeoReport part allows you to submit and view issues at the public
    local space
  contact:
    name: Open311 community
    url: http://wiki.open311.org/GeoReport_v2/
    email: discuss@lists.open311.org
  version: 1.0.0
host: csr.columbus.in.gov
basePath: /csr/open311/v2/
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
      parameters:
      - in: query
        name: end_date
        description: Latest datetime to include in search
      - in: query
        name: No Name
      - in: path
        name: response_format
        description: The response in XML or JSON format
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
x-collection-name: Columbus Indiana 311
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