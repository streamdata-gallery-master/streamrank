---
swagger: "2.0"
info:
  title: Eventbrite API
  description: Create, manage &amp; promote events. Add event-management features
    to your site. Show the world what exciting things are happening around them.
  version: 1.0.0
host: www.eventbriteapi.com
basePath: /v3/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /events/search/:
    get:
      summary: Event Search
      description: This method uses our search index to find publicly listed events
      operationId: Get_event_search_
      parameters:
      - in: query
        name: address
        description: The venue address
      - in: query
        name: category
        description: 'Event categories (comma seperated): conference, conventions,
          entertainment, fundraisers, meetings, other, performances, reunions, sales,
          seminars, social, sports, tradeshows, travel, religion, fairs, food, music,
          recreation'
      - in: query
        name: city
        description: The venue city
      - in: query
        name: country
        description: 2-letter country code, according to the ISO 3166 format
      - in: query
        name: count_only
        description: Only return the total number of events (???true??? or ???false???)
      - in: query
        name: data-type
        description: xml or json data-types are supported
      - in: query
        name: date
        description: The event start date
      - in: query
        name: date_created
        description: The date range the event was created, specified by a label or
          by exact dates
      - in: query
        name: date_modified
        description: The date range the event was modified, specified by a label or
          by exact dates
      - in: query
        name: keywords
        description: The search keywords
      - in: query
        name: latitude
        description: If ???within??? is set you can limit your search to wgs84 coordinates
          (latitude, longitude)
      - in: query
        name: longitude
        description: If ???within??? is set you can limit your search to wgs84 coordinates
          (latitude, longitude)
      - in: query
        name: max
        description: Limit the number of events returned
      - in: query
        name: organizer
        description: The organizer name
      - in: query
        name: page
        description: Allows for paging through the results of a query
      - in: query
        name: postal_code
        description: The postal/zip code of the venue
      - in: query
        name: q
        description: The query
        type: string
        format: string
      - in: query
        name: region
        description: The venue state/province/county/territory depending on the country
      - in: query
        name: since_id
        description: Returns events with id greater than ???since_id??? value
      - in: query
        name: sort_by
        description: Sort the list of events by ???id???, ???date???, ???name???,
          ???city???
      - in: query
        name: tracking_link
        description: The tracking link code to add to the event URLs
      - in: query
        name: within
        description: If ???within??? is set and the ???city??? or ???zipcode??? resolve
          to a specific geolocation, the search will be restricted to the specified
          within radius
      - in: query
        name: within_unit
        description: 'If within is set, you can specify the unit to use: ???M??? for
          miles, or ???K??? for kilometers'
      responses:
        200:
          description: OK
      tags:
      - event
      - search
definitions: []
x-collection-name: Eventbrite
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