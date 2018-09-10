---
name: Stack Exchange
x-slug: stack-exchange
description: After someone asks a question, members of the community propose answers.
  Others vote on those answers. Very quickly, the answers with the most votes rise
  to the top. You dont have to read through a lot of discussion to find the best answer.    Like
  to...
image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/253-stack-exchange.jpg
x-kinRank: "8"
x-alexaRank: "126"
tags: StreamRank
created: "2018-09-10"
modified: "2018-09-10"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/streamrank/master/_listings/stack-exchange/apis.md
specificationVersion: "0.14"
apis:
- name: Stack Exchange - Get Answers
  x-api-slug: answers-get
  description: "Returns all the undeleted answers in the system.\n \nThe sorts accepted
    by this method operate on the follow fields of the answer object:\n - activity
    - last_activity_date\n - creation - creation_date\n - votes - score\n  activity
    is the default sort.\n \n It is possible to create moderately complex queries
    using sort, min, max, fromdate, and todate.\n \nThis method returns a list of
    answers."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/253-stack-exchange.jpg
  humanURL: http://stackexchange.com
  baseURL: https://api.stackexchange.com//2.2
  tags: Citations, Answers, Code, Content, My API Stack, Imports, Stack, Media, Forums,
    Streams, Plugins, Questions, General Data, Relative Data, Service API, Pedestal,
    Historical Data API, Relative StreamRank, Streams
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/streamrank/master/_listings/stack-exchange/answers-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/streamrank/master/_listings/stack-exchange/answers-get-openapi.md
- name: Stack Exchange - Get Badges
  x-api-slug: badges-get
  description: "Returns all the badges in the system.\n \nBadge sorts are a tad complicated.
    For the purposes of sorting (and min/max) tag_based is considered to be greater
    than named.\n \nThis means that you can get a list of all tag based badges by
    passing min=tag_based, and conversely all the named badges by passing max=named,
    with sort=type.\n \nFor ranks, bronze is greater than silver which is greater
    than gold. Along with sort=rank, set max=gold for just gold badges, max=silver&min=silver
    for just silver, and min=bronze for just bronze.\n \nrank is the default sort.\n
    \nThis method returns a list of badges."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/253-stack-exchange.jpg
  humanURL: http://stackexchange.com
  baseURL: https://api.stackexchange.com//2.2
  tags: Citations, Answers, Code, Content, My API Stack, Imports, Stack, Media, Forums,
    Streams, Plugins, Questions, General Data, Relative Data, Service API, Pedestal,
    Historical Data API, Relative StreamRank, Streams
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/streamrank/master/_listings/stack-exchange/badges-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/streamrank/master/_listings/stack-exchange/badges-get-openapi.md
- name: Stack Exchange - Get Comments
  x-api-slug: comments-get
  description: "Gets all the comments on the site.\n \nIf you're filtering for interesting
    comments (by score, creation date, etc.) make use of the sort paramter with appropriate
    min and max values.\n \nIf you're looking to query conversations between users,
    instead use the /users/{ids}/mentioned and /users/{ids}/comments/{toid} methods.\n
    \nThe sorts accepted by this method operate on the follow fields of the comment
    object:\n - creation - creation_date\n - votes - score\n  creation is the default
    sort.\n \n It is possible to create moderately complex queries using sort, min,
    max, fromdate, and todate.\n \nThis method returns a list of comments."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/253-stack-exchange.jpg
  humanURL: http://stackexchange.com
  baseURL: https://api.stackexchange.com//2.2
  tags: Citations, Answers, Code, Content, My API Stack, Imports, Stack, Media, Forums,
    Streams, Plugins, Questions, General Data, Relative Data, Service API, Pedestal,
    Historical Data API, Relative StreamRank, Streams
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/streamrank/master/_listings/stack-exchange/comments-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/streamrank/master/_listings/stack-exchange/comments-get-openapi.md
- name: Stack Exchange - Get Event
  x-api-slug: events-get
  description: "Returns a stream of events that have occurred on the site.\n \nThe
    API considers the following \"events\":\n - posting a question\n - posting an
    answer\n - posting a comment\n - editing a post\n - creating a user\n  \n \nEvents
    are only accessible for 15 minutes after they occurred, and by default only events
    in the last 5 minutes are returned. You can specify the age of the oldest event
    returned by setting the since parameter.\n \nIt is advised that developers batch
    events by ids and make as few subsequent requests to other methods as possible.\n
    \nThis method returns a list of events."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/253-stack-exchange.jpg
  humanURL: http://stackexchange.com
  baseURL: https://api.stackexchange.com//2.2
  tags: Citations, Answers, Code, Content, My API Stack, Imports, Stack, Media, Forums,
    Streams, Plugins, Questions, General Data, Relative Data, Service API, Pedestal,
    Historical Data API, Relative StreamRank, Streams
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/streamrank/master/_listings/stack-exchange/events-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/streamrank/master/_listings/stack-exchange/events-get-openapi.md
- name: Stack Exchange - Get Posts
  x-api-slug: posts-get
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
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/253-stack-exchange.jpg
  humanURL: http://stackexchange.com
  baseURL: https://api.stackexchange.com//2.2
  tags: Citations, Answers, Code, Content, My API Stack, Imports, Stack, Media, Forums,
    Streams, Plugins, Questions, General Data, Relative Data, Service API, Pedestal,
    Historical Data API, Relative StreamRank, Streams
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/streamrank/master/_listings/stack-exchange/posts-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/streamrank/master/_listings/stack-exchange/posts-get-openapi.md
- name: Stack Exchange - Get Questions
  x-api-slug: questions-get
  description: "Gets all the questions on the site.\n \nThis method allows you make
    fairly flexible queries across the entire corpus of questions on a site. For example,
    getting all questions asked in the the week of Jan 1st 2011 with scores of 10
    or more is a single query with parameters sort=votes&min=10&fromdate=1293840000&todate=1294444800.\n
    \nTo constrain questions returned to those with a set of tags, use the tagged
    parameter with a semi-colon delimited list of tags. This is an and contraint,
    passing tagged=c;java will return only those questions with both tags. As such,
    passing more than 5 tags will always return zero results.\n \nThe sorts accepted
    by this method operate on the follow fields of the question object:\n - activity
    - last_activity_date\n - creation - creation_date\n - votes - score\n - hot -
    by the formula ordering the hot tab Does not accept min or max\n - week - by the
    formula ordering the week tab Does not accept min or max\n - month - by the formula
    ordering the month tab Does not accept min or max\n  activity is the default sort.\n
    \n It is possible to create moderately complex queries using sort, min, max, fromdate,
    and todate.\n \nThis method returns a list of questions."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/253-stack-exchange.jpg
  humanURL: http://stackexchange.com
  baseURL: https://api.stackexchange.com//2.2
  tags: Citations, Answers, Code, Content, My API Stack, Imports, Stack, Media, Forums,
    Streams, Plugins, Questions, General Data, Relative Data, Service API, Pedestal,
    Historical Data API, Relative StreamRank, Streams
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/streamrank/master/_listings/stack-exchange/questions-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/streamrank/master/_listings/stack-exchange/questions-get-openapi.md
- name: Stack Exchange - Search
  x-api-slug: search-get
  description: "Searches a site for any questions which fit the given criteria.\n
    \nThis method is intentionally quite limited. For more general searching, you
    should use a proper internet search engine restricted to the domain of the site
    in question.\n \nAt least one of tagged or intitle must be set on this method.
    nottagged is only used if tagged is also set, for performance reasons.\n \ntagged
    and nottagged are semi-colon delimited list of tags. At least 1 tag in tagged
    will be on each returned question if it is passed, making it the OR equivalent
    of the AND version of tagged on /questions.\n \nThe sorts accepted by this method
    operate on the follow fields of the question object:\n - activity - last_activity_date\n
    - creation - creation_date\n - votes - score\n - relevance - matches the relevance
    tab on the site itself Does not accept min or max\n  activity is the default sort.\n
    \n It is possible to create moderately complex queries using sort, min, max, fromdate,
    and todate.\n \nThis method returns a list of questions."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/253-stack-exchange.jpg
  humanURL: http://stackexchange.com
  baseURL: https://api.stackexchange.com//2.2
  tags: Citations, Answers, Code, Content, My API Stack, Imports, Stack, Media, Forums,
    Streams, Plugins, Questions, General Data, Relative Data, Service API, Pedestal,
    Historical Data API, Relative StreamRank, Streams
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/streamrank/master/_listings/stack-exchange/search-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/streamrank/master/_listings/stack-exchange/search-get-openapi.md
- name: Stack Exchange - Get Tags
  x-api-slug: tags-get
  description: "Returns the tags found on a site.\n \nThe inname parameter lets a
    consumer filter down to tags that contain a certain substring. For example, inname=own
    would return both \"download\" and \"owner\" amongst others.\n \nThis method returns
    a list of tags.\n \nThe sorts accepted by this method operate on the follow fields
    of the tag object:\n - popular - count\n - activity - the creation_date of the
    last question asked with the tag\n - name - name\n  popular is the default sort.\n
    \n It is possible to create moderately complex queries using sort, min, max, fromdate,
    and todate."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/253-stack-exchange.jpg
  humanURL: http://stackexchange.com
  baseURL: https://api.stackexchange.com//2.2
  tags: Citations, Answers, Code, Content, My API Stack, Imports, Stack, Media, Forums,
    Streams, Plugins, Questions, General Data, Relative Data, Service API, Pedestal,
    Historical Data API, Relative StreamRank, Streams
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/streamrank/master/_listings/stack-exchange/tags-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/streamrank/master/_listings/stack-exchange/tags-get-openapi.md
x-common:
- type: x-api-gallery
  url: http://square.api.gallery.streamdata.io
- type: x-api-stack
  url: http://stack.exchange.stack.network
- type: x-authentication
  url: https://api.stackexchange.com/docs/authentication
- type: x-base
  url: https://api.stackexchange.com/
- type: x-blog
  url: http://stackexchange.com/blogs
- type: x-blog-rss
  url: http://blog.stackoverflow.com/feed/
- type: x-crunchbase
  url: http://www.crunchbase.com/company/stack-exchange
- type: x-crunchbase
  url: https://crunchbase.com/organization/stack-exchange
- type: x-developer
  url: http://api.stackexchange.com/
- type: x-email
  url: legal@stackexchange.com
- type: x-email
  url: team@stackexchange.com
- type: x-email
  url: team+api@stackexchange.com
- type: x-error-codes
  url: https://api.stackexchange.com/docs/error-handling
- type: x-github
  url: https://github.com/StackExchange
- type: x-javascript-sdk
  url: https://api.stackexchange.com/docs/js-lib
- type: x-linkedin
  url: https://www.linkedin.com/company/stack-exchange
- type: x-privacy
  url: https://stackexchange.com/legal/privacy-policy
- type: x-rate-limits
  url: https://api.stackexchange.com/docs/throttle
- type: x-selfservice-registration
  url: https://stackapps.com/users/login?returnurl=/apps/oauth/register
- type: x-support
  url: https://stackexchange.com/about/contact
- type: x-terms-of-service
  url: http://stackexchange.com/legal/api-terms-of-use
- type: x-twitter
  url: https://twitter.com/StackExchange
- type: x-website
  url: http://stackexchange.com
- type: x-website
  url: https://stackexchange.com/
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---