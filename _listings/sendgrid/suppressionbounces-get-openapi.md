---
swagger: "2.0"
info:
  title: SendGrid
  description: 'The SendGrid Web API V3 Documentation. This is the entirety of the
    documented v3 endpoints. We have updated all the descriptions, parameters, requests,
    and responses. Authentication Every endpoint requires Authentication in the form
    of an Authorization Header: Authorization: Bearer API_KEY'
  version: 1.0.0
host: api.sendgrid.com
basePath: /v3
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /suppression/bounces:
    get:
      summary: Get Suppression Bounces
      description: '**This endpoint allows you to retrieve all of your bounces'
      operationId: suppression.bounces.get
      x-api-path-slug: suppressionbounces-get
      parameters:
      - in: header
        name: Accept
      - in: query
        name: end_time
        description: Refers end of the time range in unix timestamp when a bounce
          was created (inclusive)
      - in: query
        name: start_time
        description: Refers start of the time range in unix timestamp when a bounce
          was created (inclusive)
      responses:
        200:
          description: OK
      tags:
      - email
      - suppression
      - bounces
definitions:
  advanced_stats_clicks:
    properties:
      date:
        description: This is a default description.
        type: post
      stats:
        description: This is a default description.
        type: post
  advanced_stats_country:
    properties:
      date:
        description: This is a default description.
        type: post
      stats:
        description: This is a default description.
        type: post
  advanced_stats_mailbox_provider:
    properties:
      date:
        description: This is a default description.
        type: post
      stats:
        description: This is a default description.
        type: post
  advanced_stats_opens:
    properties:
      date:
        description: This is a default description.
        type: post
      stats:
        description: This is a default description.
        type: post
  api_key_name_id:
    properties:
      api_key_id:
        description: This is a default description.
        type: post
      name:
        description: This is a default description.
        type: post
  campaign_request:
    properties:
      categories:
        description: This is a default description.
        type: post
      custom_unsubscribe_url:
        description: This is a default description.
        type: post
      html_content:
        description: This is a default description.
        type: post
      ip_pool:
        description: This is a default description.
        type: post
      list_ids:
        description: This is a default description.
        type: post
      plain_content:
        description: This is a default description.
        type: post
      segment_ids:
        description: This is a default description.
        type: post
      sender_id:
        description: This is a default description.
        type: post
      subject:
        description: This is a default description.
        type: post
      suppression_group_id:
        description: This is a default description.
        type: post
  category_stats:
    properties:
      date:
        description: This is a default description.
        type: post
      stats:
        description: This is a default description.
        type: post
  contactdb_custom_field:
    properties:
      name:
        description: This is a default description.
        type: post
      type:
        description: This is a default description.
        type: post
  contactdb_list:
    properties:
      id:
        description: This is a default description.
        type: post
      name:
        description: This is a default description.
        type: post
      recipient_count:
        description: This is a default description.
        type: post
  contactdb_recipient:
    properties:
      recipients:
        description: This is a default description.
        type: post
  contactdb_recipient_count:
    properties:
      recipient_count:
        description: This is a default description.
        type: post
  contactdb_recipient_response:
    properties:
      error_count:
        description: This is a default description.
        type: post
      error_indices:
        description: This is a default description.
        type: post
      errors:
        description: This is a default description.
        type: post
      new_count:
        description: This is a default description.
        type: post
      persisted_recipients:
        description: This is a default description.
        type: post
      updated_count:
        description: This is a default description.
        type: post
  contactdb_segments:
    properties:
      conditions:
        description: This is a default description.
        type: post
      list_id:
        description: This is a default description.
        type: post
      name:
        description: This is a default description.
        type: post
      recipient_count:
        description: This is a default description.
        type: post
  contactdb_segments_conditions:
    properties:
      and_or:
        description: This is a default description.
        type: post
      field:
        description: This is a default description.
        type: post
      operator:
        description: This is a default description.
        type: post
      value:
        description: This is a default description.
        type: post
  contacts:
    properties:
      address:
        description: This is a default description.
        type: post
      address2:
        description: This is a default description.
        type: post
      city:
        description: This is a default description.
        type: post
      company:
        description: This is a default description.
        type: post
      country:
        description: This is a default description.
        type: post
      email:
        description: This is a default description.
        type: post
      first_name:
        description: This is a default description.
        type: post
      last_name:
        description: This is a default description.
        type: post
      phone:
        description: This is a default description.
        type: post
      state:
        description: This is a default description.
        type: post
  credentials:
    properties:
      permissions:
        description: This is a default description.
        type: post
      username:
        description: This is a default description.
        type: post
  email_object:
    properties:
      email:
        description: This is a default description.
        type: post
      name:
        description: This is a default description.
        type: post
  errors:
    properties:
      errors:
        description: This is a default description.
        type: post
  event_webhook_settings:
    properties:
      bounce:
        description: This is a default description.
        type: post
      click:
        description: This is a default description.
        type: post
      deferred:
        description: This is a default description.
        type: post
      delivered:
        description: This is a default description.
        type: post
      dropped:
        description: This is a default description.
        type: post
      enabled:
        description: This is a default description.
        type: post
      group_resubscribe:
        description: This is a default description.
        type: post
      group_unsubscribe:
        description: This is a default description.
        type: post
      open:
        description: This is a default description.
        type: post
      processed:
        description: This is a default description.
        type: post
  global:ErrorResponse:
    properties:
      errors:
        description: This is a default description.
        type: post
  google_analytics_settings:
    properties:
      enabled:
        description: This is a default description.
        type: post
      utm_campaign:
        description: This is a default description.
        type: post
      utm_content:
        description: This is a default description.
        type: post
      utm_medium:
        description: This is a default description.
        type: post
      utm_source:
        description: This is a default description.
        type: post
      utm_term:
        description: This is a default description.
        type: post
  ip_pool:
    properties:
      name:
        description: This is a default description.
        type: post
  ip_whitelabel:
    properties:
      a_record:
        description: This is a default description.
        type: post
      domain:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      ip:
        description: This is a default description.
        type: post
      legacy:
        description: This is a default description.
        type: post
      rdns:
        description: This is a default description.
        type: post
      subdomain:
        description: This is a default description.
        type: post
      users:
        description: This is a default description.
        type: post
      valid:
        description: This is a default description.
        type: post
  link_whitelabel:
    properties:
      default:
        description: This is a default description.
        type: post
      dns:
        description: This is a default description.
        type: post
      domain:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      legacy:
        description: This is a default description.
        type: post
      subdomain:
        description: This is a default description.
        type: post
      user_id:
        description: This is a default description.
        type: post
      username:
        description: This is a default description.
        type: post
      valid:
        description: This is a default description.
        type: post
  mail_batch_id:
    properties:
      batch_id:
        description: This is a default description.
        type: post
  mail_settings_address_whitelabel:
    properties:
      enabled:
        description: This is a default description.
        type: post
      list:
        description: This is a default description.
        type: post
  mail_settings_bcc:
    properties:
      email:
        description: This is a default description.
        type: post
      enabled:
        description: This is a default description.
        type: post
  mail_settings_bounce_purge:
    properties:
      enabled:
        description: This is a default description.
        type: post
      hard_bounces:
        description: This is a default description.
        type: post
      soft_bounces:
        description: This is a default description.
        type: post
  mail_settings_footer:
    properties:
      enabled:
        description: This is a default description.
        type: post
      html_content:
        description: This is a default description.
        type: post
      plain_content:
        description: This is a default description.
        type: post
  mail_settings_forward_bounce:
    properties:
      email:
        description: This is a default description.
        type: post
      enabled:
        description: This is a default description.
        type: post
  mail_settings_forward_spam:
    properties:
      email:
        description: This is a default description.
        type: post
      enabled:
        description: This is a default description.
        type: post
  mail_settings_patch:
    properties:
      email:
        description: This is a default description.
        type: post
      enabled:
        description: This is a default description.
        type: post
  mail_settings_spam_check:
    properties:
      enabled:
        description: This is a default description.
        type: post
      max_score:
        description: This is a default description.
        type: post
      url:
        description: This is a default description.
        type: post
  mail_settings_template:
    properties:
      enabled:
        description: This is a default description.
        type: post
      html_content:
        description: This is a default description.
        type: post
  monitor:
    properties:
      email:
        description: This is a default description.
        type: post
      frequency:
        description: This is a default description.
        type: post
  parse-setting:
    properties:
      hostname:
        description: This is a default description.
        type: post
      send_raw:
        description: This is a default description.
        type: post
      spam_check:
        description: This is a default description.
        type: post
      url:
        description: This is a default description.
        type: post
  partner_settings_new_relic:
    properties:
      enable_subuser_statistics:
        description: This is a default description.
        type: post
      enabled:
        description: This is a default description.
        type: post
      license_key:
        description: This is a default description.
        type: post
  senderID:
    properties:
      address:
        description: This is a default description.
        type: post
      address_2:
        description: This is a default description.
        type: post
      city:
        description: This is a default description.
        type: post
      country:
        description: This is a default description.
        type: post
      created_at:
        description: This is a default description.
        type: post
      from:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      locked:
        description: This is a default description.
        type: post
      nickname:
        description: This is a default description.
        type: post
      reply_to:
        description: This is a default description.
        type: post
  subscription_tracking_settings:
    properties:
      enabled:
        description: This is a default description.
        type: post
      html_content:
        description: This is a default description.
        type: post
      landing:
        description: This is a default description.
        type: post
      plain_content:
        description: This is a default description.
        type: post
      replace:
        description: This is a default description.
        type: post
      url:
        description: This is a default description.
        type: post
  subuser:
    properties:
      disabled:
        description: This is a default description.
        type: post
      email:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      username:
        description: This is a default description.
        type: post
  subuser_post:
    properties:
      authorization_token:
        description: This is a default description.
        type: post
      credit_allocation:
        description: This is a default description.
        type: post
      email:
        description: This is a default description.
        type: post
      signup_session_token:
        description: This is a default description.
        type: post
      user_id:
        description: This is a default description.
        type: post
      username:
        description: This is a default description.
        type: post
  subuser_stats:
    properties:
      date:
        description: This is a default description.
        type: post
      stats:
        description: This is a default description.
        type: post
  suppression_bounce:
    properties:
      created:
        description: This is a default description.
        type: post
      email:
        description: This is a default description.
        type: post
      reason:
        description: This is a default description.
        type: post
      status:
        description: This is a default description.
        type: post
  suppression_group:
    properties:
      description:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      is_default:
        description: This is a default description.
        type: post
      last_email_sent_at:
        description: This is a default description.
        type: post
      name:
        description: This is a default description.
        type: post
  transactional_template:
    properties:
      id:
        description: This is a default description.
        type: post
      name:
        description: This is a default description.
        type: post
      versions:
        description: This is a default description.
        type: post
  transactional_template_version:
    properties:
      active:
        description: This is a default description.
        type: post
      html_content:
        description: This is a default description.
        type: post
      name:
        description: This is a default description.
        type: post
      plain_content:
        description: This is a default description.
        type: post
      subject:
        description: This is a default description.
        type: post
      template_id:
        description: This is a default description.
        type: post
  user_profile:
    properties:
      address:
        description: This is a default description.
        type: post
      address2:
        description: This is a default description.
        type: post
      city:
        description: This is a default description.
        type: post
      company:
        description: This is a default description.
        type: post
      country:
        description: This is a default description.
        type: post
      first_name:
        description: This is a default description.
        type: post
      last_name:
        description: This is a default description.
        type: post
      phone:
        description: This is a default description.
        type: post
      state:
        description: This is a default description.
        type: post
      website:
        description: This is a default description.
        type: post
  whitelabel::domain:
    properties:
      automatic_security:
        description: This is a default description.
        type: post
      custom_spf:
        description: This is a default description.
        type: post
      default:
        description: This is a default description.
        type: post
      dns:
        description: This is a default description.
        type: post
      domain:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      ips:
        description: This is a default description.
        type: post
      legacy:
        description: This is a default description.
        type: post
      subdomain:
        description: This is a default description.
        type: post
      user_id:
        description: This is a default description.
        type: post
  whitelabel:domain_spf:
    properties:
      automatic_security:
        description: This is a default description.
        type: post
      custom_spf:
        description: This is a default description.
        type: post
      default:
        description: This is a default description.
        type: post
      dns:
        description: This is a default description.
        type: post
      domain:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      ips:
        description: This is a default description.
        type: post
      legacy:
        description: This is a default description.
        type: post
      subdomain:
        description: This is a default description.
        type: post
      user_id:
        description: This is a default description.
        type: post
x-collection-name: SendGrid
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