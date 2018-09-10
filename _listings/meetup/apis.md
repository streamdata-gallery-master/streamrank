---
name: Meetup
x-slug: meetup
description: Find Meetups so you can do more of what matters to you. Or create your
  own group and meet people near you who share your interests.
image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
x-kinRank: "9"
x-alexaRank: "917"
tags: StreamRank
created: "2018-09-10"
modified: "2018-09-10"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/streamrank/master/_listings/meetup/apis.md
specificationVersion: "0.14"
apis:
- name: Meetup - OpenEvents
  x-api-slug: 2open-events-get
  description: Searches for recent and upcoming public events hosted by Meetup groups.
    Its search window  is the past one month through the next three months, and is
    subject to change. Open Events is optimized to search for current events by location,
    category, topic, or text, and only lists Meetups that have **3 or more RSVPs**.
    The number or results returned with each request is not guaranteed to be the same
    as the page size due to secondary filtering. If you're looking for a particular
    event or events within a particular group, use the standard [Events](/meetup_api/docs/2/events/)
    method.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com//
  tags: Meetups, Events, My API Stack, Stack Network, Stack, Media, Marketplace, internet,
    API Provider, API Service Provider, Profiles, General Data, Relative Data, Service
    API, Pedestal, Historical Data API, Relative StreamRank, Streams
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/streamrank/master/_listings/meetup/2open-events-get-openapi.md
- name: Meetup - ActivityFeed
  x-api-slug: activity-get
  description: API method for retrieving the activity feed for a member's groups
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com//
  tags: Meetups, Events, My API Stack, Stack Network, Stack, Media, Marketplace, internet,
    API Provider, API Service Provider, Profiles, General Data, Relative Data, Service
    API, Pedestal, Historical Data API, Relative StreamRank, Streams
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/streamrank/master/_listings/meetup/activity-get-openapi.md
- name: Meetup - Categories
  x-api-slug: 2categories-get
  description: Returns a list of Meetup group categories
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com//
  tags: Meetups, Events, My API Stack, Stack Network, Stack, Media, Marketplace, internet,
    API Provider, API Service Provider, Profiles, General Data, Relative Data, Service
    API, Pedestal, Historical Data API, Relative StreamRank, Streams
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/streamrank/master/_listings/meetup/2categories-get-openapi.md
- name: Meetup - Find Upcoming Events
  x-api-slug: findupcoming-events-get
  description: Returns a list of upcoming events
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com//
  tags: Meetups, Events, My API Stack, Stack Network, Stack, Media, Marketplace, internet,
    API Provider, API Service Provider, Profiles, General Data, Relative Data, Service
    API, Pedestal, Historical Data API, Relative StreamRank, Streams
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/streamrank/master/_listings/meetup/findupcoming-events-get-openapi.md
- name: Meetup - Concierge
  x-api-slug: 2concierge-get
  description: Recommends upcoming meetups for the authorized member in a given location
    and in thier groups
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/6564-meetup.jpg
  humanURL: http://meetup.com
  baseURL: https://api.meetup.com//
  tags: Meetups, Events, My API Stack, Stack Network, Stack, Media, Marketplace, internet,
    API Provider, API Service Provider, Profiles, General Data, Relative Data, Service
    API, Pedestal, Historical Data API, Relative StreamRank, Streams
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/streamrank/master/_listings/meetup/2concierge-get-openapi.md
x-common:
- type: x-api-gallery
  url: http://medium.api.gallery.streamdata.io
- type: x-api-stack
  url: http://meetup.stack.network
- type: x-base
  url: http://api.meetup.com
- type: x-crunchbase
  url: https://crunchbase.com/organization/meetup
- type: x-developer
  url: http://www.meetup.com/meetup_api/
- type: x-email
  url: privacy@meetup.com
- type: x-email
  url: abuse@meetup.com
- type: x-email
  url: api_license@meetup.com
- type: x-email
  url: arbitration-opt-out@meetup.com
- type: x-email
  url: legal@meetup.com
- type: x-github
  url: https://github.com/meetup
- type: x-pricing
  url: http://www.meetup.com/pricing/
- type: x-privacy
  url: http://www.meetup.com/privacy/
- type: x-support
  url: http://www.meetup.com/help/
- type: x-terms-of-service
  url: http://www.meetup.com/terms/
- type: x-twitter
  url: https://twitter.com/MeetupAPI
- type: x-twitter
  url: https://twitter.com/Meetup
- type: x-website
  url: http://meetup.com
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---