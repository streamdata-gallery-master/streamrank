---
swagger: "2.0"
x-collection-name: Baltimore Open311
x-complete: 0
info:
  title: Baltimore Open311 Requests
  description: Query the current status of multiple requests.
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
      description: Query the current status of multiple requests.
      operationId: query-the-current-status-of-multiple-requests
      x-api-path-slug: requests-response-format-get
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
      - Requests
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