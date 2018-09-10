---
swagger: "2.0"
info:
  title: New York Times
  description: You already know that NYTimes.com is an unparalleled source of news
    and information. But now it's a premier source of data, too ??? why just read
    the news when you can hack it?
  termsOfService: https://developer.nytimes.com/tou
  version: 2.0.0
host: api.nytimes.com
basePath: /svc
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /mostpopular/v2/mostviewed/{section}/{time-period}.json:
    get:
      summary: Most Viewed by Section & Time Period
      description: With the Most Popular API, you can get links and metadata for the
        blog posts and articles that are most frequently e-mailed, shared and viewed
        by NYTimes
      operationId: GET_mostviewed-section-time-period-json
      parameters:
      - in: path
        name: section
        description: The section of the paper
        type: string
        format: string
      - in: path
        name: time-period
        description: The period of time
        type: string
        format: string
      responses:
        200:
          description: OK
      tags:
      - news
definitions:
  Article:
    properties:
      section:
        description: This is a default description.
        type: get
      subsection:
        description: This is a default description.
        type: get
      title:
        description: This is a default description.
        type: get
      abstract:
        description: This is a default description.
        type: get
      url:
        description: This is a default description.
        type: get
      thumbnail_standard:
        description: This is a default description.
        type: get
      short_url:
        description: This is a default description.
        type: get
      byline:
        description: This is a default description.
        type: get
      item_type:
        description: This is a default description.
        type: get
      updated_date:
        description: This is a default description.
        type: get
  Doc:
    properties:
      web_url:
        description: This is a default description.
        type: get
      snippet:
        description: This is a default description.
        type: get
      lead_paragraph:
        description: This is a default description.
        type: get
      abstract:
        description: This is a default description.
        type: get
      print_page:
        description: This is a default description.
        type: get
      blog:
        description: This is a default description.
        type: get
      source:
        description: This is a default description.
        type: get
      headline:
        description: This is a default description.
        type: get
      keywords:
        description: This is a default description.
        type: get
      pub_date:
        description: This is a default description.
        type: get
  Event:
    properties:
      event_id:
        description: This is a default description.
        type: get
      event_schedule_id:
        description: This is a default description.
        type: get
      last_modified:
        description: This is a default description.
        type: get
      event_name:
        description: This is a default description.
        type: get
      event_detail_url:
        description: This is a default description.
        type: get
      web_description:
        description: This is a default description.
        type: get
      city:
        description: This is a default description.
        type: get
      state:
        description: This is a default description.
        type: get
      film_rating:
        description: This is a default description.
        type: get
      critic_name:
        description: This is a default description.
        type: get
  ArticleWithCountType:
    properties:
      url:
        description: This is a default description.
        type: get
      count_type:
        description: This is a default description.
        type: get
      column:
        description: This is a default description.
        type: get
      section:
        description: This is a default description.
        type: get
      byline:
        description: This is a default description.
        type: get
      title:
        description: This is a default description.
        type: get
      abstract:
        description: This is a default description.
        type: get
      published_date:
        description: This is a default description.
        type: get
      source:
        description: This is a default description.
        type: get
      media:
        description: This is a default description.
        type: get
  Movie:
    properties:
      display_title:
        description: This is a default description.
        type: get
      mpaa_rating:
        description: This is a default description.
        type: get
      critics_pick:
        description: This is a default description.
        type: get
      byline:
        description: This is a default description.
        type: get
      headline:
        description: This is a default description.
        type: get
      summary_short:
        description: This is a default description.
        type: get
      publication_date:
        description: This is a default description.
        type: get
      opening_date:
        description: This is a default description.
        type: get
      date_updated:
        description: This is a default description.
        type: get
      link:
        description: This is a default description.
        type: get
  Critic:
    properties:
      display_name:
        description: This is a default description.
        type: get
      sort_name:
        description: This is a default description.
        type: get
      status:
        description: This is a default description.
        type: get
      bio:
        description: This is a default description.
        type: get
      seo_name:
        description: This is a default description.
        type: get
      multimedia:
        description: This is a default description.
        type: get
  Concept:
    properties:
      concept_id:
        description: This is a default description.
        type: get
      concept_name:
        description: This is a default description.
        type: get
      is_times_tag:
        description: This is a default description.
        type: get
      concept_status:
        description: This is a default description.
        type: get
      vernacular:
        description: This is a default description.
        type: get
      concept_type:
        description: This is a default description.
        type: get
      concept_created:
        description: This is a default description.
        type: get
      concept_updated:
        description: This is a default description.
        type: get
      taxonomy:
        description: This is a default description.
        type: get
      links:
        description: This is a default description.
        type: get
  ConceptRelation:
    properties:
      concept_id:
        description: This is a default description.
        type: get
      concept_name:
        description: This is a default description.
        type: get
      is_times_tag:
        description: This is a default description.
        type: get
      concept_status:
        description: This is a default description.
        type: get
      vernacular:
        description: This is a default description.
        type: get
      concept_type:
        description: This is a default description.
        type: get
      concept_created:
        description: This is a default description.
        type: get
      concept_updated:
        description: This is a default description.
        type: get
x-collection-name: The New York Times
x-streamrank:
  polling_total_time_average: "0.17"
  polling_size_download_average: "60188.9"
  streaming_total_time_average: "0.1"
  streaming_size_download_average: "30094.68"
  change_yes: "21"
  change_no: "2131"
  time_percentage: "41"
  size_percentage: "50"
  change_percentage: "1"
  last_run: "2018-05-12"
  days_run: "7"
  minute_run: "0"
---