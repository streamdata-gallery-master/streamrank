---
swagger: "2.0"
info:
  title: Twitter
  description: The Twitter API gives you programmatic control over any Twitter account,
    and most aspect of the platform. Allowing developers to build social applications
    that use the platform, and automate interactions between users.
  version: "1.1"
host: api.twitter.com
basePath: /1.1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /trends/available.json:
    get:
      summary: Show Available Trends
      description: Returns the availability
      operationId: returns-the-availability
      responses:
        200:
          description: OK
      tags:
      - social
      - trends
definitions:
  Tweets:
    properties:
      contributors:
        description: This is a default description.
        type: string
      created_at:
        description: This is a default description.
        type: string
      favorite_count:
        description: This is a default description.
        type: string
      favorited:
        description: This is a default description.
        type: string
      filter_level:
        description: This is a default description.
        type: string
      id:
        description: This is a default description.
        type: string
      id_str:
        description: This is a default description.
        type: string
      in_reply_to_screen_name:
        description: This is a default description.
        type: string
      in_reply_to_status_id:
        description: This is a default description.
        type: string
      in_reply_to_status_id_str:
        description: This is a default description.
        type: string
  Contributors:
    properties:
      id:
        description: This is a default description.
        type: string
      id_str:
        description: This is a default description.
        type: string
      screen_name:
        description: This is a default description.
        type: string
  Coordinates:
    properties:
      coordinates:
        description: This is a default description.
        type: string
      type:
        description: This is a default description.
        type: string
  Users:
    properties:
      contributors_enabled:
        description: This is a default description.
        type: string
      created_at:
        description: This is a default description.
        type: string
      default_profile:
        description: This is a default description.
        type: string
      default_profile_image:
        description: This is a default description.
        type: string
      description:
        description: This is a default description.
        type: string
      favorites_count:
        description: This is a default description.
        type: string
      follow_request_sent:
        description: This is a default description.
        type: string
      following:
        description: This is a default description.
        type: string
      followers_count:
        description: This is a default description.
        type: string
      friends_count:
        description: This is a default description.
        type: string
  Entities:
    properties:
      hashtags:
        description: This is a default description.
        type: string
      media:
        description: This is a default description.
        type: string
      urls:
        description: This is a default description.
        type: string
      user_mentions:
        description: This is a default description.
        type: string
  Hashtags:
    properties:
      indices:
        description: This is a default description.
        type: string
      text:
        description: This is a default description.
        type: string
  Media:
    properties:
      display_url:
        description: This is a default description.
        type: string
      expanded_url:
        description: This is a default description.
        type: string
      id:
        description: This is a default description.
        type: string
      id_str:
        description: This is a default description.
        type: string
      indices:
        description: This is a default description.
        type: string
      media_url:
        description: This is a default description.
        type: string
      media_url_https:
        description: This is a default description.
        type: string
      source_status_id:
        description: This is a default description.
        type: string
      source_status_id_str:
        description: This is a default description.
        type: string
      type:
        description: This is a default description.
        type: string
  Size:
    properties:
      h:
        description: This is a default description.
        type: string
      resize:
        description: This is a default description.
        type: string
      w:
        description: This is a default description.
        type: string
  Sizes:
    properties: []
  URL:
    properties:
      display_url:
        description: This is a default description.
        type: string
      expanded_url:
        description: This is a default description.
        type: string
      indices:
        description: This is a default description.
        type: string
      url:
        description: This is a default description.
        type: string
  User_Mention:
    properties:
      id:
        description: This is a default description.
        type: string
      id_str:
        description: This is a default description.
        type: string
      indices:
        description: This is a default description.
        type: string
      name:
        description: This is a default description.
        type: string
      screen_name:
        description: This is a default description.
        type: string
  Places:
    properties:
      attributes:
        description: This is a default description.
        type: string
      country:
        description: This is a default description.
        type: string
      country_code:
        description: This is a default description.
        type: string
      full_name:
        description: This is a default description.
        type: string
      id:
        description: This is a default description.
        type: string
      name:
        description: This is a default description.
        type: string
      place_type:
        description: This is a default description.
        type: string
      url:
        description: This is a default description.
        type: string
  Bounding_box:
    properties:
      coordinates:
        description: This is a default description.
        type: string
      type:
        description: This is a default description.
        type: string
  Lists:
    properties:
      created_at:
        description: This is a default description.
        type: string
      slug:
        description: This is a default description.
        type: string
      name:
        description: This is a default description.
        type: string
      description:
        description: This is a default description.
        type: string
      mode:
        description: This is a default description.
        type: string
      following:
        description: This is a default description.
        type: string
      member_count:
        description: This is a default description.
        type: string
      id_str:
        description: This is a default description.
        type: string
      subscriber_count:
        description: This is a default description.
        type: string
      id:
        description: This is a default description.
        type: string
  Cursor_lists:
    properties:
      previous_cursor:
        description: This is a default description.
        type: string
      lists:
        description: This is a default description.
        type: string
      previous_cursor_str:
        description: This is a default description.
        type: string
      next_cursor:
        description: This is a default description.
        type: string
      next_cursor_str:
        description: This is a default description.
        type: string
  Cursor_users:
    properties:
      previous_cursor:
        description: This is a default description.
        type: string
      users:
        description: This is a default description.
        type: string
      previous_cursor_str:
        description: This is a default description.
        type: string
      next_cursor:
        description: This is a default description.
        type: string
      next_cursor_str:
        description: This is a default description.
        type: string
  Cursor_ids:
    properties:
      previous_cursor:
        description: This is a default description.
        type: string
      users:
        description: This is a default description.
        type: string
      previous_cursor_str:
        description: This is a default description.
        type: string
      next_cursor:
        description: This is a default description.
        type: string
      next_cursor_str:
        description: This is a default description.
        type: string
  Messages:
    properties:
      created_at:
        description: This is a default description.
        type: string
      id:
        description: This is a default description.
        type: string
      id_string:
        description: This is a default description.
        type: string
      recipient_id:
        description: This is a default description.
        type: string
      recipient_screen_name:
        description: This is a default description.
        type: string
      sender_id:
        description: This is a default description.
        type: string
      sender_screen_name:
        description: This is a default description.
        type: string
      text:
        description: This is a default description.
        type: string
  Query:
    properties:
      created_at:
        description: This is a default description.
        type: string
      id:
        description: This is a default description.
        type: string
      id_str:
        description: This is a default description.
        type: string
      name:
        description: This is a default description.
        type: string
      position:
        description: This is a default description.
        type: string
      query:
        description: This is a default description.
        type: string
  Friendship:
    properties: []
  Targets:
    properties: []
  Target:
    properties:
      id_str:
        description: This is a default description.
        type: string
      id:
        description: This is a default description.
        type: string
      followed_by:
        description: This is a default description.
        type: string
      screen_name:
        description: This is a default description.
        type: string
      following:
        description: This is a default description.
        type: string
  Source:
    properties:
      can_dm:
        description: This is a default description.
        type: string
      blocking:
        description: This is a default description.
        type: string
      id_str:
        description: This is a default description.
        type: string
      all_replies:
        description: This is a default description.
        type: string
      want_retweets:
        description: This is a default description.
        type: string
      id:
        description: This is a default description.
        type: string
      marked_spam:
        description: This is a default description.
        type: string
      followed_by:
        description: This is a default description.
        type: string
      notifications_enable:
        description: This is a default description.
        type: string
      screen_name:
        description: This is a default description.
        type: string
  Settings:
    properties:
      use_cookie_personalization:
        description: This is a default description.
        type: string
      trend_location:
        description: This is a default description.
        type: string
      language:
        description: This is a default description.
        type: string
      discoverable_by_email:
        description: This is a default description.
        type: string
      always_use_https:
        description: This is a default description.
        type: string
      protected:
        description: This is a default description.
        type: string
      geo_enabled:
        description: This is a default description.
        type: string
      show_all_inline_media:
        description: This is a default description.
        type: string
      screen_name:
        description: This is a default description.
        type: string
  Sleep:
    properties:
      end_time:
        description: This is a default description.
        type: string
      enabled:
        description: This is a default description.
        type: string
      start_time:
        description: This is a default description.
        type: string
  Location:
    properties:
      name:
        description: This is a default description.
        type: string
      woeid:
        description: This is a default description.
        type: string
      country:
        description: This is a default description.
        type: string
      url:
        description: This is a default description.
        type: string
      countryCode:
        description: This is a default description.
        type: string
      parentid:
        description: This is a default description.
        type: string
  PlaceType:
    properties:
      name:
        description: This is a default description.
        type: string
      code:
        description: This is a default description.
        type: string
  TrendInfo:
    properties:
      as_of:
        description: This is a default description.
        type: string
      created_at:
        description: This is a default description.
        type: string
      locations:
        description: This is a default description.
        type: string
      trends:
        description: This is a default description.
        type: string
  Trends:
    properties:
      events:
        description: This is a default description.
        type: string
      name:
        description: This is a default description.
        type: string
      promoted_content:
        description: This is a default description.
        type: string
      query:
        description: This is a default description.
        type: string
      url:
        description: This is a default description.
        type: string
  Help_Config:
    properties:
      dm_text_character_limit:
        description: This is a default description.
        type: string
      characters_reserved_per_media:
        description: This is a default description.
        type: string
      max_media_per_upload:
        description: This is a default description.
        type: string
      non_username_paths:
        description: This is a default description.
        type: string
      photo_size_limit:
        description: This is a default description.
        type: string
  Help_Language:
    properties:
      code:
        description: This is a default description.
        type: string
      status:
        description: This is a default description.
        type: string
      name:
        description: This is a default description.
        type: string
  Help_Privacy:
    properties:
      privacy:
        description: This is a default description.
        type: string
  Help_Tos:
    properties:
      Tos:
        description: This is a default description.
        type: string
x-collection-name: Postmark
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