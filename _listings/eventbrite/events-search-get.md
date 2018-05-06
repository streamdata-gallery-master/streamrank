---
swagger: "2.0"
info:
  title: Eventbrite
  description: The Eventbrite API is the best way to integrate and extend Eventbrite
    for your event or organising needs. Version 3 of the API brings you faster responses,
    consistent data types, more endpoints, and easier debugging and testing.
  version: 1.0.0
host: www.eventbriteapi.com
basePath: /v3
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /events/search/:
    get:
      summary: Get Events Search
      description: Allows you to retrieve a paginated response of public event objects
        from across Eventbrite?s directory, regardless of which user owns the event
      operationId: getEventsSearch
      parameters:
      - in: query
        name: categories
        description: Only return events under the given category IDs
        type: query
      - in: query
        name: date_modified.keyword
        description: Only return events with modified dates within the given keyword
          date range
        type: query
      - in: query
        name: date_modified.range_end
        description: Only return events with modified dates before the given UTC date
        type: query
      - in: query
        name: date_modified.range_start
        description: Only return events with modified dates after the given UTC date
        type: query
      - in: query
        name: formats
        description: Only return events with the given format IDs
        type: query
      - in: query
        name: high_affinity_categories
        description: Make search results prefer events in these categories
        type: query
      - in: query
        name: include_all_series_instances
        description: Boolean for whether or not you want to see all instances of repeating
          events in search results
        type: query
      - in: query
        name: include_unavailable_events
        description: Boolean for whether or not you want to see events without tickets
          on sale
        type: query
      - in: query
        name: incorporate_user_affinities
        description: Incorporate additional information from the user&#8217;s historic
          preferences
        type: query
      - in: query
        name: location.address
        description: The address of the location you want to search for events around
        type: query
      - in: query
        name: location.latitude
        description: The latitude of of the location you want to search for events
          around
        type: query
      - in: query
        name: location.longitude
        description: The longitude of the location you want to search for events around
        type: query
      - in: query
        name: location.viewport.northeast.latitude
        description: The latitude of the northeast corner of a viewport
        type: query
      - in: query
        name: location.viewport.northeast.longitude
        description: The longitude of the northeast corner of a viewport
        type: query
      - in: query
        name: location.viewport.southwest.latitude
        description: The latitude of the southwest corner of a viewport
        type: query
      - in: query
        name: location.viewport.southwest.longitude
        description: The longitude of the southwest corner of a viewport
        type: query
      - in: query
        name: location.within
        description: The distance you want to search around the given location
        type: query
      - in: query
        name: organizer.id
        description: Only return events organized by the given Organizer ID
        type: query
      - in: query
        name: price
        description: Only return events that are &#8220;free&#8221; or &#8220;paid&#8221;
        type: query
      - in: query
        name: q
        description: Return events matching the given keywords
      - in: query
        name: search_type
        description: Use the preconfigured settings for this type of search - Current
          option is &#8220;promoted&#8221;
        type: query
      - in: query
        name: sort_by
        description: Parameter you want to sort by - options are &#8220;date&#8221;,
          &#8220;distance&#8221; and &#8220;best&#8221;
        type: query
      - in: query
        name: start_date.keyword
        description: Only return events with start dates within the given keyword
          date range
        type: query
      - in: query
        name: start_date.range_end
        description: Only return events with start dates before the given date
        type: query
      - in: query
        name: start_date.range_start
        description: Only return events with start dates after the given date
        type: query
      - in: query
        name: subcategories
        description: Only return events under the given subcategory IDs
        type: query
      - in: query
        name: tracking_code
        description: Append the given tracking_code to the event URLs returned
        type: query
      - in: query
        name: user.id
        description: Only return events owned by the given User ID
        type: query
      responses:
        200:
          description: OK
      tags:
      - events
      - search
definitions: []
x-collection-name: Eventbrite
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