---
swagger: "2.0"
info:
  title: Uber
  description: Using the Uber API, developers can integrate the power of Uber into
    3rd party applications. Calls to the API can be made to request information on
    available car types, driver location expressed in geo-coordinates, time estimates,
    estimated prices (including currency conversion when applicable), as well as user
    account history and activity. The Uber API documentation describes deep linking
    techniques to programmatically launch the native app from iOS or Android, or the
    Uber mobile site from mobile web. The API comes with a detailed style guide and
    asset package for implementing licensed brandings. The Uber API Affiliate program
    grants cash and issues Uber credits for new user onboarding through a 3rd party
    app.
  version: 1.0.0
host: api.uber.com
basePath: /v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /estimates/price:
    get:
      summary: Price Estimates
      description: The Price Estimates endpoint returns an estimated price range for
        each product offered at a given location
      operationId: the-price-estimates-endpoint-returns-an-estimated-price-range-for-each-product-offered-at-a-given-lo
      parameters:
      - in: query
        name: end_latitude
        description: Latitude component of end location
      - in: query
        name: end_longitude
        description: Longitude component of end location
      - in: query
        name: start_latitude
        description: Latitude component of start location
      - in: query
        name: start_longitude
        description: Longitude component of start location
      responses:
        200:
          description: OK
      tags:
      - transportation
definitions:
  Product:
    properties:
      product_id:
        description: This is a default description.
        type: get
      description:
        description: This is a default description.
        type: get
      display_name:
        description: This is a default description.
        type: get
      capacity:
        description: This is a default description.
        type: get
      image:
        description: This is a default description.
        type: get
  ProductList:
    properties:
      products:
        description: This is a default description.
        type: get
  PriceEstimate:
    properties:
      product_id:
        description: This is a default description.
        type: get
      currency_code:
        description: This is a default description.
        type: get
      display_name:
        description: This is a default description.
        type: get
      estimate:
        description: This is a default description.
        type: get
      low_estimate:
        description: This is a default description.
        type: get
      high_estimate:
        description: This is a default description.
        type: get
      surge_multiplier:
        description: This is a default description.
        type: get
  Profile:
    properties:
      first_name:
        description: This is a default description.
        type: get
      last_name:
        description: This is a default description.
        type: get
      email:
        description: This is a default description.
        type: get
      picture:
        description: This is a default description.
        type: get
      promo_code:
        description: This is a default description.
        type: get
  Activity:
    properties:
      uuid:
        description: This is a default description.
        type: get
  Activities:
    properties:
      offset:
        description: This is a default description.
        type: get
      limit:
        description: This is a default description.
        type: get
      count:
        description: This is a default description.
        type: get
      history:
        description: This is a default description.
        type: get
  Error:
    properties:
      code:
        description: This is a default description.
        type: get
      message:
        description: This is a default description.
        type: get
      fields:
        description: This is a default description.
        type: get
x-collection-name: Uber
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