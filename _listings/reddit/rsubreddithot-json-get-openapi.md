---
swagger: "2.0"
info:
  title: Reddit
  description: The Reddit API allows you to access the user submitted and rated stories
    on reddit.com. It also provides advanced functionality, including user account
    information and sub-reddit moderation.
  version: 1.0.0
host: www.reddit.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  '{/r/subreddit}/hot.json':
    get:
      summary: Get Subreddit Hot
      description: This endpoint is a listing
      operationId: get&nbsp;RSubredditHot
      x-api-path-slug: rsubreddithot-json-get
      parameters:
      - in: path
        name: /r/subreddit
        description: The subreddit
        type: string
        format: string
      - in: query
        name: after
        description: fullname of a thing
        type: string
      - in: query
        name: before
        description: fullname of a thing
        type: string
      - in: query
        name: count
        description: 'a positive integer (default: 0)'
        type: string
      - in: query
        name: g
        description: one of (GLOBAL, US, AR, AU, BG, CA, CL, CO, HR, CZ, FI, GR, HU,
          IS, IN, IE, JP, MY, MX, NZ, PH, PL, PT, PR, RO, RS, SG, SE, TW, TH, TR,
          GB, US_WA, US_DE, US_DC, US_WI, US_WV, US_HI, US_FL, US_WY, US_NH, US_NJ,
          US_NM, US_TX, US_LA, US_NC, US_ND, US_NE, US_TN, US_NY, US_PA, US_CA, US_NV,
          US_VA, US_CO, US_AK, US_AL, US_AR, US_VT, US_IL, US_GA, US_IN, US_IA, US_OK,
          US_AZ, US_ID, US_CT, US_ME, US_MD, US_MA, US_OH, US_UT, US_MO, US_MN, US_MI,
          US_RI, US_KS, US_MT, US_MS, US_SC, US_KY, US_OR, US_SD)
        type: string
      - in: query
        name: limit
        description: 'the maximum number of items desired (default: 25, maximum: 100)'
        type: string
      - in: query
        name: show
        description: (optional) the string all
        type: string
      - in: query
        name: sr_detail
        description: (optional) expand subreddits
        type: string
      responses:
        200:
          description: OK
      tags:
      - subreddit
      - hot
definitions: []
x-collection-name: Reddit
x-streamrank:
  polling_total_time_average: "0.72"
  polling_size_download_average: "49480.54"
  streaming_total_time_average: "0.47"
  streaming_size_download_average: "24741.57"
  change_yes: "112"
  change_no: "86"
  time_percentage: "35"
  size_percentage: "50"
  change_percentage: "57"
  last_run: "2018-05-06"
  days_run: "1"
  minute_run: "0"
---