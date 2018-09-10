---
swagger: "2.0"
info:
  title: Tolls API
  description: 'The Tolls API is a read-only service to answer questions about theprices
    and locations of toll roads.Some tolls are charged at _single points_, so you
    pay them when you cross atoll gate or pass a toll booth. Other tolls are _distance-based_:
    the amountthat you pay depends on where you enter a toll road and also where youexit.
    Some toll roads charge different prices by _time of day_, and some aretotally
    _dynamic_, changing their price depending on demand at a given time.Note that
    while we support distance based tolls that are applied using tollgates or booths,
    we currently do not support mileage-based user fees thatare assessed based on
    odometer readings.We provide toll information in four different ways:  * We can
    tell you how much you will pay based on your trip''s GPS trajectory.    To find
    this out, use the [/gps_trace](#reference/0/tolls-on-a-gps-trace) POST request.  *
    We can tell you how much you will pay to drive a given route.    To find this
    out, use the [/route](#reference/0/tolls-on-a-route) POST request.  * We can tell
    you the full payment details of all the toll locations in    an area, using the
    [/toll](#reference/0/tolls-in-an-area) GET request.  * We can tell you the payment
    details of a single toll location,    using the [/toll/{id}](#reference/0/toll-details)
    GET request.In all four cases, we can return multiple costs for a single toll.
    This is becausethe amount a user pays can depend on the kind of vehicle, the occupancy,
    and thepayment method. To figure out how much a particular user pays, you must
    know therequisite information about them and find the matching cost.For more information
    about how the Tolls API can be used see the &lt;a href=&quot;https://coord.co/quickstart/tolls&quot;
    target=&quot;_blank&quot;&gt;Toll Guide&lt;/a&gt;.'
  version: 1.0.0
host: api.coord.co
basePath: /v1/search/tolling
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /toll:
    get:
      summary: Get all tolls in an area defined by a center location and a radius
      description: Returns information on all tolls within a given radius
      operationId: details_by_area
      x-api-path-slug: toll-get
      parameters:
      - in: query
        name: access_key
        description: The API access key for the request
      - in: query
        name: latitude
        description: Latitude to return results for
      - in: query
        name: longitude
        description: Longitude to return results for
      - in: query
        name: radius_km
        description: |-
          Distance, in kilometers, from (`latitude`, `longitude`) we will return
          results for
      - in: query
        name: return_geometry
        description: |
          Should we return geometry in the response?
      - in: query
        name: return_price
        description: |
          Should we return prices in the response?
      responses:
        200:
          description: OK
      tags:
      - tolls
definitions:
  BikeLocationFeature:
    properties:
      id:
        description: This is a default description.
        type: x-summary
      type:
        description: This is a default description.
        type: x-summary
  BikeLocationFeatureProperties:
    properties:
      is_renting:
        description: This is a default description.
        type: x-summary
      is_returning:
        description: This is a default description.
        type: x-summary
      last_reported:
        description: This is a default description.
        type: x-summary
      lat:
        description: This is a default description.
        type: x-summary
      location_id:
        description: This is a default description.
        type: x-summary
      lon:
        description: This is a default description.
        type: x-summary
      name:
        description: This is a default description.
        type: x-summary
      num_bikes_available:
        description: This is a default description.
        type: x-summary
      num_docks_available:
        description: This is a default description.
        type: x-summary
      region_id:
        description: This is a default description.
        type: x-summary
  BikeLocationList:
    properties:
      features:
        description: This is a default description.
        type: x-summary
      type:
        description: This is a default description.
        type: x-summary
  Error:
    properties:
      code:
        description: This is a default description.
        type: x-summary
      message:
        description: This is a default description.
        type: x-summary
  GeoJsonLineString:
    properties:
      coordinates:
        description: This is a default description.
        type: x-summary
      type:
        description: This is a default description.
        type: x-summary
  LatLng:
    properties:
      lat:
        description: This is a default description.
        type: x-summary
      lng:
        description: This is a default description.
        type: x-summary
  LineString:
    properties:
      coordinates:
        description: This is a default description.
        type: x-summary
      type:
        description: This is a default description.
        type: x-summary
  Money:
    properties:
      amount:
        description: This is a default description.
        type: x-summary
      currency:
        description: This is a default description.
        type: x-summary
  MultiPolygonGeometry:
    properties:
      coordinates:
        description: This is a default description.
        type: x-summary
      type:
        description: This is a default description.
        type: x-summary
  NamedLocation:
    properties:
      name:
        description: This is a default description.
        type: x-summary
  ParkingCondition:
    properties:
      absolute_time_end_ts:
        description: This is a default description.
        type: x-summary
      absolute_time_start_ts:
        description: This is a default description.
        type: x-summary
      day_times:
        description: This is a default description.
        type: x-summary
      id:
        description: This is a default description.
        type: x-summary
  ParkingLocationMetadata:
    properties:
      address:
        description: This is a default description.
        type: x-summary
      amenities:
        description: This is a default description.
        type: x-summary
      created:
        description: This is a default description.
        type: x-summary
      id:
        description: This is a default description.
        type: x-summary
      last_updated:
        description: This is a default description.
        type: x-summary
      name:
        description: This is a default description.
        type: x-summary
      online_access_type:
        description: This is a default description.
        type: x-summary
      operator_name:
        description: This is a default description.
        type: x-summary
      time_zone:
        description: This is a default description.
        type: x-summary
  ParkingRate:
    properties:
      absolute_end_time:
        description: This is a default description.
        type: x-summary
      absolute_start_time:
        description: This is a default description.
        type: x-summary
      arrival_window_end:
        description: This is a default description.
        type: x-summary
      arrival_window_start:
        description: This is a default description.
        type: x-summary
      days:
        description: This is a default description.
        type: x-summary
      departure_window_end:
        description: This is a default description.
        type: x-summary
      departure_window_start:
        description: This is a default description.
        type: x-summary
      max_duration_m:
        description: This is a default description.
        type: x-summary
      name:
        description: This is a default description.
        type: x-summary
      rate_type:
        description: This is a default description.
        type: x-summary
  ParkingRule:
    properties:
      price_mechanism:
        description: This is a default description.
        type: x-summary
      prices:
        description: This is a default description.
        type: x-summary
      spaces_total:
        description: This is a default description.
        type: x-summary
  ParkingSession:
    properties:
      billing_info:
        description: This is a default description.
        type: x-summary
      end_time:
        description: This is a default description.
        type: x-summary
      id:
        description: This is a default description.
        type: x-summary
      location_id:
        description: This is a default description.
        type: x-summary
      resource_id:
        description: This is a default description.
        type: x-summary
      start_time:
        description: This is a default description.
        type: x-summary
      user_id:
        description: This is a default description.
        type: x-summary
  Partner:
    properties:
      api_access_enabled:
        description: This is a default description.
        type: x-summary
      api_keys:
        description: This is a default description.
        type: x-summary
      creation_time:
        description: This is a default description.
        type: x-summary
      first_login_time:
        description: This is a default description.
        type: x-summary
      id:
        description: This is a default description.
        type: x-summary
      is_provider:
        description: This is a default description.
        type: x-summary
      name:
        description: This is a default description.
        type: x-summary
      prod_enabled:
        description: This is a default description.
        type: x-summary
      secret_keys:
        description: This is a default description.
        type: x-summary
      whitelisted_domains:
        description: This is a default description.
        type: x-summary
  PaymentMethod:
    properties:
      detail_url:
        description: This is a default description.
        type: x-summary
      details:
        description: This is a default description.
        type: x-summary
      issuing_agency:
        description: This is a default description.
        type: x-summary
      type:
        description: This is a default description.
        type: x-summary
  Plate:
    properties:
      state:
        description: This is a default description.
        type: x-summary
      text:
        description: This is a default description.
        type: x-summary
  PointGeometry:
    properties:
      coordinates:
        description: This is a default description.
        type: x-summary
      type:
        description: This is a default description.
        type: x-summary
  PricingRule:
    properties:
      end_duration_h:
        description: This is a default description.
        type: x-summary
      minimum_hours_paid:
        description: This is a default description.
        type: x-summary
      start_duration_h:
        description: This is a default description.
        type: x-summary
  RedemptionInfo:
    properties:
      barcode:
        description: This is a default description.
        type: x-summary
  Reservation:
    properties:
      duration_m:
        description: This is a default description.
        type: x-summary
      id:
        description: This is a default description.
        type: x-summary
      lease_expiration_time:
        description: This is a default description.
        type: x-summary
      plate:
        description: This is a default description.
        type: x-summary
      resource_id:
        description: This is a default description.
        type: x-summary
      start_time:
        description: This is a default description.
        type: x-summary
      status:
        description: This is a default description.
        type: x-summary
      user_id:
        description: This is a default description.
        type: x-summary
      vehicle_id:
        description: This is a default description.
        type: x-summary
  Route:
    properties:
      departure_time:
        description: This is a default description.
        type: x-summary
      steps:
        description: This is a default description.
        type: x-summary
  RouteStep:
    properties:
      duration_s:
        description: This is a default description.
        type: x-summary
      encoded_polyline:
        description: This is a default description.
        type: x-summary
      polyline:
        description: This is a default description.
        type: x-summary
      road_name:
        description: This is a default description.
        type: x-summary
  RouteToll:
    properties:
      checkpoints:
        description: This is a default description.
        type: x-summary
      dynamic:
        description: This is a default description.
        type: x-summary
      estimated_cross_time:
        description: This is a default description.
        type: x-summary
      id:
        description: This is a default description.
        type: x-summary
      name:
        description: This is a default description.
        type: x-summary
      optional:
        description: This is a default description.
        type: x-summary
      prices:
        description: This is a default description.
        type: x-summary
      roadway_name:
        description: This is a default description.
        type: x-summary
  TimeAndDay:
    properties:
      day_of_year_end:
        description: This is a default description.
        type: x-summary
      day_of_year_start:
        description: This is a default description.
        type: x-summary
      days:
        description: This is a default description.
        type: x-summary
      time_of_day_end:
        description: This is a default description.
        type: x-summary
      time_of_day_start:
        description: This is a default description.
        type: x-summary
  TimeRange:
    properties:
      max_value:
        description: This is a default description.
        type: x-summary
      min_value:
        description: This is a default description.
        type: x-summary
  TimestampedLatLng:
    properties:
      lat:
        description: This is a default description.
        type: x-summary
      lng:
        description: This is a default description.
        type: x-summary
      timestamp:
        description: This is a default description.
        type: x-summary
  Toll:
    properties:
      geometry:
        description: This is a default description.
        type: x-summary
      id:
        description: This is a default description.
        type: x-summary
      name:
        description: This is a default description.
        type: x-summary
      optional:
        description: This is a default description.
        type: x-summary
      permanently_closed:
        description: This is a default description.
        type: x-summary
      roadway_access_schedule:
        description: This is a default description.
        type: x-summary
      roadway_name:
        description: This is a default description.
        type: x-summary
      segments:
        description: This is a default description.
        type: x-summary
      time_zone:
        description: This is a default description.
        type: x-summary
  TollByTraceRequest:
    properties:
      locations:
        description: This is a default description.
        type: x-summary
  TollCheckPoint:
    properties: []
  TollRule:
    properties:
      not_allowed:
        description: This is a default description.
        type: x-summary
  TollSchedule:
    properties:
      day_of_year_end:
        description: This is a default description.
        type: x-summary
      day_of_year_start:
        description: This is a default description.
        type: x-summary
      days_of_week:
        description: This is a default description.
        type: x-summary
      dynamic:
        description: This is a default description.
        type: x-summary
      prices:
        description: This is a default description.
        type: x-summary
      time_end:
        description: This is a default description.
        type: x-summary
      time_start:
        description: This is a default description.
        type: x-summary
  TollSegment:
    properties:
      checkpoints:
        description: This is a default description.
        type: x-summary
      pricing:
        description: This is a default description.
        type: x-summary
  TransactionRequirements:
    properties:
      jwt_claims:
        description: This is a default description.
        type: x-summary
      linked_account:
        description: This is a default description.
        type: x-summary
      users_api_fields:
        description: This is a default description.
        type: x-summary
  Vehicle:
    properties:
      license_plate:
        description: This is a default description.
        type: x-summary
  VehicleType:
    properties:
      axles:
        description: This is a default description.
        type: x-summary
      detail_url:
        description: This is a default description.
        type: x-summary
      details:
        description: This is a default description.
        type: x-summary
      min_occupancy:
        description: This is a default description.
        type: x-summary
      motorcycle:
        description: This is a default description.
        type: x-summary
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