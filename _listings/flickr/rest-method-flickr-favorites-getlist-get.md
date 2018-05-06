---
swagger: "2.0"
info:
  title: Flickr API Schema
  description: A subset of Flickr's API defined in Swagger format.
  termsOfService: https://www.flickr.com/services/api/tos/
  version: 1.0.0
host: api.flickr.com
basePath: /services
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /rest?method=flickr.favorites.getList:
    get:
      summary: Get Favorite List
      description: Returns a list of the user's favorite photos
      operationId: getFavoritesByPersonID
      parameters:
      - in: query
        name: api_key
      - in: query
        name: max_fave_date
      - in: query
        name: min_fave_date
      - in: query
        name: page
      - in: query
        name: per_page
      - in: query
        name: user_id
      responses:
        200:
          description: OK
      tags:
      - photos
      - favorites
definitions:
  ContextPhoto:
    properties:
      id:
        description: This is a default description.
        type: post
      secret:
        description: This is a default description.
        type: post
      server:
        description: This is a default description.
        type: post
      farm:
        description: This is a default description.
        type: post
      title:
        description: This is a default description.
        type: post
      url:
        description: This is a default description.
        type: post
      thumb:
        description: This is a default description.
        type: post
      media:
        description: This is a default description.
        type: post
      owner:
        description: This is a default description.
        type: post
      license:
        description: This is a default description.
        type: post
  ContextPhotos:
    properties:
      photos:
        description: This is a default description.
        type: post
  Cover:
    properties:
      id:
        description: This is a default description.
        type: post
      owner:
        description: This is a default description.
        type: post
      secret:
        description: This is a default description.
        type: post
      server:
        description: This is a default description.
        type: post
      farm:
        description: This is a default description.
        type: post
      title:
        description: This is a default description.
        type: post
      ispublic:
        description: This is a default description.
        type: post
      isfriend:
        description: This is a default description.
        type: post
      isfamily:
        description: This is a default description.
        type: post
      "y":
        description: This is a default description.
        type: post
  Group:
    properties:
      id:
        description: This is a default description.
        type: post
      path_alias:
        description: This is a default description.
        type: post
      iconserver:
        description: This is a default description.
        type: post
      iconfarm:
        description: This is a default description.
        type: post
      name:
        description: This is a default description.
        type: post
      description:
        description: This is a default description.
        type: post
      rules:
        description: This is a default description.
        type: post
      members:
        description: This is a default description.
        type: post
      pool_count:
        description: This is a default description.
        type: post
      topic_count:
        description: This is a default description.
        type: post
  Note:
    properties:
      description:
        description: This is a default description.
        type: post
  Owner:
    properties:
      nsid:
        description: This is a default description.
        type: post
      username:
        description: This is a default description.
        type: post
      realname:
        description: This is a default description.
        type: post
      location:
        description: This is a default description.
        type: post
      iconserver:
        description: This is a default description.
        type: post
      iconfarm:
        description: This is a default description.
        type: post
      path_alias:
        description: This is a default description.
        type: post
      noindexfollow:
        description: This is a default description.
        type: post
      ispro:
        description: This is a default description.
        type: post
      is_ad_free:
        description: This is a default description.
        type: post
  Person:
    properties:
      id:
        description: This is a default description.
        type: post
      nsid:
        description: This is a default description.
        type: post
      ispro:
        description: This is a default description.
        type: post
      can_buy_pro:
        description: This is a default description.
        type: post
      iconserver:
        description: This is a default description.
        type: post
      iconfarm:
        description: This is a default description.
        type: post
      path_alias:
        description: This is a default description.
        type: post
      has_stats:
        description: This is a default description.
        type: post
      coverphoto_server:
        description: This is a default description.
        type: post
      coverphoto_farm:
        description: This is a default description.
        type: post
  Photo:
    properties:
      id:
        description: This is a default description.
        type: post
      secret:
        description: This is a default description.
        type: post
      server:
        description: This is a default description.
        type: post
      farm:
        description: This is a default description.
        type: post
      dateuploaded:
        description: This is a default description.
        type: post
      isfavorite:
        description: This is a default description.
        type: post
      license:
        description: This is a default description.
        type: post
      safety_level:
        description: This is a default description.
        type: post
      rotation:
        description: This is a default description.
        type: post
      originalsecret:
        description: This is a default description.
        type: post
  PhotoURLs:
    properties:
      h:
        description: This is a default description.
        type: post
      l:
        description: This is a default description.
        type: post
      s:
        description: This is a default description.
        type: post
      t:
        description: This is a default description.
        type: post
  Tag:
    properties:
      id:
        description: This is a default description.
        type: post
      author:
        description: This is a default description.
        type: post
      authorname:
        description: This is a default description.
        type: post
      raw:
        description: This is a default description.
        type: post
      _content:
        description: This is a default description.
        type: post
      machine_tag:
        description: This is a default description.
        type: post
  Topic:
    properties:
      id:
        description: This is a default description.
        type: post
      subject:
        description: This is a default description.
        type: post
      message:
        description: This is a default description.
        type: post
      author:
        description: This is a default description.
        type: post
      authorname:
        description: This is a default description.
        type: post
      author_path_alias:
        description: This is a default description.
        type: post
      author_is_deleted:
        description: This is a default description.
        type: post
      is_pro:
        description: This is a default description.
        type: post
      role:
        description: This is a default description.
        type: post
      iconserver:
        description: This is a default description.
        type: post
  TopicReply:
    properties:
      id:
        description: This is a default description.
        type: post
      message:
        description: This is a default description.
        type: post
      author:
        description: This is a default description.
        type: post
      authorname:
        description: This is a default description.
        type: post
      author_path_alias:
        description: This is a default description.
        type: post
      author_is_deleted:
        description: This is a default description.
        type: post
      is_pro:
        description: This is a default description.
        type: post
      iconserver:
        description: This is a default description.
        type: post
      iconfarm:
        description: This is a default description.
        type: post
      can_edit:
        description: This is a default description.
        type: post
  URL:
    properties:
      type:
        description: This is a default description.
        type: post
      _content:
        description: This is a default description.
        type: post
  Album:
    properties:
      id:
        description: This is a default description.
        type: post
      primary:
        description: This is a default description.
        type: post
      secret:
        description: This is a default description.
        type: post
      server:
        description: This is a default description.
        type: post
      farm:
        description: This is a default description.
        type: post
      photos:
        description: This is a default description.
        type: post
      videos:
        description: This is a default description.
        type: post
      count_views:
        description: This is a default description.
        type: post
      count_comments:
        description: This is a default description.
        type: post
      can_comment:
        description: This is a default description.
        type: post
  Size:
    properties:
      label:
        description: This is a default description.
        type: get
      width:
        description: This is a default description.
        type: get
      height:
        description: This is a default description.
        type: get
      source:
        description: This is a default description.
        type: get
      url:
        description: This is a default description.
        type: get
      media:
        description: This is a default description.
        type: get
x-collection-name: Flickr
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