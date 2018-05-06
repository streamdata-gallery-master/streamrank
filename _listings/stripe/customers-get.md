---
swagger: "2.0"
info:
  title: Stripe
  description: The Stripe REST API. Please see https://stripe.com/docs/api for more
    details.
  termsOfService: https://stripe.com/us/terms/
  contact:
    name: Stripe Dev Platform Team
    url: https://stripe.com
    email: dev-platform@stripe.com
  version: v1
host: api.stripe.com
basePath: v1/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /customers:
    get:
      summary: Get Customers
      description: Returns a list of your customers
      operationId: getCustomers
      parameters:
      - in: query
        name: created
      - in: query
        name: email
        description: A filter on the list based on the customer's `email` field
      - in: query
        name: ending_before
        description: A cursor for use in pagination
      - in: query
        name: expand
        description: Specifies which fields in the response should be expanded
      - in: query
        name: limit
        description: A limit on the number of objects to be returned
      - in: query
        name: starting_after
        description: A cursor for use in pagination
      responses:
        200:
          description: OK
      tags:
      - customers
definitions:
  account:
    properties:
      business_name:
        description: This is a default description.
        type: post
      business_url:
        description: This is a default description.
        type: post
      charges_enabled:
        description: This is a default description.
        type: post
      country:
        description: This is a default description.
        type: post
      created:
        description: This is a default description.
        type: post
      debit_negative_balances:
        description: This is a default description.
        type: post
      default_currency:
        description: This is a default description.
        type: post
      details_submitted:
        description: This is a default description.
        type: post
      display_name:
        description: This is a default description.
        type: post
      email:
        description: This is a default description.
        type: post
  account_debit_account:
    properties:
      id:
        description: This is a default description.
        type: post
      object:
        description: This is a default description.
        type: post
  account_decline_charge_on:
    properties:
      avs_failure:
        description: This is a default description.
        type: post
      cvc_failure:
        description: This is a default description.
        type: post
  account_tos_acceptance:
    properties:
      date:
        description: This is a default description.
        type: post
      ip:
        description: This is a default description.
        type: post
      user_agent:
        description: This is a default description.
        type: post
  account_verification:
    properties:
      disabled_reason:
        description: This is a default description.
        type: post
      due_by:
        description: This is a default description.
        type: post
      fields_needed:
        description: This is a default description.
        type: post
  account_with_keys:
    properties:
      business_name:
        description: This is a default description.
        type: post
      business_url:
        description: This is a default description.
        type: post
      charges_enabled:
        description: This is a default description.
        type: post
      country:
        description: This is a default description.
        type: post
      created:
        description: This is a default description.
        type: post
      debit_negative_balances:
        description: This is a default description.
        type: post
      default_currency:
        description: This is a default description.
        type: post
      details_submitted:
        description: This is a default description.
        type: post
      display_name:
        description: This is a default description.
        type: post
      email:
        description: This is a default description.
        type: post
  address:
    properties:
      city:
        description: This is a default description.
        type: post
      country:
        description: This is a default description.
        type: post
      line1:
        description: This is a default description.
        type: post
      line2:
        description: This is a default description.
        type: post
      postal_code:
        description: This is a default description.
        type: post
      state:
        description: This is a default description.
        type: post
  alipay_account:
    properties:
      created:
        description: This is a default description.
        type: post
      customer:
        description: This is a default description.
        type: post
      fingerprint:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      livemode:
        description: This is a default description.
        type: post
      metadata:
        description: This is a default description.
        type: post
      object:
        description: This is a default description.
        type: post
      payment_amount:
        description: This is a default description.
        type: post
      payment_currency:
        description: This is a default description.
        type: post
      reusable:
        description: This is a default description.
        type: post
  apple_pay_domain:
    properties:
      created:
        description: This is a default description.
        type: post
      domain_name:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      livemode:
        description: This is a default description.
        type: post
      object:
        description: This is a default description.
        type: post
  application:
    properties:
      id:
        description: This is a default description.
        type: post
      name:
        description: This is a default description.
        type: post
      object:
        description: This is a default description.
        type: post
  backwards_compatible_platform_earning:
    properties:
      account:
        description: This is a default description.
        type: post
      amount:
        description: This is a default description.
        type: post
      amount_refunded:
        description: This is a default description.
        type: post
      application:
        description: This is a default description.
        type: post
      balance_transaction:
        description: This is a default description.
        type: post
      charge:
        description: This is a default description.
        type: post
      created:
        description: This is a default description.
        type: post
      currency:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      livemode:
        description: This is a default description.
        type: post
  balance:
    properties:
      available:
        description: This is a default description.
        type: post
      connect_reserved:
        description: This is a default description.
        type: post
      livemode:
        description: This is a default description.
        type: post
      object:
        description: This is a default description.
        type: post
      pending:
        description: This is a default description.
        type: post
  balance_transaction:
    properties:
      amount:
        description: This is a default description.
        type: post
      available_on:
        description: This is a default description.
        type: post
      created:
        description: This is a default description.
        type: post
      currency:
        description: This is a default description.
        type: post
      description:
        description: This is a default description.
        type: post
      exchange_rate:
        description: This is a default description.
        type: post
      fee:
        description: This is a default description.
        type: post
      fee_details:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      net:
        description: This is a default description.
        type: post
  bank_account:
    properties:
      account:
        description: This is a default description.
        type: post
      account_holder_name:
        description: This is a default description.
        type: post
      account_holder_type:
        description: This is a default description.
        type: post
      bank_name:
        description: This is a default description.
        type: post
      country:
        description: This is a default description.
        type: post
      currency:
        description: This is a default description.
        type: post
      customer:
        description: This is a default description.
        type: post
      default_for_currency:
        description: This is a default description.
        type: post
      fingerprint:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
  bitcoin_receiver:
    properties:
      active:
        description: This is a default description.
        type: post
      amount:
        description: This is a default description.
        type: post
      amount_received:
        description: This is a default description.
        type: post
      bitcoin_amount:
        description: This is a default description.
        type: post
      bitcoin_amount_received:
        description: This is a default description.
        type: post
      bitcoin_uri:
        description: This is a default description.
        type: post
      created:
        description: This is a default description.
        type: post
      currency:
        description: This is a default description.
        type: post
      customer:
        description: This is a default description.
        type: post
      description:
        description: This is a default description.
        type: post
  bitcoin_transaction:
    properties:
      amount:
        description: This is a default description.
        type: post
      bitcoin_amount:
        description: This is a default description.
        type: post
      created:
        description: This is a default description.
        type: post
      currency:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      object:
        description: This is a default description.
        type: post
      receiver:
        description: This is a default description.
        type: post
  card:
    properties:
      account:
        description: This is a default description.
        type: post
      address_city:
        description: This is a default description.
        type: post
      address_country:
        description: This is a default description.
        type: post
      address_line1:
        description: This is a default description.
        type: post
      address_line1_check:
        description: This is a default description.
        type: post
      address_line2:
        description: This is a default description.
        type: post
      address_state:
        description: This is a default description.
        type: post
      address_zip:
        description: This is a default description.
        type: post
      address_zip_check:
        description: This is a default description.
        type: post
      available_payout_methods:
        description: This is a default description.
        type: post
  charge:
    properties:
      amount:
        description: This is a default description.
        type: post
      amount_refunded:
        description: This is a default description.
        type: post
      application:
        description: This is a default description.
        type: post
      application_fee:
        description: This is a default description.
        type: post
      balance_transaction:
        description: This is a default description.
        type: post
      captured:
        description: This is a default description.
        type: post
      created:
        description: This is a default description.
        type: post
      currency:
        description: This is a default description.
        type: post
      customer:
        description: This is a default description.
        type: post
      description:
        description: This is a default description.
        type: post
  charge_outcome:
    properties:
      network_status:
        description: This is a default description.
        type: post
      reason:
        description: This is a default description.
        type: post
      risk_level:
        description: This is a default description.
        type: post
      rule:
        description: This is a default description.
        type: post
      seller_message:
        description: This is a default description.
        type: post
      type:
        description: This is a default description.
        type: post
  connect_collection_transfer:
    properties:
      amount:
        description: This is a default description.
        type: post
      currency:
        description: This is a default description.
        type: post
      destination:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      livemode:
        description: This is a default description.
        type: post
      object:
        description: This is a default description.
        type: post
  country_spec:
    properties:
      default_currency:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      object:
        description: This is a default description.
        type: post
      supported_bank_account_currencies:
        description: This is a default description.
        type: post
      supported_payment_currencies:
        description: This is a default description.
        type: post
      supported_payment_methods:
        description: This is a default description.
        type: post
      verification_fields:
        description: This is a default description.
        type: post
  coupon:
    properties:
      amount_off:
        description: This is a default description.
        type: post
      created:
        description: This is a default description.
        type: post
      currency:
        description: This is a default description.
        type: post
      duration:
        description: This is a default description.
        type: post
      duration_in_months:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      livemode:
        description: This is a default description.
        type: post
      max_redemptions:
        description: This is a default description.
        type: post
      metadata:
        description: This is a default description.
        type: post
      object:
        description: This is a default description.
        type: post
  customer:
    properties:
      account_balance:
        description: This is a default description.
        type: post
      business_vat_id:
        description: This is a default description.
        type: post
      created:
        description: This is a default description.
        type: post
      currency:
        description: This is a default description.
        type: post
      default_source:
        description: This is a default description.
        type: post
      delinquent:
        description: This is a default description.
        type: post
      description:
        description: This is a default description.
        type: post
      email:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      livemode:
        description: This is a default description.
        type: post
  customer_shipping:
    properties:
      name:
        description: This is a default description.
        type: post
      phone:
        description: This is a default description.
        type: post
  customer_source:
    properties:
      id:
        description: This is a default description.
        type: post
      metadata:
        description: This is a default description.
        type: post
      object:
        description: This is a default description.
        type: post
  customer_source_create:
    properties:
      currency:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      metadata:
        description: This is a default description.
        type: post
      object:
        description: This is a default description.
        type: post
  delivery_estimate:
    properties:
      date:
        description: This is a default description.
        type: post
      earliest:
        description: This is a default description.
        type: post
      latest:
        description: This is a default description.
        type: post
      type:
        description: This is a default description.
        type: post
  discount:
    properties:
      customer:
        description: This is a default description.
        type: post
      end:
        description: This is a default description.
        type: post
      object:
        description: This is a default description.
        type: post
      start:
        description: This is a default description.
        type: post
      subscription:
        description: This is a default description.
        type: post
  dispute:
    properties:
      amount:
        description: This is a default description.
        type: post
      balance_transactions:
        description: This is a default description.
        type: post
      charge:
        description: This is a default description.
        type: post
      created:
        description: This is a default description.
        type: post
      currency:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      is_charge_refundable:
        description: This is a default description.
        type: post
      livemode:
        description: This is a default description.
        type: post
      metadata:
        description: This is a default description.
        type: post
      object:
        description: This is a default description.
        type: post
  dispute_evidence:
    properties:
      access_activity_log:
        description: This is a default description.
        type: post
      billing_address:
        description: This is a default description.
        type: post
      cancellation_policy:
        description: This is a default description.
        type: post
      cancellation_policy_disclosure:
        description: This is a default description.
        type: post
      cancellation_rebuttal:
        description: This is a default description.
        type: post
      customer_communication:
        description: This is a default description.
        type: post
      customer_email_address:
        description: This is a default description.
        type: post
      customer_name:
        description: This is a default description.
        type: post
      customer_purchase_ip:
        description: This is a default description.
        type: post
      customer_signature:
        description: This is a default description.
        type: post
  dispute_evidence_details:
    properties:
      due_by:
        description: This is a default description.
        type: post
      has_evidence:
        description: This is a default description.
        type: post
      past_due:
        description: This is a default description.
        type: post
      submission_count:
        description: This is a default description.
        type: post
  ephemeral_key:
    properties:
      created:
        description: This is a default description.
        type: post
      expires:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      livemode:
        description: This is a default description.
        type: post
      object:
        description: This is a default description.
        type: post
  ephemeral_key_with_secret:
    properties:
      created:
        description: This is a default description.
        type: post
      expires:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      livemode:
        description: This is a default description.
        type: post
      object:
        description: This is a default description.
        type: post
      secret:
        description: This is a default description.
        type: post
  error:
    properties:
      error:
        description: This is a default description.
        type: post
  event:
    properties:
      api_version:
        description: This is a default description.
        type: post
      created:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      livemode:
        description: This is a default description.
        type: post
      object:
        description: This is a default description.
        type: post
      pending_webhooks:
        description: This is a default description.
        type: post
      type:
        description: This is a default description.
        type: post
  event_data:
    properties:
      object:
        description: This is a default description.
        type: post
      previous_attributes:
        description: This is a default description.
        type: post
  event_request:
    properties:
      id:
        description: This is a default description.
        type: post
      idempotency_key:
        description: This is a default description.
        type: post
  exchange_rate:
    properties:
      id:
        description: This is a default description.
        type: post
      object:
        description: This is a default description.
        type: post
      rates:
        description: This is a default description.
        type: post
  external_account_source:
    properties:
      account:
        description: This is a default description.
        type: post
      country:
        description: This is a default description.
        type: post
      currency:
        description: This is a default description.
        type: post
      customer:
        description: This is a default description.
        type: post
      default_for_currency:
        description: This is a default description.
        type: post
      fingerprint:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      last4:
        description: This is a default description.
        type: post
      metadata:
        description: This is a default description.
        type: post
      object:
        description: This is a default description.
        type: post
  fee:
    properties:
      amount:
        description: This is a default description.
        type: post
      application:
        description: This is a default description.
        type: post
      currency:
        description: This is a default description.
        type: post
      description:
        description: This is a default description.
        type: post
      type:
        description: This is a default description.
        type: post
  fee_refund:
    properties:
      amount:
        description: This is a default description.
        type: post
      balance_transaction:
        description: This is a default description.
        type: post
      created:
        description: This is a default description.
        type: post
      currency:
        description: This is a default description.
        type: post
      fee:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      metadata:
        description: This is a default description.
        type: post
      object:
        description: This is a default description.
        type: post
  file_upload:
    properties:
      created:
        description: This is a default description.
        type: post
      filename:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      object:
        description: This is a default description.
        type: post
      purpose:
        description: This is a default description.
        type: post
      size:
        description: This is a default description.
        type: post
      type:
        description: This is a default description.
        type: post
      url:
        description: This is a default description.
        type: post
  inventory:
    properties:
      quantity:
        description: This is a default description.
        type: post
      type:
        description: This is a default description.
        type: post
      value:
        description: This is a default description.
        type: post
  invoice:
    properties:
      amount_due:
        description: This is a default description.
        type: post
      application_fee:
        description: This is a default description.
        type: post
      attempt_count:
        description: This is a default description.
        type: post
      attempted:
        description: This is a default description.
        type: post
      billing:
        description: This is a default description.
        type: post
      charge:
        description: This is a default description.
        type: post
      closed:
        description: This is a default description.
        type: post
      currency:
        description: This is a default description.
        type: post
      customer:
        description: This is a default description.
        type: post
      date:
        description: This is a default description.
        type: post
  invoice_item:
    properties:
      amount:
        description: This is a default description.
        type: post
      currency:
        description: This is a default description.
        type: post
      customer:
        description: This is a default description.
        type: post
      date:
        description: This is a default description.
        type: post
      description:
        description: This is a default description.
        type: post
      discountable:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      invoice:
        description: This is a default description.
        type: post
      livemode:
        description: This is a default description.
        type: post
      metadata:
        description: This is a default description.
        type: post
  invoice_line_item:
    properties:
      amount:
        description: This is a default description.
        type: post
      currency:
        description: This is a default description.
        type: post
      description:
        description: This is a default description.
        type: post
      discountable:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      livemode:
        description: This is a default description.
        type: post
      metadata:
        description: This is a default description.
        type: post
      object:
        description: This is a default description.
        type: post
      period:
        description: This is a default description.
        type: post
      proration:
        description: This is a default description.
        type: post
  legacy_transfer_reversal:
    properties:
      amount:
        description: This is a default description.
        type: post
      balance_transaction:
        description: This is a default description.
        type: post
      created:
        description: This is a default description.
        type: post
      currency:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      metadata:
        description: This is a default description.
        type: post
      object:
        description: This is a default description.
        type: post
      transfer:
        description: This is a default description.
        type: post
  legal_entity:
    properties:
      additional_owners:
        description: This is a default description.
        type: post
      business_name:
        description: This is a default description.
        type: post
      business_name_kana:
        description: This is a default description.
        type: post
      business_name_kanji:
        description: This is a default description.
        type: post
      business_tax_id_provided:
        description: This is a default description.
        type: post
      business_vat_id_provided:
        description: This is a default description.
        type: post
      first_name:
        description: This is a default description.
        type: post
      first_name_kana:
        description: This is a default description.
        type: post
      first_name_kanji:
        description: This is a default description.
        type: post
      gender:
        description: This is a default description.
        type: post
  legal_entity_additional_owner:
    properties:
      first_name:
        description: This is a default description.
        type: post
      last_name:
        description: This is a default description.
        type: post
      maiden_name:
        description: This is a default description.
        type: post
      personal_id_number_provided:
        description: This is a default description.
        type: post
  legal_entity_address:
    properties:
      city:
        description: This is a default description.
        type: post
      country:
        description: This is a default description.
        type: post
      line1:
        description: This is a default description.
        type: post
      line2:
        description: This is a default description.
        type: post
      postal_code:
        description: This is a default description.
        type: post
      state:
        description: This is a default description.
        type: post
  legal_entity_dob:
    properties:
      day:
        description: This is a default description.
        type: post
      month:
        description: This is a default description.
        type: post
      year:
        description: This is a default description.
        type: post
  legal_entity_japan_address:
    properties:
      city:
        description: This is a default description.
        type: post
      country:
        description: This is a default description.
        type: post
      line1:
        description: This is a default description.
        type: post
      line2:
        description: This is a default description.
        type: post
      postal_code:
        description: This is a default description.
        type: post
      state:
        description: This is a default description.
        type: post
      town:
        description: This is a default description.
        type: post
  legal_entity_verification:
    properties:
      details:
        description: This is a default description.
        type: post
      details_code:
        description: This is a default description.
        type: post
      document:
        description: This is a default description.
        type: post
      status:
        description: This is a default description.
        type: post
  light_account_logout:
    properties: []
  limited_account:
    properties:
      application_icon:
        description: This is a default description.
        type: post
      application_logo:
        description: This is a default description.
        type: post
      application_name:
        description: This is a default description.
        type: post
      application_url:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      object:
        description: This is a default description.
        type: post
  login_link:
    properties:
      created:
        description: This is a default description.
        type: post
      object:
        description: This is a default description.
        type: post
      url:
        description: This is a default description.
        type: post
  order:
    properties:
      amount:
        description: This is a default description.
        type: post
      amount_returned:
        description: This is a default description.
        type: post
      application:
        description: This is a default description.
        type: post
      application_fee:
        description: This is a default description.
        type: post
      charge:
        description: This is a default description.
        type: post
      created:
        description: This is a default description.
        type: post
      currency:
        description: This is a default description.
        type: post
      customer:
        description: This is a default description.
        type: post
      email:
        description: This is a default description.
        type: post
      external_coupon_code:
        description: This is a default description.
        type: post
  order_item:
    properties:
      amount:
        description: This is a default description.
        type: post
      currency:
        description: This is a default description.
        type: post
      description:
        description: This is a default description.
        type: post
      object:
        description: This is a default description.
        type: post
      parent:
        description: This is a default description.
        type: post
      quantity:
        description: This is a default description.
        type: post
      type:
        description: This is a default description.
        type: post
  order_return:
    properties:
      amount:
        description: This is a default description.
        type: post
      created:
        description: This is a default description.
        type: post
      currency:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      items:
        description: This is a default description.
        type: post
      livemode:
        description: This is a default description.
        type: post
      object:
        description: This is a default description.
        type: post
      order:
        description: This is a default description.
        type: post
      refund:
        description: This is a default description.
        type: post
  package_dimensions:
    properties:
      height:
        description: This is a default description.
        type: post
      length:
        description: This is a default description.
        type: post
      weight:
        description: This is a default description.
        type: post
      width:
        description: This is a default description.
        type: post
  payout:
    properties:
      amount:
        description: This is a default description.
        type: post
      arrival_date:
        description: This is a default description.
        type: post
      automatic:
        description: This is a default description.
        type: post
      balance_transaction:
        description: This is a default description.
        type: post
      created:
        description: This is a default description.
        type: post
      currency:
        description: This is a default description.
        type: post
      description:
        description: This is a default description.
        type: post
      destination:
        description: This is a default description.
        type: post
      failure_balance_transaction:
        description: This is a default description.
        type: post
      failure_code:
        description: This is a default description.
        type: post
  plan:
    properties:
      amount:
        description: This is a default description.
        type: post
      created:
        description: This is a default description.
        type: post
      currency:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      interval:
        description: This is a default description.
        type: post
      interval_count:
        description: This is a default description.
        type: post
      livemode:
        description: This is a default description.
        type: post
      metadata:
        description: This is a default description.
        type: post
      name:
        description: This is a default description.
        type: post
      object:
        description: This is a default description.
        type: post
  platform_earning:
    properties:
      account:
        description: This is a default description.
        type: post
      amount:
        description: This is a default description.
        type: post
      amount_refunded:
        description: This is a default description.
        type: post
      application:
        description: This is a default description.
        type: post
      balance_transaction:
        description: This is a default description.
        type: post
      charge:
        description: This is a default description.
        type: post
      created:
        description: This is a default description.
        type: post
      currency:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      livemode:
        description: This is a default description.
        type: post
  platform_fee:
    properties:
      account:
        description: This is a default description.
        type: post
      amount:
        description: This is a default description.
        type: post
      amount_refunded:
        description: This is a default description.
        type: post
      application:
        description: This is a default description.
        type: post
      balance_transaction:
        description: This is a default description.
        type: post
      charge:
        description: This is a default description.
        type: post
      created:
        description: This is a default description.
        type: post
      currency:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      livemode:
        description: This is a default description.
        type: post
  product:
    properties:
      active:
        description: This is a default description.
        type: post
      attributes:
        description: This is a default description.
        type: post
      caption:
        description: This is a default description.
        type: post
      created:
        description: This is a default description.
        type: post
      deactivate_on:
        description: This is a default description.
        type: post
      description:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      images:
        description: This is a default description.
        type: post
      livemode:
        description: This is a default description.
        type: post
      metadata:
        description: This is a default description.
        type: post
  refund:
    properties:
      amount:
        description: This is a default description.
        type: post
      balance_transaction:
        description: This is a default description.
        type: post
      charge:
        description: This is a default description.
        type: post
      created:
        description: This is a default description.
        type: post
      currency:
        description: This is a default description.
        type: post
      failure_balance_transaction:
        description: This is a default description.
        type: post
      failure_reason:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      metadata:
        description: This is a default description.
        type: post
      object:
        description: This is a default description.
        type: post
  reserve_transaction:
    properties:
      amount:
        description: This is a default description.
        type: post
      currency:
        description: This is a default description.
        type: post
      description:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      object:
        description: This is a default description.
        type: post
  review:
    properties:
      charge:
        description: This is a default description.
        type: post
      created:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      livemode:
        description: This is a default description.
        type: post
      object:
        description: This is a default description.
        type: post
      open:
        description: This is a default description.
        type: post
      reason:
        description: This is a default description.
        type: post
  rule:
    properties:
      action:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      predicate:
        description: This is a default description.
        type: post
  shipping:
    properties:
      carrier:
        description: This is a default description.
        type: post
      name:
        description: This is a default description.
        type: post
      phone:
        description: This is a default description.
        type: post
      tracking_number:
        description: This is a default description.
        type: post
  shipping_method:
    properties:
      amount:
        description: This is a default description.
        type: post
      currency:
        description: This is a default description.
        type: post
      description:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
  sku:
    properties:
      active:
        description: This is a default description.
        type: post
      attributes:
        description: This is a default description.
        type: post
      created:
        description: This is a default description.
        type: post
      currency:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      image:
        description: This is a default description.
        type: post
      livemode:
        description: This is a default description.
        type: post
      metadata:
        description: This is a default description.
        type: post
      object:
        description: This is a default description.
        type: post
      price:
        description: This is a default description.
        type: post
  source:
    properties:
      ach_credit_transfer:
        description: This is a default description.
        type: post
      alipay:
        description: This is a default description.
        type: post
      amount:
        description: This is a default description.
        type: post
      bancontact:
        description: This is a default description.
        type: post
      bitcoin:
        description: This is a default description.
        type: post
      card:
        description: This is a default description.
        type: post
      client_secret:
        description: This is a default description.
        type: post
      created:
        description: This is a default description.
        type: post
      currency:
        description: This is a default description.
        type: post
      flow:
        description: This is a default description.
        type: post
  source_code_verification_flow:
    properties:
      attempts_remaining:
        description: This is a default description.
        type: post
      status:
        description: This is a default description.
        type: post
  source_mandate_notification:
    properties:
      amount:
        description: This is a default description.
        type: post
      created:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      livemode:
        description: This is a default description.
        type: post
      object:
        description: This is a default description.
        type: post
      reason:
        description: This is a default description.
        type: post
      status:
        description: This is a default description.
        type: post
      type:
        description: This is a default description.
        type: post
  source_owner:
    properties:
      email:
        description: This is a default description.
        type: post
      name:
        description: This is a default description.
        type: post
      phone:
        description: This is a default description.
        type: post
      verified_email:
        description: This is a default description.
        type: post
      verified_name:
        description: This is a default description.
        type: post
      verified_phone:
        description: This is a default description.
        type: post
  source_receiver_flow:
    properties:
      address:
        description: This is a default description.
        type: post
      amount_charged:
        description: This is a default description.
        type: post
      amount_received:
        description: This is a default description.
        type: post
      amount_returned:
        description: This is a default description.
        type: post
  source_redirect_flow:
    properties:
      failure_reason:
        description: This is a default description.
        type: post
      return_url:
        description: This is a default description.
        type: post
      status:
        description: This is a default description.
        type: post
      url:
        description: This is a default description.
        type: post
  source_transaction:
    properties:
      ach_credit_transfer:
        description: This is a default description.
        type: post
      alipay:
        description: This is a default description.
        type: post
      amount:
        description: This is a default description.
        type: post
      bancontact:
        description: This is a default description.
        type: post
      bitcoin:
        description: This is a default description.
        type: post
      card:
        description: This is a default description.
        type: post
      created:
        description: This is a default description.
        type: post
      currency:
        description: This is a default description.
        type: post
      giropay:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
  status_transitions:
    properties:
      canceled:
        description: This is a default description.
        type: post
      fulfiled:
        description: This is a default description.
        type: post
      paid:
        description: This is a default description.
        type: post
      returned:
        description: This is a default description.
        type: post
  subscription:
    properties:
      application_fee_percent:
        description: This is a default description.
        type: post
      billing:
        description: This is a default description.
        type: post
      cancel_at_period_end:
        description: This is a default description.
        type: post
      canceled_at:
        description: This is a default description.
        type: post
      created:
        description: This is a default description.
        type: post
      current_period_end:
        description: This is a default description.
        type: post
      current_period_start:
        description: This is a default description.
        type: post
      customer:
        description: This is a default description.
        type: post
      days_until_due:
        description: This is a default description.
        type: post
      ended_at:
        description: This is a default description.
        type: post
  subscription_item:
    properties:
      created:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      metadata:
        description: This is a default description.
        type: post
      object:
        description: This is a default description.
        type: post
      quantity:
        description: This is a default description.
        type: post
      subscription:
        description: This is a default description.
        type: post
  three_d_secure:
    properties:
      amount:
        description: This is a default description.
        type: post
      authenticated:
        description: This is a default description.
        type: post
      created:
        description: This is a default description.
        type: post
      currency:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      livemode:
        description: This is a default description.
        type: post
      object:
        description: This is a default description.
        type: post
      redirect_url:
        description: This is a default description.
        type: post
      status:
        description: This is a default description.
        type: post
  token:
    properties:
      client_ip:
        description: This is a default description.
        type: post
      created:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      livemode:
        description: This is a default description.
        type: post
      object:
        description: This is a default description.
        type: post
      type:
        description: This is a default description.
        type: post
      used:
        description: This is a default description.
        type: post
  token_bank_account:
    properties:
      account_holder_name:
        description: This is a default description.
        type: post
      account_holder_type:
        description: This is a default description.
        type: post
      bank_name:
        description: This is a default description.
        type: post
      country:
        description: This is a default description.
        type: post
      currency:
        description: This is a default description.
        type: post
      fingerprint:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      last4:
        description: This is a default description.
        type: post
      object:
        description: This is a default description.
        type: post
      routing_number:
        description: This is a default description.
        type: post
  token_card:
    properties:
      address_city:
        description: This is a default description.
        type: post
      address_country:
        description: This is a default description.
        type: post
      address_line1:
        description: This is a default description.
        type: post
      address_line1_check:
        description: This is a default description.
        type: post
      address_line2:
        description: This is a default description.
        type: post
      address_state:
        description: This is a default description.
        type: post
      address_zip:
        description: This is a default description.
        type: post
      address_zip_check:
        description: This is a default description.
        type: post
      brand:
        description: This is a default description.
        type: post
      country:
        description: This is a default description.
        type: post
  topup:
    properties:
      amount:
        description: This is a default description.
        type: post
      created:
        description: This is a default description.
        type: post
      currency:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      livemode:
        description: This is a default description.
        type: post
      object:
        description: This is a default description.
        type: post
  transfer:
    properties:
      amount:
        description: This is a default description.
        type: post
      amount_reversed:
        description: This is a default description.
        type: post
      balance_transaction:
        description: This is a default description.
        type: post
      created:
        description: This is a default description.
        type: post
      currency:
        description: This is a default description.
        type: post
      description:
        description: This is a default description.
        type: post
      destination:
        description: This is a default description.
        type: post
      destination_payment:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      livemode:
        description: This is a default description.
        type: post
  transfer_recipient:
    properties:
      cards:
        description: This is a default description.
        type: post
      created:
        description: This is a default description.
        type: post
      default_card:
        description: This is a default description.
        type: post
      description:
        description: This is a default description.
        type: post
      email:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      livemode:
        description: This is a default description.
        type: post
      metadata:
        description: This is a default description.
        type: post
      migrated_to:
        description: This is a default description.
        type: post
      name:
        description: This is a default description.
        type: post
  transfer_recipient_transfer:
    properties:
      amount:
        description: This is a default description.
        type: post
      amount_reversed:
        description: This is a default description.
        type: post
      application_fee:
        description: This is a default description.
        type: post
      automatic:
        description: This is a default description.
        type: post
      balance_transaction:
        description: This is a default description.
        type: post
      created:
        description: This is a default description.
        type: post
      currency:
        description: This is a default description.
        type: post
      date:
        description: This is a default description.
        type: post
      description:
        description: This is a default description.
        type: post
      destination:
        description: This is a default description.
        type: post
  transfer_reversal:
    properties:
      amount:
        description: This is a default description.
        type: post
      balance_transaction:
        description: This is a default description.
        type: post
      created:
        description: This is a default description.
        type: post
      currency:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      metadata:
        description: This is a default description.
        type: post
      object:
        description: This is a default description.
        type: post
      transfer:
        description: This is a default description.
        type: post
  transfer_schedule:
    properties:
      delay_days:
        description: This is a default description.
        type: post
      interval:
        description: This is a default description.
        type: post
      monthly_anchor:
        description: This is a default description.
        type: post
      weekly_anchor:
        description: This is a default description.
        type: post
  upcoming_invoice:
    properties:
      amount_due:
        description: This is a default description.
        type: post
      application_fee:
        description: This is a default description.
        type: post
      attempt_count:
        description: This is a default description.
        type: post
      attempted:
        description: This is a default description.
        type: post
      billing:
        description: This is a default description.
        type: post
      charge:
        description: This is a default description.
        type: post
      closed:
        description: This is a default description.
        type: post
      currency:
        description: This is a default description.
        type: post
      customer:
        description: This is a default description.
        type: post
      date:
        description: This is a default description.
        type: post
x-collection-name: Stripe
x-streamrank:
  polling_total_time_average: ~
  polling_size_download_average: ~
  streaming_total_time_average: ~
  streaming_size_download_average: ~
  change_yes: ~
  change_no: ~
  time_percentage: ~
  size_percentage: ~
  change_percentage: "200"
  last_run: ~
  days_run: ~
  minute_run: ~
---