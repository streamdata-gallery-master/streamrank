---
swagger: "2.0"
info:
  title: Shared Vehicle (Bike+Scooter) API
  description: The Shared Vehicle API is a comprehensive API that provides information
    about bike and scooter share systems, including available vehicles and prices.
  version: 1.0.0
host: api.coord.co
basePath: /v1/sv/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /location:
    get:
      summary: Find Vehicles by location
      description: Get locations in the requested search area, as a GeoJSON FeatureCollection
      operationId: findVehiclesbyLocation
      x-api-path-slug: location-get
      parameters:
      - in: query
        name: latitude
        description: Latitude to return results for
        type: string
        format: string
      - in: query
        name: longitude
        description: Longitude to return results for
        type: string
        format: string
      - in: query
        name: radius_km
        description: ' Distance, in kilometers, from (latitude, longitude) we will
          return results for'
        type: string
        format: string
      responses:
        200:
          description: OK
      tags:
      - scooters
      - bikes
definitions: []
x-collection-name: Coord
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