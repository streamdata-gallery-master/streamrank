---
swagger: "2.0"
info:
  title: Taxamo
  description: Taxamo???s elegant suite of APIs and comprehensive reporting dashboard
    enables digital merchants to easily comply with EU regulatory requirements on
    tax calculation, evidence collection, tax return creation and data storage.
  version: "1"
host: api.taxamo.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/v1/transactions:
    get:
      summary: Browse Transactions
      description: Browse transactions
      operationId: listTransactions
      x-api-path-slug: apiv1transactions-get
      parameters:
      - in: query
        name: currency_code
        description: Three letter ISO currency code
      - in: query
        name: filter_text
        description: Filtering expression
      - in: query
        name: format
        description: Output format - supports 'csv' value for this operation
      - in: query
        name: has_note
        description: Return only transactions with a note field set
      - in: query
        name: invoice_number
        description: Transaction invoice number
      - in: query
        name: key_or_custom_id
        description: Taxamo provided transaction key or custom id
      - in: query
        name: limit
        description: Limit (no more than 1000, defaults to 100)
      - in: query
        name: offset
        description: Offset
      - in: query
        name: order_date_from
        description: Order date from in yyyy-MM-dd format
      - in: query
        name: order_date_to
        description: Order date to in yyyy-MM-dd format
      - in: query
        name: original_transaction_key
        description: Taxamo provided original transaction key
      - in: query
        name: sort_reverse
        description: If true, results are sorted in descending order
      - in: query
        name: statuses
        description: Comma separated list of of transaction statuses
      - in: query
        name: tax_country_code
        description: Two letter ISO tax country code
      - in: query
        name: tax_country_codes
        description: Comma separated list of two letter ISO tax country codes
      - in: query
        name: total_amount_greater_than
        description: Return only transactions with total amount greater than given
          number
      - in: query
        name: total_amount_less_than
        description: Return only transactions with total amount less than a given
          number
      responses:
        200:
          description: OK
      tags:
      - browse
      - transactions
definitions:
  C:
    properties:
      day:
        description: This is a default description.
        type: get
      day_raw:
        description: This is a default description.
        type: get
      status:
        description: This is a default description.
        type: get
      value:
        description: This is a default description.
        type: get
  "N":
    properties:
      day:
        description: This is a default description.
        type: get
      day_raw:
        description: This is a default description.
        type: get
      status:
        description: This is a default description.
        type: get
      value:
        description: This is a default description.
        type: get
  additional_currencies:
    properties: []
  additional_currency:
    properties:
      amount:
        description: This is a default description.
        type: get
      currency_code:
        description: This is a default description.
        type: get
      fx_rate:
        description: This is a default description.
        type: get
      tax_amount:
        description: This is a default description.
        type: get
      total_amount:
        description: This is a default description.
        type: get
  by_country:
    properties:
      currency_code:
        description: This is a default description.
        type: get
      tax_country_code:
        description: This is a default description.
        type: get
      tax_country_name:
        description: This is a default description.
        type: get
      value:
        description: This is a default description.
        type: get
  by_status:
    properties:
      C:
        description: This is a default description.
        type: get
      "N":
        description: This is a default description.
        type: get
  by_taxation_type:
    properties:
      deducted_count:
        description: This is a default description.
        type: get
      eu_b2b:
        description: This is a default description.
        type: get
      eu_taxed:
        description: This is a default description.
        type: get
      taxed_count:
        description: This is a default description.
        type: get
      transactions_count:
        description: This is a default description.
        type: get
  calculateSimpleTaxIn:
    properties:
      amount:
        description: This is a default description.
        type: get
      billing_country_code:
        description: This is a default description.
        type: get
      buyer_credit_card_prefix:
        description: This is a default description.
        type: get
      buyer_tax_number:
        description: This is a default description.
        type: get
      currency_code:
        description: This is a default description.
        type: get
      force_country_code:
        description: This is a default description.
        type: get
      invoice_address_city:
        description: This is a default description.
        type: get
      invoice_address_postal_code:
        description: This is a default description.
        type: get
      invoice_address_region:
        description: This is a default description.
        type: get
      order_date:
        description: This is a default description.
        type: get
  calculateSimpleTaxOut:
    properties:
      storage_required_fields:
        description: This is a default description.
        type: get
      tax_required_fields:
        description: This is a default description.
        type: get
  calculateTaxIn:
    properties: []
  calculateTaxLocationIn:
    properties:
      billing_country_code:
        description: This is a default description.
        type: get
      buyer_credit_card_prefix:
        description: This is a default description.
        type: get
  calculateTaxLocationOut:
    properties:
      billing_country_code:
        description: This is a default description.
        type: get
      buyer_credit_card_prefix:
        description: This is a default description.
        type: get
      buyer_ip:
        description: This is a default description.
        type: get
      tax_country_code:
        description: This is a default description.
        type: get
      tax_deducted:
        description: This is a default description.
        type: get
      tax_supported:
        description: This is a default description.
        type: get
  calculateTaxOut:
    properties:
      storage_required_fields:
        description: This is a default description.
        type: get
      tax_required_fields:
        description: This is a default description.
        type: get
  cancelTransactionOut:
    properties:
      success:
        description: This is a default description.
        type: get
  capturePaymentOut:
    properties:
      success:
        description: This is a default description.
        type: get
  confirmTransactionIn:
    properties: []
  confirmTransactionOut:
    properties:
      storage_required_fields:
        description: This is a default description.
        type: get
      tax_required_fields:
        description: This is a default description.
        type: get
  countries:
    properties: []
  country:
    properties:
      callingCode:
        description: This is a default description.
        type: get
      cca2:
        description: This is a default description.
        type: get
      cca3:
        description: This is a default description.
        type: get
      ccn3:
        description: This is a default description.
        type: get
      code:
        description: This is a default description.
        type: get
      code_long:
        description: This is a default description.
        type: get
      codenum:
        description: This is a default description.
        type: get
      currency:
        description: This is a default description.
        type: get
      name:
        description: This is a default description.
        type: get
      tax_number_country_code:
        description: This is a default description.
        type: get
  country_schema:
    properties:
      callingCode:
        description: This is a default description.
        type: get
      cca2:
        description: This is a default description.
        type: get
      cca3:
        description: This is a default description.
        type: get
      ccn3:
        description: This is a default description.
        type: get
      code:
        description: This is a default description.
        type: get
      code_long:
        description: This is a default description.
        type: get
      codenum:
        description: This is a default description.
        type: get
      currency:
        description: This is a default description.
        type: get
      name:
        description: This is a default description.
        type: get
      tax_number_country_code:
        description: This is a default description.
        type: get
  createPaymentIn:
    properties:
      amount:
        description: This is a default description.
        type: get
      payment_information:
        description: This is a default description.
        type: get
      payment_timestamp:
        description: This is a default description.
        type: get
  createPaymentOut:
    properties:
      success:
        description: This is a default description.
        type: get
  createRefundIn:
    properties:
      amount:
        description: This is a default description.
        type: get
      custom_id:
        description: This is a default description.
        type: get
      line_key:
        description: This is a default description.
        type: get
      refund_reason:
        description: This is a default description.
        type: get
      total_amount:
        description: This is a default description.
        type: get
  createRefundOut:
    properties:
      refunded_tax_amount:
        description: This is a default description.
        type: get
      refunded_total_amount:
        description: This is a default description.
        type: get
      tax_amount:
        description: This is a default description.
        type: get
      total_amount:
        description: This is a default description.
        type: get
  createSMSTokenIn:
    properties:
      country_code:
        description: This is a default description.
        type: get
      recipient:
        description: This is a default description.
        type: get
  createSMSTokenOut:
    properties:
      success:
        description: This is a default description.
        type: get
  createTransactionIn:
    properties:
      manual_mode:
        description: This is a default description.
        type: get
  createTransactionOut:
    properties:
      storage_required_fields:
        description: This is a default description.
        type: get
      tax_required_fields:
        description: This is a default description.
        type: get
  currency_schema:
    properties:
      code:
        description: This is a default description.
        type: get
      description:
        description: This is a default description.
        type: get
      isocode:
        description: This is a default description.
        type: get
      isonum:
        description: This is a default description.
        type: get
      minorunits:
        description: This is a default description.
        type: get
  custom_fields:
    properties:
      key:
        description: This is a default description.
        type: get
      value:
        description: This is a default description.
        type: get
  emailInvoiceIn:
    properties:
      buyer_email:
        description: This is a default description.
        type: get
  emailInvoiceOut:
    properties:
      success:
        description: This is a default description.
        type: get
  emailRefundIn:
    properties:
      buyer_email:
        description: This is a default description.
        type: get
  emailRefundOut:
    properties:
      success:
        description: This is a default description.
        type: get
  evidence:
    properties: []
  evidence_schema:
    properties:
      evidence_type:
        description: This is a default description.
        type: get
      evidence_value:
        description: This is a default description.
        type: get
      resolved_country_code:
        description: This is a default description.
        type: get
      used:
        description: This is a default description.
        type: get
  getCountriesDictIn:
    properties:
      tax_supported:
        description: This is a default description.
        type: get
  getCountriesDictOut:
    properties:
      dictionary:
        description: This is a default description.
        type: get
  getCurrenciesDictOut:
    properties:
      dictionary:
        description: This is a default description.
        type: get
  getDailySettlementStatsIn:
    properties:
      date_from:
        description: This is a default description.
        type: get
      date_to:
        description: This is a default description.
        type: get
      interval:
        description: This is a default description.
        type: get
  getDailySettlementStatsOut:
    properties:
      settlement_daily:
        description: This is a default description.
        type: get
  getDetailedRefundsIn:
    properties:
      country_codes:
        description: This is a default description.
        type: get
      date_from:
        description: This is a default description.
        type: get
      date_to:
        description: This is a default description.
        type: get
      format:
        description: This is a default description.
        type: get
      limit:
        description: This is a default description.
        type: get
      offset:
        description: This is a default description.
        type: get
  getDetailedRefundsOut:
    properties:
      report:
        description: This is a default description.
        type: get
  getDomesticSummaryReportIn:
    properties:
      country_code:
        description: This is a default description.
        type: get
      currency_code:
        description: This is a default description.
        type: get
      end_month:
        description: This is a default description.
        type: get
      format:
        description: This is a default description.
        type: get
      fx_date_type:
        description: This is a default description.
        type: get
      start_month:
        description: This is a default description.
        type: get
  getDomesticSummaryReportOut:
    properties:
      currency_code:
        description: This is a default description.
        type: get
      domestic_refunds_amount:
        description: This is a default description.
        type: get
      domestic_refunds_tax_amount:
        description: This is a default description.
        type: get
      domestic_sales_amount:
        description: This is a default description.
        type: get
      domestic_tax_amount:
        description: This is a default description.
        type: get
      end_date:
        description: This is a default description.
        type: get
      eu_tax_deducted_refunds:
        description: This is a default description.
        type: get
      eu_tax_deducted_sales:
        description: This is a default description.
        type: get
      global_refunds_amount:
        description: This is a default description.
        type: get
      global_refunds_tax_amount:
        description: This is a default description.
        type: get
  getEuViesReportIn:
    properties:
      currency_code:
        description: This is a default description.
        type: get
      end_month:
        description: This is a default description.
        type: get
      eu_country_code:
        description: This is a default description.
        type: get
      format:
        description: This is a default description.
        type: get
      fx_date_type:
        description: This is a default description.
        type: get
      lff_sequence_number:
        description: This is a default description.
        type: get
      period_length:
        description: This is a default description.
        type: get
      start_month:
        description: This is a default description.
        type: get
      tax_id:
        description: This is a default description.
        type: get
      transformation:
        description: This is a default description.
        type: get
  getEuViesReportOut:
    properties:
      currency_code:
        description: This is a default description.
        type: get
      end_date:
        description: This is a default description.
        type: get
      report:
        description: This is a default description.
        type: get
      start_date:
        description: This is a default description.
        type: get
  getProductTypesDictOut:
    properties:
      dictionary:
        description: This is a default description.
        type: get
  getRefundsIn:
    properties:
      date_from:
        description: This is a default description.
        type: get
      format:
        description: This is a default description.
        type: get
      moss_country_code:
        description: This is a default description.
        type: get
      tax_region:
        description: This is a default description.
        type: get
  getRefundsOut:
    properties:
      report:
        description: This is a default description.
        type: get
  getSettlementIn:
    properties:
      currency_code:
        description: This is a default description.
        type: get
      end_month:
        description: This is a default description.
        type: get
      format:
        description: This is a default description.
        type: get
      moss_country_code:
        description: This is a default description.
        type: get
      moss_tax_id:
        description: This is a default description.
        type: get
      refund_date_kind_override:
        description: This is a default description.
        type: get
      start_month:
        description: This is a default description.
        type: get
      tax_country_code:
        description: This is a default description.
        type: get
      tax_id:
        description: This is a default description.
        type: get
  getSettlementOut:
    properties:
      end_date:
        description: This is a default description.
        type: get
      fx_rate_date:
        description: This is a default description.
        type: get
      indicative:
        description: This is a default description.
        type: get
      report:
        description: This is a default description.
        type: get
      start_date:
        description: This is a default description.
        type: get
  getSettlementStatsByCountryIn:
    properties:
      date_from:
        description: This is a default description.
        type: get
      date_to:
        description: This is a default description.
        type: get
  getSettlementStatsByCountryOut:
    properties:
      by_country:
        description: This is a default description.
        type: get
  getSettlementStatsByTaxationTypeIn:
    properties:
      date_from:
        description: This is a default description.
        type: get
      date_to:
        description: This is a default description.
        type: get
  getSettlementStatsByTaxationTypeOut:
    properties: []
  getSettlementSummaryIn:
    properties:
      end_month:
        description: This is a default description.
        type: get
      moss_country_code:
        description: This is a default description.
        type: get
      start_month:
        description: This is a default description.
        type: get
      tax_region:
        description: This is a default description.
        type: get
  getSettlementSummaryOut:
    properties: []
  getTransactionOut:
    properties:
      storage_required_fields:
        description: This is a default description.
        type: get
      tax_required_fields:
        description: This is a default description.
        type: get
  getTransactionsStatsByCountryIn:
    properties:
      date_from:
        description: This is a default description.
        type: get
      date_to:
        description: This is a default description.
        type: get
      global_currency_code:
        description: This is a default description.
        type: get
  getTransactionsStatsByCountryOut:
    properties:
      by_country:
        description: This is a default description.
        type: get
  getTransactionsStatsIn:
    properties:
      date_from:
        description: This is a default description.
        type: get
      date_to:
        description: This is a default description.
        type: get
      interval:
        description: This is a default description.
        type: get
  getTransactionsStatsOut:
    properties: []
  input_transaction:
    properties:
      billing_country_code:
        description: This is a default description.
        type: get
      buyer_credit_card_prefix:
        description: This is a default description.
        type: get
      buyer_email:
        description: This is a default description.
        type: get
      buyer_ip:
        description: This is a default description.
        type: get
      buyer_name:
        description: This is a default description.
        type: get
      buyer_tax_number:
        description: This is a default description.
        type: get
      comments:
        description: This is a default description.
        type: get
      currency_code:
        description: This is a default description.
        type: get
      custom_data:
        description: This is a default description.
        type: get
      custom_fields:
        description: This is a default description.
        type: get
  input_transaction_line:
    properties:
      amount:
        description: This is a default description.
        type: get
      custom_fields:
        description: This is a default description.
        type: get
      custom_id:
        description: This is a default description.
        type: get
      deducted_tax_rate:
        description: This is a default description.
        type: get
      description:
        description: This is a default description.
        type: get
      informative:
        description: This is a default description.
        type: get
      line_key:
        description: This is a default description.
        type: get
      product_code:
        description: This is a default description.
        type: get
      product_tax_code:
        description: This is a default description.
        type: get
      product_type:
        description: This is a default description.
        type: get
  input_transaction_update:
    properties:
      billing_country_code:
        description: This is a default description.
        type: get
      buyer_credit_card_prefix:
        description: This is a default description.
        type: get
      buyer_email:
        description: This is a default description.
        type: get
      buyer_ip:
        description: This is a default description.
        type: get
      buyer_name:
        description: This is a default description.
        type: get
      buyer_tax_number:
        description: This is a default description.
        type: get
      comments:
        description: This is a default description.
        type: get
      currency_code:
        description: This is a default description.
        type: get
      custom_data:
        description: This is a default description.
        type: get
      custom_fields:
        description: This is a default description.
        type: get
  invoice_address:
    properties:
      address_detail:
        description: This is a default description.
        type: get
      building_number:
        description: This is a default description.
        type: get
      city:
        description: This is a default description.
        type: get
      country:
        description: This is a default description.
        type: get
      freeform_address:
        description: This is a default description.
        type: get
      postal_code:
        description: This is a default description.
        type: get
      region:
        description: This is a default description.
        type: get
      street_name:
        description: This is a default description.
        type: get
  listPaymentsIn:
    properties:
      limit:
        description: This is a default description.
        type: get
      offset:
        description: This is a default description.
        type: get
  listPaymentsOut:
    properties:
      payments:
        description: This is a default description.
        type: get
  listRefundsOut:
    properties:
      refunds:
        description: This is a default description.
        type: get
  listTransactionsIn:
    properties:
      currency_code:
        description: This is a default description.
        type: get
      filter_text:
        description: This is a default description.
        type: get
      format:
        description: This is a default description.
        type: get
      has_note:
        description: This is a default description.
        type: get
      invoice_number:
        description: This is a default description.
        type: get
      key_or_custom_id:
        description: This is a default description.
        type: get
      limit:
        description: This is a default description.
        type: get
      offset:
        description: This is a default description.
        type: get
      order_date_from:
        description: This is a default description.
        type: get
      order_date_to:
        description: This is a default description.
        type: get
  listTransactionsOut:
    properties:
      transactions:
        description: This is a default description.
        type: get
  locateGivenIPOut:
    properties:
      country_code:
        description: This is a default description.
        type: get
      remote_addr:
        description: This is a default description.
        type: get
  locateMyIPOut:
    properties:
      country_code:
        description: This is a default description.
        type: get
      remote_addr:
        description: This is a default description.
        type: get
  payments:
    properties:
      amount:
        description: This is a default description.
        type: get
      payment_information:
        description: This is a default description.
        type: get
      payment_timestamp:
        description: This is a default description.
        type: get
  product_type_schema:
    properties:
      code:
        description: This is a default description.
        type: get
  refunds:
    properties:
      amount:
        description: This is a default description.
        type: get
      informative:
        description: This is a default description.
        type: get
      line_key:
        description: This is a default description.
        type: get
      refund_note_number:
        description: This is a default description.
        type: get
      refund_note_url:
        description: This is a default description.
        type: get
      refund_reason:
        description: This is a default description.
        type: get
      refund_timestamp:
        description: This is a default description.
        type: get
      tax_amount:
        description: This is a default description.
        type: get
      tax_rate:
        description: This is a default description.
        type: get
      total_amount:
        description: This is a default description.
        type: get
  report:
    properties:
      amount:
        description: This is a default description.
        type: get
      country_code:
        description: This is a default description.
        type: get
      country_name:
        description: This is a default description.
        type: get
      country_subdivision:
        description: This is a default description.
        type: get
      currency_code:
        description: This is a default description.
        type: get
      skip_moss:
        description: This is a default description.
        type: get
      tax_amount:
        description: This is a default description.
        type: get
      tax_rate:
        description: This is a default description.
        type: get
      tax_region:
        description: This is a default description.
        type: get
  settlement_daily_stats_schema:
    properties:
      b2b:
        description: This is a default description.
        type: get
      b2c:
        description: This is a default description.
        type: get
      count:
        description: This is a default description.
        type: get
      day:
        description: This is a default description.
        type: get
      day_raw:
        description: This is a default description.
        type: get
      eu_b2b:
        description: This is a default description.
        type: get
      eu_taxed:
        description: This is a default description.
        type: get
      eu_total:
        description: This is a default description.
        type: get
      untaxed:
        description: This is a default description.
        type: get
  storage_required_fields:
    properties:
      field_name:
        description: This is a default description.
        type: get
  summary:
    properties:
      currency_code:
        description: This is a default description.
        type: get
      end_date:
        description: This is a default description.
        type: get
      fx_rate_date:
        description: This is a default description.
        type: get
      indicative:
        description: This is a default description.
        type: get
      quarter:
        description: This is a default description.
        type: get
      start_date:
        description: This is a default description.
        type: get
      tax_amount:
        description: This is a default description.
        type: get
      tax_entity_name:
        description: This is a default description.
        type: get
  tax_data_schema:
    properties: []
  tax_required_fields:
    properties:
      field_name:
        description: This is a default description.
        type: get
  transaction:
    properties:
      amount:
        description: This is a default description.
        type: get
      billing_country_code:
        description: This is a default description.
        type: get
      buyer_credit_card_prefix:
        description: This is a default description.
        type: get
      buyer_email:
        description: This is a default description.
        type: get
      buyer_ip:
        description: This is a default description.
        type: get
      buyer_name:
        description: This is a default description.
        type: get
      buyer_tax_number:
        description: This is a default description.
        type: get
      buyer_tax_number_valid:
        description: This is a default description.
        type: get
      comments:
        description: This is a default description.
        type: get
      confirm_timestamp:
        description: This is a default description.
        type: get
  transaction_lines:
    properties:
      amount:
        description: This is a default description.
        type: get
      custom_fields:
        description: This is a default description.
        type: get
      custom_id:
        description: This is a default description.
        type: get
      deducted_tax_amount:
        description: This is a default description.
        type: get
      deducted_tax_rate:
        description: This is a default description.
        type: get
      description:
        description: This is a default description.
        type: get
      id:
        description: This is a default description.
        type: get
      informative:
        description: This is a default description.
        type: get
      line_key:
        description: This is a default description.
        type: get
      product_code:
        description: This is a default description.
        type: get
  transactions:
    properties:
      amount:
        description: This is a default description.
        type: get
      billing_country_code:
        description: This is a default description.
        type: get
      buyer_credit_card_prefix:
        description: This is a default description.
        type: get
      buyer_email:
        description: This is a default description.
        type: get
      buyer_ip:
        description: This is a default description.
        type: get
      buyer_name:
        description: This is a default description.
        type: get
      buyer_tax_number:
        description: This is a default description.
        type: get
      buyer_tax_number_valid:
        description: This is a default description.
        type: get
      comments:
        description: This is a default description.
        type: get
      confirm_timestamp:
        description: This is a default description.
        type: get
  unconfirmTransactionIn:
    properties: []
  unconfirmTransactionOut:
    properties:
      storage_required_fields:
        description: This is a default description.
        type: get
      tax_required_fields:
        description: This is a default description.
        type: get
  updateTransactionIn:
    properties: []
  updateTransactionOut:
    properties:
      storage_required_fields:
        description: This is a default description.
        type: get
      tax_required_fields:
        description: This is a default description.
        type: get
  us_tax_exempt_state:
    properties:
      identifier_for_exemption_reason:
        description: This is a default description.
        type: get
      reason_for_exemption:
        description: This is a default description.
        type: get
      state_abbr:
        description: This is a default description.
        type: get
  us_tax_exemption_certificate_details_schema:
    properties:
      exempt_states:
        description: This is a default description.
        type: get
      purchaser_address1:
        description: This is a default description.
        type: get
      purchaser_address2:
        description: This is a default description.
        type: get
      purchaser_business_type:
        description: This is a default description.
        type: get
      purchaser_business_type_other_value:
        description: This is a default description.
        type: get
      purchaser_city:
        description: This is a default description.
        type: get
      purchaser_exemption_reason:
        description: This is a default description.
        type: get
      purchaser_exemption_reason_value:
        description: This is a default description.
        type: get
      purchaser_first_name:
        description: This is a default description.
        type: get
      purchaser_last_name:
        description: This is a default description.
        type: get
  us_tax_exemption_certificate_schema:
    properties:
      certificate_id:
        description: This is a default description.
        type: get
  us_tax_id:
    properties:
      state_of_issue:
        description: This is a default description.
        type: get
      tax_id:
        description: This is a default description.
        type: get
      tax_id_type:
        description: This is a default description.
        type: get
  validateTaxNumberIn:
    properties:
      country_code:
        description: This is a default description.
        type: get
  validateTaxNumberOut:
    properties:
      billing_country_code:
        description: This is a default description.
        type: get
      buyer_tax_number:
        description: This is a default description.
        type: get
      buyer_tax_number_valid:
        description: This is a default description.
        type: get
      tax_deducted:
        description: This is a default description.
        type: get
  verifySMSTokenOut:
    properties:
      country_code:
        description: This is a default description.
        type: get
x-collection-name: Taxamo
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