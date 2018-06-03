---
swagger: "2.0"
info:
  title: Tumblr
  description: 'ntShare photos, mobile apps, and social network using Tumblr''s API''s.n    '
  version: 1.0.0
host: api.tumblr.com
basePath: /v2/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /blog/{base-hostname}/post:
    post:
      summary: Add Blog Base Hostname Add
      description: Creates a new video blog post
      operationId: blog.base_hostname.post.post
      parameters:
      - in: path
        name: base-hostname
        description: The unique hostname of the blog
      - in: query
        name: caption
        description: The user-supplied caption
      - in: query
        name: data
        description: A video file, as URL-encoded binary
      - in: query
        name: date
        description: The GMT date and time of the post, as a string
      - in: query
        name: embed
        description: HTML embed code for the video
      - in: query
        name: markdown
        description: Indicates whether the post uses markdown syntax
      - in: query
        name: tags
        description: Comma-separated tags for this post
      - in: query
        name: tweet
        description: 'Manages the autotweet (if enabled) for this post: set to off
          for no tweet, or enter text to override the default tweet'
      - in: query
        name: type
        description: The type of post to create
      responses:
        200:
          description: OK
      tags:
      - blog
      - base
      - hostname
      - post
definitions: []
x-collection-name: Tumblr
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