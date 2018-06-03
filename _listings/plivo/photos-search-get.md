---
swagger: "2.0"
info:
  title: Codenvy Account API
  description: This is the API for managing Codenvy account.
  version: 1.0.0
host: /account
basePath: https://codenvy.com/api
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /photos/search:
    get:
      summary: Get Photos Search
      description: Returns a listing of twenty (up to one hundred) photos from search
        results for a specified tag, keyword, or location
      operationId: returns-a-listing-of-twenty-up-to-one-hundred-photos-from-search-results-for-a-specified-tag-keyword
      parameters:
      - in: query
        name: comments_count u2014u00a0Sort by the number of comments, most commented
          first.
      - in: query
        name: created_at
        description: 'Default: sort by time of upload, most recent first'
      - in: query
        name: exclude
        description: String name of the category to exclude from the results
      - in: query
        name: favorites_count
        description: Sort by the number of favorites, most favorited first
      - in: query
        name: geo
        description: A geo-location point of the format latitude,longitude,radius&lt;units&gt;
      - in: query
        name: highest_rating
        description: Sort by highest rating achieved, highest rated first
      - in: query
        name: image_size
        description: The photo size to be returned
      - in: query
        name: 'license_type -- Restrict the results to one or more license types.  Multiple
          types can be separated with a comma: license_type=1,4.'
      - in: query
        name: only
        description: String name of the category to return photos from
      - in: query
        name: page
        description: Return a specific page
      - in: query
        name: rating
        description: Sort by current rating, highest rated first
      - in: query
        name: rpp
        description: The number of results to return
      - in: query
        name: sort u2014u00a0Sort photos in the specified order. The following values
          are recognized:nnnn_score
        description: Sort by query score, best match first
      - in: query
        name: tag
        description: A complete tag string to search for
      - in: query
        name: tags
        description: Returns an array of tags for each photo
      - in: query
        name: taken_at u2014u00a0Sort by the original date of the image extracted
          from metadata, most recent first (might not be available for all images).
      - in: query
        name: term
        description: A keyword to search for
      - in: query
        name: times_viewed u2014u00a0Sort by the number of views, most viewed first.
      - in: query
        name: votes_count u2013 Sort by the number of votes, most voted on first.
      responses:
        200:
          description: OK
      tags:
      - photos
      - search
definitions:
  AccountUpdate:
    properties:
      name:
        description: This is a default description.
        type: string
      attributes:
        description: This is a default description.
        type: string
  MemberDescriptor:
    properties:
      links:
        description: This is a default description.
        type: string
      userId:
        description: This is a default description.
        type: string
      accountReference:
        description: This is a default description.
        type: string
      roles:
        description: This is a default description.
        type: string
  RequestBodyDescriptor:
    properties:
      description:
        description: This is a default description.
        type: string
  UpdateResourcesDescriptor:
    properties:
      workspaceId:
        description: This is a default description.
        type: string
      runnerRam:
        description: This is a default description.
        type: string
      builderTimeout:
        description: This is a default description.
        type: string
      runnerTimeout:
        description: This is a default description.
        type: string
      resourcesUsageLimit:
        description: This is a default description.
        type: string
  NewMembership:
    properties:
      userId:
        description: This is a default description.
        type: string
      roles:
        description: This is a default description.
        type: string
  LinkParameter:
    properties:
      required:
        description: This is a default description.
        type: string
      valid:
        description: This is a default description.
        type: string
      description:
        description: This is a default description.
        type: string
      name:
        description: This is a default description.
        type: string
      type:
        description: This is a default description.
        type: string
      defaultValue:
        description: This is a default description.
        type: string
  SubscriptionDescriptor:
    properties:
      accountId:
        description: This is a default description.
        type: string
      startDate:
        description: This is a default description.
        type: string
      endDate:
        description: This is a default description.
        type: string
      links:
        description: This is a default description.
        type: string
      planId:
        description: This is a default description.
        type: string
      usePaymentSystem:
        description: This is a default description.
        type: string
      serviceId:
        description: This is a default description.
        type: string
      billingCycleType:
        description: This is a default description.
        type: string
      billingCycle:
        description: This is a default description.
        type: string
      billingContractTerm:
        description: This is a default description.
        type: string
  AccountDescriptor:
    properties:
      links:
        description: This is a default description.
        type: string
      name:
        description: This is a default description.
        type: string
      id:
        description: This is a default description.
        type: string
      attributes:
        description: This is a default description.
        type: string
  AccountReference:
    properties:
      links:
        description: This is a default description.
        type: string
      name:
        description: This is a default description.
        type: string
      id:
        description: This is a default description.
        type: string
  NewSubscription:
    properties:
      accountId:
        description: This is a default description.
        type: string
      planId:
        description: This is a default description.
        type: string
      usePaymentSystem:
        description: This is a default description.
        type: string
      trialDuration:
        description: This is a default description.
        type: string
      properties:
        description: This is a default description.
        type: string
  NewAccount:
    properties:
      name:
        description: This is a default description.
        type: string
      attributes:
        description: This is a default description.
        type: string
  Link:
    properties:
      rel:
        description: This is a default description.
        type: string
      href:
        description: This is a default description.
        type: string
      produces:
        description: This is a default description.
        type: string
      consumes:
        description: This is a default description.
        type: string
      requestBody:
        description: This is a default description.
        type: string
      method:
        description: This is a default description.
        type: string
      parameters:
        description: This is a default description.
        type: string
  Account:
    properties:
      id:
        description: This is a default description.
        type: string
      name:
        description: This is a default description.
        type: string
      attributes:
        description: This is a default description.
        type: string
x-collection-name: Plivo
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