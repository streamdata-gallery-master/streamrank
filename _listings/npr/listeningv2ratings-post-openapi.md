---
swagger: "2.0"
info:
  title: NPR One API Reference
  description: NPR One is a smart application that brings the best of NPR and Member
    Station programming, newscasts, podcasts, and stories together to create a new
    experience for listening. It provides an editor-curated and localized mobile listening
    experience based on the content the listener chooses, likes, shares, and enjoys.
    The API provides all of the content and customization in a simple, structured
    way that is easy for applicationdevelopers to implement.
  termsOfService: http://dev.npr.org/develop/terms-of-use
  contact:
    name: NPR One Enterprise Team
    url: http://dev.npr.org
    email: NPROneEnterprise@npr.org
  version: 1.0.0
host: api.npr.org
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /listening/v2/ratings:
    post:
      summary: Collect new ratings for media previously recommended to the logged-in
        user
      description: This endpoint is the main mechanism for providing feedback from
        the user to NPR about the recommendations that are obtained from `GET /listening/v2/recommendations`
      operationId: postRating
      x-api-path-slug: listeningv2ratings-post
      parameters:
      - in: body
        name: body
        description: A list of RatingData objects which contains data about ratings
          such as the id of the content, the rating value, elapsed time and more
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: recommend
        description: If set to `false`, this call will return a blank document; otherwise
          it will return a new recommendation object
      responses:
        200:
          description: OK
      tags:
      - news
      - listening
      - ratings
definitions:
  AbstractLink:
    properties:
      href:
        description: This is a default description.
        type: get
  AccessTokenData:
    properties:
      access_token:
        description: This is a default description.
        type: get
      expires_in:
        description: This is a default description.
        type: get
      refresh_token:
        description: This is a default description.
        type: get
      token_type:
        description: This is a default description.
        type: get
  AdTrackingData:
    properties:
      adId:
        description: This is a default description.
        type: get
      event:
        description: This is a default description.
        type: get
  AdXml:
    properties:
      id:
        description: This is a default description.
        type: get
  Affiliation:
    properties:
      daysSinceLastListen:
        description: This is a default description.
        type: get
      following:
        description: This is a default description.
        type: get
      href:
        description: This is a default description.
        type: get
      id:
        description: This is a default description.
        type: get
      notif_following:
        description: This is a default description.
        type: get
      notif_rated:
        description: This is a default description.
        type: get
      rating:
        description: This is a default description.
        type: get
      title:
        description: This is a default description.
        type: get
  AggregationData:
    properties:
      affiliation:
        description: This is a default description.
        type: get
      description:
        description: This is a default description.
        type: get
      station:
        description: This is a default description.
        type: get
      title:
        description: This is a default description.
        type: get
      type:
        description: This is a default description.
        type: get
  AggregationLinks:
    properties:
      image:
        description: This is a default description.
        type: get
      more:
        description: This is a default description.
        type: get
      web:
        description: This is a default description.
        type: get
  AudioItemData:
    properties:
      album:
        description: This is a default description.
        type: get
      artist:
        description: This is a default description.
        type: get
      audioTitle:
        description: This is a default description.
        type: get
      button:
        description: This is a default description.
        type: get
      date:
        description: This is a default description.
        type: get
      description:
        description: This is a default description.
        type: get
      duration:
        description: This is a default description.
        type: get
      expires:
        description: This is a default description.
        type: get
      label:
        description: This is a default description.
        type: get
      primary:
        description: This is a default description.
        type: get
  AudioItemLinks:
    properties:
      action:
        description: This is a default description.
        type: get
      audio:
        description: This is a default description.
        type: get
      image:
        description: This is a default description.
        type: get
      onramps:
        description: This is a default description.
        type: get
      recommendations:
        description: This is a default description.
        type: get
      up:
        description: This is a default description.
        type: get
      web:
        description: This is a default description.
        type: get
  Brand:
    properties:
      band:
        description: This is a default description.
        type: get
      call:
        description: This is a default description.
        type: get
      frequency:
        description: This is a default description.
        type: get
      marketCity:
        description: This is a default description.
        type: get
      marketState:
        description: This is a default description.
        type: get
      name:
        description: This is a default description.
        type: get
      tagline:
        description: This is a default description.
        type: get
  CategoryData:
    properties:
      displayType:
        description: This is a default description.
        type: get
      orgId:
        description: This is a default description.
        type: get
      title:
        description: This is a default description.
        type: get
      type:
        description: This is a default description.
        type: get
  CategoryLinks:
    properties:
      more:
        description: This is a default description.
        type: get
  ChannelData:
    properties:
      description:
        description: This is a default description.
        type: get
      displayType:
        description: This is a default description.
        type: get
      emptyText:
        description: This is a default description.
        type: get
      fullName:
        description: This is a default description.
        type: get
      id:
        description: This is a default description.
        type: get
      refreshRule:
        description: This is a default description.
        type: get
  ChannelsData:
    properties:
      defaultChannel:
        description: This is a default description.
        type: get
  Cohort:
    properties:
      directory:
        description: This is a default description.
        type: get
      id:
        description: This is a default description.
        type: get
      name:
        description: This is a default description.
        type: get
  CollectionDocument:
    properties:
      attributes:
        description: This is a default description.
        type: get
      errors:
        description: This is a default description.
        type: get
      href:
        description: This is a default description.
        type: get
      items:
        description: This is a default description.
        type: get
      links:
        description: This is a default description.
        type: get
      version:
        description: This is a default description.
        type: get
  CompanionXml:
    properties:
      CompanionClickThrough:
        description: This is a default description.
        type: get
      TrackingEvents:
        description: This is a default description.
        type: get
      height:
        description: This is a default description.
        type: get
      id:
        description: This is a default description.
        type: get
      width:
        description: This is a default description.
        type: get
  CreativeXml:
    properties:
      CompanionAds:
        description: This is a default description.
        type: get
      id:
        description: This is a default description.
        type: get
      sequence:
        description: This is a default description.
        type: get
  DAASTXml:
    properties:
      version:
        description: This is a default description.
        type: get
  DeviceCodeData:
    properties:
      device_code:
        description: This is a default description.
        type: get
      expires_in:
        description: This is a default description.
        type: get
      interval:
        description: This is a default description.
        type: get
      user_code:
        description: This is a default description.
        type: get
      verification_uri:
        description: This is a default description.
        type: get
  Error:
    properties:
      code:
        description: This is a default description.
        type: get
      debug:
        description: This is a default description.
        type: get
      text:
        description: This is a default description.
        type: get
  ErrorXmlDocument:
    properties:
      error:
        description: This is a default description.
        type: get
      version:
        description: This is a default description.
        type: get
  Geofence:
    properties:
      countries:
        description: This is a default description.
        type: get
      restricted:
        description: This is a default description.
        type: get
  HALDocument:
    properties:
      _links:
        description: This is a default description.
        type: get
  ImpressionXml:
    properties:
      id:
        description: This is a default description.
        type: get
  InLineXml:
    properties:
      AdSystem:
        description: This is a default description.
        type: get
      AdTitle:
        description: This is a default description.
        type: get
      Category:
        description: This is a default description.
        type: get
      Creatives:
        description: This is a default description.
        type: get
      Description:
        description: This is a default description.
        type: get
      Extensions:
        description: This is a default description.
        type: get
      Impression:
        description: This is a default description.
        type: get
  LinearXml:
    properties:
      Duration:
        description: This is a default description.
        type: get
      MediaFiles:
        description: This is a default description.
        type: get
      TrackingEvents:
        description: This is a default description.
        type: get
  MediaFileXml:
    properties:
      bitrate:
        description: This is a default description.
        type: get
      delivery:
        description: This is a default description.
        type: get
      type:
        description: This is a default description.
        type: get
  Organization:
    properties:
      call:
        description: This is a default description.
        type: get
      city:
        description: This is a default description.
        type: get
      displayName:
        description: This is a default description.
        type: get
      donationUrl:
        description: This is a default description.
        type: get
      id:
        description: This is a default description.
        type: get
      logo:
        description: This is a default description.
        type: get
      notif_org:
        description: This is a default description.
        type: get
      smallLogo:
        description: This is a default description.
        type: get
  OrganizationOverviewData:
    properties:
      home:
        description: This is a default description.
        type: get
      orgId:
        description: This is a default description.
        type: get
      type:
        description: This is a default description.
        type: get
  OrganizationOverviewLinks:
    properties:
      image:
        description: This is a default description.
        type: get
      related:
        description: This is a default description.
        type: get
      web:
        description: This is a default description.
        type: get
  RatingData:
    properties:
      affiliations:
        description: This is a default description.
        type: get
      channel:
        description: This is a default description.
        type: get
      cohort:
        description: This is a default description.
        type: get
      duration:
        description: This is a default description.
        type: get
      elapsed:
        description: This is a default description.
        type: get
      mediaId:
        description: This is a default description.
        type: get
      origin:
        description: This is a default description.
        type: get
      rating:
        description: This is a default description.
        type: get
      timestamp:
        description: This is a default description.
        type: get
  RecommendationOrganization:
    properties:
      donateUrl:
        description: This is a default description.
        type: get
      homepageUrl:
        description: This is a default description.
        type: get
      logoUrl:
        description: This is a default description.
        type: get
      name:
        description: This is a default description.
        type: get
  SearchItemDocument:
    properties:
      type:
        description: This is a default description.
        type: get
  SearchMetaData:
    properties:
      query:
        description: This is a default description.
        type: get
  SimpleError:
    properties:
      message:
        description: This is a default description.
        type: get
      type:
        description: This is a default description.
        type: get
  StaticResourceXml:
    properties:
      creativeType:
        description: This is a default description.
        type: get
  StationBrandData:
    properties:
      band:
        description: This is a default description.
        type: get
      call:
        description: This is a default description.
        type: get
      frequency:
        description: This is a default description.
        type: get
      marketCity:
        description: This is a default description.
        type: get
      marketState:
        description: This is a default description.
        type: get
      name:
        description: This is a default description.
        type: get
      tagline:
        description: This is a default description.
        type: get
  StationData:
    properties:
      guid:
        description: This is a default description.
        type: get
      orgId:
        description: This is a default description.
        type: get
  StationEligibilityData:
    properties:
      format:
        description: This is a default description.
        type: get
      musicOnly:
        description: This is a default description.
        type: get
      nprOne:
        description: This is a default description.
        type: get
      status:
        description: This is a default description.
        type: get
  StationLinks:
    properties:
      brand:
        description: This is a default description.
        type: get
      donation:
        description: This is a default description.
        type: get
      podcasts:
        description: This is a default description.
        type: get
      related:
        description: This is a default description.
        type: get
      streams:
        description: This is a default description.
        type: get
  StationNetworkData:
    properties:
      currentOrgId:
        description: This is a default description.
        type: get
      usesInheritance:
        description: This is a default description.
        type: get
  StationNetworkTierOneData:
    properties:
      id:
        description: This is a default description.
        type: get
      name:
        description: This is a default description.
        type: get
      status:
        description: This is a default description.
        type: get
      tier2:
        description: This is a default description.
        type: get
      usesInheritance:
        description: This is a default description.
        type: get
  StationNetworkTierThreeData:
    properties:
      id:
        description: This is a default description.
        type: get
      name:
        description: This is a default description.
        type: get
      usesInheritance:
        description: This is a default description.
        type: get
  StationNetworkTierTwoData:
    properties:
      id:
        description: This is a default description.
        type: get
      name:
        description: This is a default description.
        type: get
      tier3:
        description: This is a default description.
        type: get
      usesInheritance:
        description: This is a default description.
        type: get
  StationNewscastData:
    properties:
      id:
        description: This is a default description.
        type: get
      recency:
        description: This is a default description.
        type: get
  StationSearchMetaData:
    properties:
      city:
        description: This is a default description.
        type: get
      lat:
        description: This is a default description.
        type: get
      lon:
        description: This is a default description.
        type: get
      query:
        description: This is a default description.
        type: get
      state:
        description: This is a default description.
        type: get
  TrackingXml:
    properties:
      event:
        description: This is a default description.
        type: get
  UserAdData:
    properties:
      ipAddress:
        description: This is a default description.
        type: get
      listenerId:
        description: This is a default description.
        type: get
      userAgent:
        description: This is a default description.
        type: get
  UserData:
    properties:
      affiliations:
        description: This is a default description.
        type: get
      email:
        description: This is a default description.
        type: get
      firstName:
        description: This is a default description.
        type: get
      id:
        description: This is a default description.
        type: get
      lastName:
        description: This is a default description.
        type: get
      organizations:
        description: This is a default description.
        type: get
x-collection-name: NPR
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