---
swagger: "2.0"
x-collection-name: Stack Exchange
x-complete: 0
info:
  title: Stack Exchange Get Posts
  description: "Fetches all posts (questions and answers) on the site.\n \nIn many
    ways this method is the union of /questions and /answers, returning both sets
    of data albeit only the common fields.\n \nMost applications should use the question
    or answer specific methods, but /posts is available for those rare cases where
    any activity is of intereset. Examples of such queries would be: \"all posts on
    Jan. 1st 2011\" or \"top 10 posts by score of all time\".\n \nThe sorts accepted
    by this method operate on the follow fields of the post object:\n - activity -
    last_activity_date\n - creation - creation_date\n - votes - score\n  activity
    is the default sort.\n \n It is possible to create moderately complex queries
    using sort, min, max, fromdate, and todate.\n \nThis method returns a list of
    posts."
  version: "2.0"
host: api.stackexchange.com
basePath: /2.2
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /answers:
    get:
      summary: Get Answers
      description: "Returns all the undeleted answers in the system.\n \nThe sorts
        accepted by this method operate on the follow fields of the answer object:\n
        - activity - last_activity_date\n - creation - creation_date\n - votes - score\n
        \ activity is the default sort.\n \n It is possible to create moderately complex
        queries using sort, min, max, fromdate, and todate.\n \nThis method returns
        a list of answers."
      operationId: returns-all-the-undeleted-answers-in-the-system-the-sorts-accepted-by-this-method-operate-on-the-fol
      x-api-path-slug: answers-get
      parameters:
      - in: query
        name: callback
        description: All API responses are JSON, we do support JSONP with the callback
          query parameter
      - in: query
        name: filter
        description: Filter the discussion
      - in: query
        name: fromdate
        description: Unix date
      - in: query
        name: max
        description: sort = activity => datesort = creation => datesort = votes =>
          number
      - in: query
        name: min
        description: sort = activity => datesort = creation => datesort = votes =>
          number
      - in: query
        name: order
      - in: query
        name: page
      - in: query
        name: pagesize
      - in: query
        name: site
        description: Each of these methods operates on a single site at a time, identified
          by the site parameter
      - in: query
        name: sort
      - in: query
        name: todate
        description: Unix date
      responses:
        200:
          description: OK
      tags:
      - Answers
  /badges:
    get:
      summary: Get Badges
      description: "Returns all the badges in the system.\n \nBadge sorts are a tad
        complicated. For the purposes of sorting (and min/max) tag_based is considered
        to be greater than named.\n \nThis means that you can get a list of all tag
        based badges by passing min=tag_based, and conversely all the named badges
        by passing max=named, with sort=type.\n \nFor ranks, bronze is greater than
        silver which is greater than gold. Along with sort=rank, set max=gold for
        just gold badges, max=silver&min=silver for just silver, and min=bronze for
        just bronze.\n \nrank is the default sort.\n \nThis method returns a list
        of badges."
      operationId: returns-all-the-badges-in-the-system-badge-sorts-are-a-tad-complicated-for-the-purposes-of-sorting-a
      x-api-path-slug: badges-get
      parameters:
      - in: query
        name: callback
        description: All API responses are JSON, we do support JSONP with the callback
          query parameter
      - in: query
        name: filter
        description: '#DiscussionThe Stack Exchange API allows applications to exclude
          almost every field returned'
      - in: query
        name: fromdate
        description: Unix date
      - in: query
        name: inname
      - in: query
        name: max
        description: sort = rank => stringsort = name => stringsort = type => string
      - in: query
        name: min
        description: sort = rank => stringsort = name => stringsort = type => string
      - in: query
        name: order
      - in: query
        name: page
      - in: query
        name: pagesize
      - in: query
        name: site
        description: Each of these methods operates on a single site at a time, identified
          by the site parameter
      - in: query
        name: sort
      - in: query
        name: todate
        description: Unix date
      responses:
        200:
          description: OK
      tags:
      - Badges
  /comments:
    get:
      summary: Get Comments
      description: "Gets all the comments on the site.\n \nIf you're filtering for
        interesting comments (by score, creation date, etc.) make use of the sort
        paramter with appropriate min and max values.\n \nIf you're looking to query
        conversations between users, instead use the /users/{ids}/mentioned and /users/{ids}/comments/{toid}
        methods.\n \nThe sorts accepted by this method operate on the follow fields
        of the comment object:\n - creation - creation_date\n - votes - score\n  creation
        is the default sort.\n \n It is possible to create moderately complex queries
        using sort, min, max, fromdate, and todate.\n \nThis method returns a list
        of comments."
      operationId: gets-all-the-comments-on-the-site-if-youre-filtering-for-interesting-comments-by-score-creation-date
      x-api-path-slug: comments-get
      parameters:
      - in: query
        name: callback
        description: All API responses are JSON, we do support JSONP with the callback
          query parameter
      - in: query
        name: filter
        description: '#DiscussionThe Stack Exchange API allows applications to exclude
          almost every field returned'
      - in: query
        name: fromdate
        description: Unix date
      - in: query
        name: max
        description: sort = creation => datesort = votes => number
      - in: query
        name: min
        description: sort = creation => datesort = votes => number
      - in: query
        name: order
      - in: query
        name: page
      - in: query
        name: pagesize
      - in: query
        name: site
        description: Each of these methods operates on a single site at a time, identified
          by the site parameter
      - in: query
        name: sort
      - in: query
        name: todate
        description: Unix date
      responses:
        200:
          description: OK
      tags:
      - Comments
  /events:
    get:
      summary: Get Event
      description: "Returns a stream of events that have occurred on the site.\n \nThe
        API considers the following \"events\":\n - posting a question\n - posting
        an answer\n - posting a comment\n - editing a post\n - creating a user\n  \n
        \nEvents are only accessible for 15 minutes after they occurred, and by default
        only events in the last 5 minutes are returned. You can specify the age of
        the oldest event returned by setting the since parameter.\n \nIt is advised
        that developers batch events by ids and make as few subsequent requests to
        other methods as possible.\n \nThis method returns a list of events."
      operationId: returns-a-stream-of-events-that-have-occurred-on-the-site-the-api-considers-the-following-events--po
      x-api-path-slug: events-get
      parameters:
      - in: query
        name: callback
        description: All API responses are JSON, we do support JSONP with the callback
          query parameter
      - in: query
        name: filter
        description: '#DiscussionThe Stack Exchange API allows applications to exclude
          almost every field returned'
      - in: query
        name: page
      - in: query
        name: pagesize
      - in: query
        name: since
        description: Unix date
      - in: query
        name: site
        description: Each of these methods operates on a single site at a time, identified
          by the site parameter
      responses:
        200:
          description: OK
      tags:
      - Events
  /posts:
    get:
      summary: Get Posts
      description: "Fetches all posts (questions and answers) on the site.\n \nIn
        many ways this method is the union of /questions and /answers, returning both
        sets of data albeit only the common fields.\n \nMost applications should use
        the question or answer specific methods, but /posts is available for those
        rare cases where any activity is of intereset. Examples of such queries would
        be: \"all posts on Jan. 1st 2011\" or \"top 10 posts by score of all time\".\n
        \nThe sorts accepted by this method operate on the follow fields of the post
        object:\n - activity - last_activity_date\n - creation - creation_date\n -
        votes - score\n  activity is the default sort.\n \n It is possible to create
        moderately complex queries using sort, min, max, fromdate, and todate.\n \nThis
        method returns a list of posts."
      operationId: fetches-all-posts-questions-and-answers-on-the-site-in-many-ways-this-method-is-the-union-of-questio
      x-api-path-slug: posts-get
      parameters:
      - in: query
        name: callback
        description: All API responses are JSON, we do support JSONP with the callback
          query parameter
      - in: query
        name: filter
        description: '#DiscussionThe Stack Exchange API allows applications to exclude
          almost every field returned'
      - in: query
        name: fromdate
        description: Unix date
      - in: query
        name: max
        description: sort = activity => datesort = creation => datesort = votes =>
          number
      - in: query
        name: min
        description: sort = activity => datesort = creation => datesort = votes =>
          number
      - in: query
        name: order
      - in: query
        name: page
      - in: query
        name: pagesize
      - in: query
        name: site
        description: Each of these methods operates on a single site at a time, identified
          by the site parameter
      - in: query
        name: sort
      - in: query
        name: todate
        description: Unix date
      responses:
        200:
          description: OK
      tags:
      - Posts
x-streamrank:
  polling_total_time_average: "0.21"
  polling_size_download_average: "233.73"
  streaming_total_time_average: "0.12"
  streaming_size_download_average: "117.98"
  change_yes: "889"
  change_no: "919"
  time_percentage: "45"
  size_percentage: "50"
  change_percentage: "49"
  last_run: "2018-05-01"
  days_run: "1"
  minute_run: "0"
---