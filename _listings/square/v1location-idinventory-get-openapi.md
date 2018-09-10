---
swagger: "2.0"
info:
  title: Square Connect
  description: Client library for accessing the Square Connect APIs
  termsOfService: https://connect.squareup.com/tos
  contact:
    name: Square Developer Platform
    url: https://squareup.com/developers
    email: developers@squareup.com
  version: "2.0"
host: connect.squareup.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v1/{location_id}/inventory:
    get:
      summary: Provides inventory information for all of a merchant's inventory-enabled
        item variations.
      description: Provides inventory information for all of a merchant's inventory-enabled
        item variations
      operationId: ListInventory
      x-api-path-slug: v1location-idinventory-get
      parameters:
      - in: query
        name: batch_token
        description: |-
          A pagination cursor to retrieve the next set of results for your
          original query to the endpoint
      - in: query
        name: limit
        description: The maximum number of inventory entries to return in a single
          response
      - in: path
        name: location_id
        description: The ID of the item's associated location
      responses:
        200:
          description: OK
      tags:
      - provides
      - inventory
      - information
      - of
      - merchants
      - inventory-enabled
      - item
      - variations
definitions:
  Address:
    properties:
      address_line_1:
        description: This is a default description.
        type: post
      address_line_2:
        description: This is a default description.
        type: post
      address_line_3:
        description: This is a default description.
        type: post
      administrative_district_level_1:
        description: This is a default description.
        type: post
      administrative_district_level_2:
        description: This is a default description.
        type: post
      administrative_district_level_3:
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
      locality:
        description: This is a default description.
        type: post
  BatchDeleteCatalogObjectsRequest:
    properties:
      object_ids:
        description: This is a default description.
        type: post
  BatchDeleteCatalogObjectsResponse:
    properties:
      deleted_at:
        description: This is a default description.
        type: post
      deleted_object_ids:
        description: This is a default description.
        type: post
      errors:
        description: This is a default description.
        type: post
  BatchRetrieveCatalogObjectsRequest:
    properties:
      include_related_objects:
        description: This is a default description.
        type: post
      object_ids:
        description: This is a default description.
        type: post
  BatchRetrieveCatalogObjectsResponse:
    properties:
      errors:
        description: This is a default description.
        type: post
      objects:
        description: This is a default description.
        type: post
      related_objects:
        description: This is a default description.
        type: post
  BatchUpsertCatalogObjectsRequest:
    properties:
      batches:
        description: This is a default description.
        type: post
      idempotency_key:
        description: This is a default description.
        type: post
  BatchUpsertCatalogObjectsResponse:
    properties:
      errors:
        description: This is a default description.
        type: post
      id_mappings:
        description: This is a default description.
        type: post
      objects:
        description: This is a default description.
        type: post
      updated_at:
        description: This is a default description.
        type: post
  CaptureTransactionRequest:
    properties: []
  CaptureTransactionResponse:
    properties:
      errors:
        description: This is a default description.
        type: post
  Card:
    properties:
      card_brand:
        description: This is a default description.
        type: post
      cardholder_name:
        description: This is a default description.
        type: post
      exp_month:
        description: This is a default description.
        type: post
      exp_year:
        description: This is a default description.
        type: post
      fingerprint:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      last_4:
        description: This is a default description.
        type: post
  CatalogCategory:
    properties:
      name:
        description: This is a default description.
        type: post
  CatalogDiscount:
    properties:
      discount_type:
        description: This is a default description.
        type: post
      label_color:
        description: This is a default description.
        type: post
      name:
        description: This is a default description.
        type: post
      percentage:
        description: This is a default description.
        type: post
      pin_required:
        description: This is a default description.
        type: post
  CatalogIdMapping:
    properties:
      client_object_id:
        description: This is a default description.
        type: post
      object_id:
        description: This is a default description.
        type: post
  CatalogInfoRequest:
    properties: []
  CatalogInfoResponse:
    properties:
      errors:
        description: This is a default description.
        type: post
  CatalogInfoResponseLimits:
    properties:
      batch_delete_max_object_ids:
        description: This is a default description.
        type: post
      batch_retrieve_max_object_ids:
        description: This is a default description.
        type: post
      batch_upsert_max_objects_per_batch:
        description: This is a default description.
        type: post
      batch_upsert_max_total_objects:
        description: This is a default description.
        type: post
      search_max_page_limit:
        description: This is a default description.
        type: post
      update_item_modifier_lists_max_item_ids:
        description: This is a default description.
        type: post
      update_item_modifier_lists_max_modifier_lists_to_disable:
        description: This is a default description.
        type: post
      update_item_modifier_lists_max_modifier_lists_to_enable:
        description: This is a default description.
        type: post
      update_item_taxes_max_item_ids:
        description: This is a default description.
        type: post
      update_item_taxes_max_taxes_to_disable:
        description: This is a default description.
        type: post
  CatalogItem:
    properties:
      abbreviation:
        description: This is a default description.
        type: post
      available_electronically:
        description: This is a default description.
        type: post
      available_for_pickup:
        description: This is a default description.
        type: post
      available_online:
        description: This is a default description.
        type: post
      category_id:
        description: This is a default description.
        type: post
      description:
        description: This is a default description.
        type: post
      image_url:
        description: This is a default description.
        type: post
      label_color:
        description: This is a default description.
        type: post
      modifier_list_info:
        description: This is a default description.
        type: post
      name:
        description: This is a default description.
        type: post
  CatalogItemModifierListInfo:
    properties:
      enabled:
        description: This is a default description.
        type: post
      max_selected_modifiers:
        description: This is a default description.
        type: post
      min_selected_modifiers:
        description: This is a default description.
        type: post
      modifier_list_id:
        description: This is a default description.
        type: post
      modifier_overrides:
        description: This is a default description.
        type: post
  CatalogItemVariation:
    properties:
      inventory_alert_threshold:
        description: This is a default description.
        type: post
      inventory_alert_type:
        description: This is a default description.
        type: post
      item_id:
        description: This is a default description.
        type: post
      location_overrides:
        description: This is a default description.
        type: post
      name:
        description: This is a default description.
        type: post
      pricing_type:
        description: This is a default description.
        type: post
      service_duration:
        description: This is a default description.
        type: post
      sku:
        description: This is a default description.
        type: post
      track_inventory:
        description: This is a default description.
        type: post
      upc:
        description: This is a default description.
        type: post
  CatalogModifier:
    properties:
      name:
        description: This is a default description.
        type: post
  CatalogModifierList:
    properties:
      modifiers:
        description: This is a default description.
        type: post
      name:
        description: This is a default description.
        type: post
      selection_type:
        description: This is a default description.
        type: post
  CatalogModifierOverride:
    properties:
      modifier_id:
        description: This is a default description.
        type: post
      on_by_default:
        description: This is a default description.
        type: post
  CatalogObject:
    properties:
      absent_at_location_ids:
        description: This is a default description.
        type: post
      catalog_v1_ids:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      is_deleted:
        description: This is a default description.
        type: post
      present_at_all_locations:
        description: This is a default description.
        type: post
      present_at_location_ids:
        description: This is a default description.
        type: post
      type:
        description: This is a default description.
        type: post
      updated_at:
        description: This is a default description.
        type: post
      version:
        description: This is a default description.
        type: post
  CatalogObjectBatch:
    properties:
      objects:
        description: This is a default description.
        type: post
  CatalogQuery:
    properties: []
  CatalogQueryExact:
    properties:
      attribute_name:
        description: This is a default description.
        type: post
      attribute_value:
        description: This is a default description.
        type: post
  CatalogQueryItemsForModifierList:
    properties:
      modifier_list_ids:
        description: This is a default description.
        type: post
  CatalogQueryItemsForTax:
    properties:
      tax_ids:
        description: This is a default description.
        type: post
  CatalogQueryPrefix:
    properties:
      attribute_name:
        description: This is a default description.
        type: post
      attribute_prefix:
        description: This is a default description.
        type: post
  CatalogQueryRange:
    properties:
      attribute_max_value:
        description: This is a default description.
        type: post
      attribute_min_value:
        description: This is a default description.
        type: post
      attribute_name:
        description: This is a default description.
        type: post
  CatalogQuerySortedAttribute:
    properties:
      attribute_name:
        description: This is a default description.
        type: post
      initial_attribute_value:
        description: This is a default description.
        type: post
      sort_order:
        description: This is a default description.
        type: post
  CatalogQueryText:
    properties:
      keywords:
        description: This is a default description.
        type: post
  CatalogTax:
    properties:
      applies_to_custom_amounts:
        description: This is a default description.
        type: post
      calculation_phase:
        description: This is a default description.
        type: post
      enabled:
        description: This is a default description.
        type: post
      inclusion_type:
        description: This is a default description.
        type: post
      name:
        description: This is a default description.
        type: post
      percentage:
        description: This is a default description.
        type: post
  CatalogV1Id:
    properties:
      catalog_v1_id:
        description: This is a default description.
        type: post
      location_id:
        description: This is a default description.
        type: post
  ChargeRequest:
    properties:
      buyer_email_address:
        description: This is a default description.
        type: post
      card_nonce:
        description: This is a default description.
        type: post
      customer_card_id:
        description: This is a default description.
        type: post
      customer_id:
        description: This is a default description.
        type: post
      delay_capture:
        description: This is a default description.
        type: post
      idempotency_key:
        description: This is a default description.
        type: post
      note:
        description: This is a default description.
        type: post
      reference_id:
        description: This is a default description.
        type: post
  ChargeResponse:
    properties:
      errors:
        description: This is a default description.
        type: post
  Checkout:
    properties:
      ask_for_shipping_address:
        description: This is a default description.
        type: post
      checkout_page_url:
        description: This is a default description.
        type: post
      created_at:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      merchant_support_email:
        description: This is a default description.
        type: post
      pre_populate_buyer_email:
        description: This is a default description.
        type: post
      redirect_url:
        description: This is a default description.
        type: post
  CreateCheckoutRequest:
    properties:
      ask_for_shipping_address:
        description: This is a default description.
        type: post
      idempotency_key:
        description: This is a default description.
        type: post
      merchant_support_email:
        description: This is a default description.
        type: post
      pre_populate_buyer_email:
        description: This is a default description.
        type: post
      redirect_url:
        description: This is a default description.
        type: post
  CreateCheckoutResponse:
    properties:
      errors:
        description: This is a default description.
        type: post
  CreateCustomerCardRequest:
    properties:
      card_nonce:
        description: This is a default description.
        type: post
      cardholder_name:
        description: This is a default description.
        type: post
  CreateCustomerCardResponse:
    properties:
      errors:
        description: This is a default description.
        type: post
  CreateCustomerRequest:
    properties:
      company_name:
        description: This is a default description.
        type: post
      email_address:
        description: This is a default description.
        type: post
      family_name:
        description: This is a default description.
        type: post
      given_name:
        description: This is a default description.
        type: post
      nickname:
        description: This is a default description.
        type: post
      note:
        description: This is a default description.
        type: post
      phone_number:
        description: This is a default description.
        type: post
      reference_id:
        description: This is a default description.
        type: post
  CreateCustomerResponse:
    properties:
      errors:
        description: This is a default description.
        type: post
  CreateOrderRequest:
    properties:
      discounts:
        description: This is a default description.
        type: post
      line_items:
        description: This is a default description.
        type: post
      reference_id:
        description: This is a default description.
        type: post
      taxes:
        description: This is a default description.
        type: post
      idempotency_key:
        description: This is a default description.
        type: post
  CreateOrderRequestDiscount:
    properties:
      name:
        description: This is a default description.
        type: post
      percentage:
        description: This is a default description.
        type: post
  CreateOrderRequestLineItem:
    properties:
      discounts:
        description: This is a default description.
        type: post
      name:
        description: This is a default description.
        type: post
      quantity:
        description: This is a default description.
        type: post
      taxes:
        description: This is a default description.
        type: post
  CreateOrderRequestTax:
    properties:
      name:
        description: This is a default description.
        type: post
      percentage:
        description: This is a default description.
        type: post
      type:
        description: This is a default description.
        type: post
  CreateRefundRequest:
    properties:
      idempotency_key:
        description: This is a default description.
        type: post
      reason:
        description: This is a default description.
        type: post
      tender_id:
        description: This is a default description.
        type: post
  CreateRefundResponse:
    properties:
      errors:
        description: This is a default description.
        type: post
  Customer:
    properties:
      cards:
        description: This is a default description.
        type: post
      company_name:
        description: This is a default description.
        type: post
      created_at:
        description: This is a default description.
        type: post
      email_address:
        description: This is a default description.
        type: post
      family_name:
        description: This is a default description.
        type: post
      given_name:
        description: This is a default description.
        type: post
      groups:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      nickname:
        description: This is a default description.
        type: post
      note:
        description: This is a default description.
        type: post
  CustomerGroupInfo:
    properties:
      id:
        description: This is a default description.
        type: post
      name:
        description: This is a default description.
        type: post
  CustomerPreferences:
    properties:
      email_unsubscribed:
        description: This is a default description.
        type: post
  DeleteCatalogObjectRequest:
    properties: []
  DeleteCatalogObjectResponse:
    properties:
      deleted_at:
        description: This is a default description.
        type: post
      deleted_object_ids:
        description: This is a default description.
        type: post
      errors:
        description: This is a default description.
        type: post
  DeleteCustomerCardRequest:
    properties: []
  DeleteCustomerCardResponse:
    properties:
      errors:
        description: This is a default description.
        type: post
  DeleteCustomerRequest:
    properties: []
  DeleteCustomerResponse:
    properties:
      errors:
        description: This is a default description.
        type: post
  Device:
    properties:
      id:
        description: This is a default description.
        type: post
      name:
        description: This is a default description.
        type: post
  Error:
    properties:
      category:
        description: This is a default description.
        type: post
      code:
        description: This is a default description.
        type: post
      detail:
        description: This is a default description.
        type: post
      field:
        description: This is a default description.
        type: post
  ItemVariationLocationOverrides:
    properties:
      inventory_alert_threshold:
        description: This is a default description.
        type: post
      inventory_alert_type:
        description: This is a default description.
        type: post
      location_id:
        description: This is a default description.
        type: post
      pricing_type:
        description: This is a default description.
        type: post
      track_inventory:
        description: This is a default description.
        type: post
  ListCatalogRequest:
    properties:
      cursor:
        description: This is a default description.
        type: post
      types:
        description: This is a default description.
        type: post
  ListCatalogResponse:
    properties:
      cursor:
        description: This is a default description.
        type: post
      errors:
        description: This is a default description.
        type: post
      objects:
        description: This is a default description.
        type: post
  ListCustomersRequest:
    properties:
      cursor:
        description: This is a default description.
        type: post
  ListCustomersResponse:
    properties:
      cursor:
        description: This is a default description.
        type: post
      customers:
        description: This is a default description.
        type: post
      errors:
        description: This is a default description.
        type: post
  ListLocationsRequest:
    properties: []
  ListLocationsResponse:
    properties:
      errors:
        description: This is a default description.
        type: post
      locations:
        description: This is a default description.
        type: post
  ListRefundsRequest:
    properties:
      begin_time:
        description: This is a default description.
        type: post
      cursor:
        description: This is a default description.
        type: post
      end_time:
        description: This is a default description.
        type: post
      sort_order:
        description: This is a default description.
        type: post
  ListRefundsResponse:
    properties:
      cursor:
        description: This is a default description.
        type: post
      errors:
        description: This is a default description.
        type: post
      refunds:
        description: This is a default description.
        type: post
  ListTransactionsRequest:
    properties:
      begin_time:
        description: This is a default description.
        type: post
      cursor:
        description: This is a default description.
        type: post
      end_time:
        description: This is a default description.
        type: post
      sort_order:
        description: This is a default description.
        type: post
  ListTransactionsResponse:
    properties:
      cursor:
        description: This is a default description.
        type: post
      errors:
        description: This is a default description.
        type: post
      transactions:
        description: This is a default description.
        type: post
  Location:
    properties:
      capabilities:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      name:
        description: This is a default description.
        type: post
      timezone:
        description: This is a default description.
        type: post
  Money:
    properties:
      amount:
        description: This is a default description.
        type: post
      currency:
        description: This is a default description.
        type: post
  Order:
    properties:
      line_items:
        description: This is a default description.
        type: post
      location_id:
        description: This is a default description.
        type: post
      reference_id:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
  OrderLineItem:
    properties:
      discounts:
        description: This is a default description.
        type: post
      name:
        description: This is a default description.
        type: post
      quantity:
        description: This is a default description.
        type: post
      taxes:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
  OrderLineItemDiscount:
    properties:
      name:
        description: This is a default description.
        type: post
      percentage:
        description: This is a default description.
        type: post
      scope:
        description: This is a default description.
        type: post
      type:
        description: This is a default description.
        type: post
  OrderLineItemTax:
    properties:
      name:
        description: This is a default description.
        type: post
      percentage:
        description: This is a default description.
        type: post
      type:
        description: This is a default description.
        type: post
  Refund:
    properties:
      created_at:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      location_id:
        description: This is a default description.
        type: post
      reason:
        description: This is a default description.
        type: post
      status:
        description: This is a default description.
        type: post
      tender_id:
        description: This is a default description.
        type: post
      transaction_id:
        description: This is a default description.
        type: post
  RetrieveCatalogObjectRequest:
    properties:
      include_related_objects:
        description: This is a default description.
        type: post
  RetrieveCatalogObjectResponse:
    properties:
      errors:
        description: This is a default description.
        type: post
      related_objects:
        description: This is a default description.
        type: post
  RetrieveCustomerRequest:
    properties: []
  RetrieveCustomerResponse:
    properties:
      errors:
        description: This is a default description.
        type: post
  RetrieveTransactionRequest:
    properties: []
  RetrieveTransactionResponse:
    properties:
      errors:
        description: This is a default description.
        type: post
  SearchCatalogObjectsRequest:
    properties:
      begin_time:
        description: This is a default description.
        type: post
      cursor:
        description: This is a default description.
        type: post
      include_deleted_objects:
        description: This is a default description.
        type: post
      include_related_objects:
        description: This is a default description.
        type: post
      limit:
        description: This is a default description.
        type: post
      object_types:
        description: This is a default description.
        type: post
  SearchCatalogObjectsResponse:
    properties:
      cursor:
        description: This is a default description.
        type: post
      errors:
        description: This is a default description.
        type: post
      objects:
        description: This is a default description.
        type: post
      related_objects:
        description: This is a default description.
        type: post
  Tender:
    properties:
      created_at:
        description: This is a default description.
        type: post
      customer_id:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      location_id:
        description: This is a default description.
        type: post
      note:
        description: This is a default description.
        type: post
      transaction_id:
        description: This is a default description.
        type: post
      type:
        description: This is a default description.
        type: post
  TenderCardDetails:
    properties:
      entry_method:
        description: This is a default description.
        type: post
      status:
        description: This is a default description.
        type: post
  TenderCashDetails:
    properties: []
  Transaction:
    properties:
      client_id:
        description: This is a default description.
        type: post
      created_at:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      location_id:
        description: This is a default description.
        type: post
      product:
        description: This is a default description.
        type: post
      reference_id:
        description: This is a default description.
        type: post
      refunds:
        description: This is a default description.
        type: post
      tenders:
        description: This is a default description.
        type: post
  UpdateCustomerRequest:
    properties:
      company_name:
        description: This is a default description.
        type: post
      email_address:
        description: This is a default description.
        type: post
      family_name:
        description: This is a default description.
        type: post
      given_name:
        description: This is a default description.
        type: post
      nickname:
        description: This is a default description.
        type: post
      note:
        description: This is a default description.
        type: post
      phone_number:
        description: This is a default description.
        type: post
      reference_id:
        description: This is a default description.
        type: post
  UpdateCustomerResponse:
    properties:
      errors:
        description: This is a default description.
        type: post
  UpdateItemModifierListsRequest:
    properties:
      item_ids:
        description: This is a default description.
        type: post
      modifier_lists_to_disable:
        description: This is a default description.
        type: post
      modifier_lists_to_enable:
        description: This is a default description.
        type: post
  UpdateItemModifierListsResponse:
    properties:
      errors:
        description: This is a default description.
        type: post
      updated_at:
        description: This is a default description.
        type: post
  UpdateItemTaxesRequest:
    properties:
      item_ids:
        description: This is a default description.
        type: post
      taxes_to_disable:
        description: This is a default description.
        type: post
      taxes_to_enable:
        description: This is a default description.
        type: post
  UpdateItemTaxesResponse:
    properties:
      errors:
        description: This is a default description.
        type: post
      updated_at:
        description: This is a default description.
        type: post
  UpsertCatalogObjectRequest:
    properties:
      idempotency_key:
        description: This is a default description.
        type: post
  UpsertCatalogObjectResponse:
    properties:
      errors:
        description: This is a default description.
        type: post
      id_mappings:
        description: This is a default description.
        type: post
  VoidTransactionRequest:
    properties: []
  VoidTransactionResponse:
    properties:
      errors:
        description: This is a default description.
        type: post
  v1AdjustInventoryRequest:
    properties:
      adjustment_type:
        description: This is a default description.
        type: post
      memo:
        description: This is a default description.
        type: post
      quantity_delta:
        description: This is a default description.
        type: post
  v1BankAccount:
    properties:
      account_number_suffix:
        description: This is a default description.
        type: post
      bank_name:
        description: This is a default description.
        type: post
      currency_code:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      merchant_id:
        description: This is a default description.
        type: post
      name:
        description: This is a default description.
        type: post
      routing_number:
        description: This is a default description.
        type: post
      type:
        description: This is a default description.
        type: post
  v1CashDrawerEvent:
    properties:
      created_at:
        description: This is a default description.
        type: post
      description:
        description: This is a default description.
        type: post
      employee_id:
        description: This is a default description.
        type: post
      event_type:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
  v1CashDrawerShift:
    properties:
      closed_at:
        description: This is a default description.
        type: post
      closing_employee_id:
        description: This is a default description.
        type: post
      description:
        description: This is a default description.
        type: post
      employee_ids:
        description: This is a default description.
        type: post
      ended_at:
        description: This is a default description.
        type: post
      ending_employee_id:
        description: This is a default description.
        type: post
      event_type:
        description: This is a default description.
        type: post
      events:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      opened_at:
        description: This is a default description.
        type: post
  v1Category:
    properties:
      id:
        description: This is a default description.
        type: post
      name:
        description: This is a default description.
        type: post
  v1CreateRefundRequest:
    properties:
      payment_id:
        description: This is a default description.
        type: post
      reason:
        description: This is a default description.
        type: post
      request_idempotence_key:
        description: This is a default description.
        type: post
      type:
        description: This is a default description.
        type: post
  v1Discount:
    properties:
      color:
        description: This is a default description.
        type: post
      discount_type:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      name:
        description: This is a default description.
        type: post
      pin_required:
        description: This is a default description.
        type: post
      rate:
        description: This is a default description.
        type: post
  v1Employee:
    properties:
      authorized_location_ids:
        description: This is a default description.
        type: post
      created_at:
        description: This is a default description.
        type: post
      email:
        description: This is a default description.
        type: post
      external_id:
        description: This is a default description.
        type: post
      first_name:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      last_name:
        description: This is a default description.
        type: post
      role_ids:
        description: This is a default description.
        type: post
      status:
        description: This is a default description.
        type: post
      updated_at:
        description: This is a default description.
        type: post
  v1EmployeeRole:
    properties:
      created_at:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      is_owner:
        description: This is a default description.
        type: post
      name:
        description: This is a default description.
        type: post
      permissions:
        description: This is a default description.
        type: post
      updated_at:
        description: This is a default description.
        type: post
  v1Fee:
    properties:
      adjustment_type:
        description: This is a default description.
        type: post
      applies_to_custom_amounts:
        description: This is a default description.
        type: post
      calculation_phase:
        description: This is a default description.
        type: post
      enabled:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      inclusion_type:
        description: This is a default description.
        type: post
      name:
        description: This is a default description.
        type: post
      rate:
        description: This is a default description.
        type: post
      type:
        description: This is a default description.
        type: post
  v1InventoryEntry:
    properties:
      quantity_on_hand:
        description: This is a default description.
        type: post
      variation_id:
        description: This is a default description.
        type: post
  v1Item:
    properties:
      abbreviation:
        description: This is a default description.
        type: post
      available_online:
        description: This is a default description.
        type: post
      color:
        description: This is a default description.
        type: post
      description:
        description: This is a default description.
        type: post
      fees:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      modifier_lists:
        description: This is a default description.
        type: post
      name:
        description: This is a default description.
        type: post
      taxable:
        description: This is a default description.
        type: post
      type:
        description: This is a default description.
        type: post
  v1ItemImage:
    properties:
      id:
        description: This is a default description.
        type: post
      url:
        description: This is a default description.
        type: post
  v1Merchant:
    properties:
      account_capabilities:
        description: This is a default description.
        type: post
      account_type:
        description: This is a default description.
        type: post
      business_name:
        description: This is a default description.
        type: post
      business_type:
        description: This is a default description.
        type: post
      country_code:
        description: This is a default description.
        type: post
      currency_code:
        description: This is a default description.
        type: post
      email:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      language_code:
        description: This is a default description.
        type: post
      location_details:
        description: This is a default description.
        type: post
  v1ModifierList:
    properties:
      id:
        description: This is a default description.
        type: post
      modifier_options:
        description: This is a default description.
        type: post
      name:
        description: This is a default description.
        type: post
      selection_type:
        description: This is a default description.
        type: post
  v1ModifierOption:
    properties:
      id:
        description: This is a default description.
        type: post
      modifier_list_id:
        description: This is a default description.
        type: post
      name:
        description: This is a default description.
        type: post
      on_by_default:
        description: This is a default description.
        type: post
      ordinal:
        description: This is a default description.
        type: post
  v1Money:
    properties:
      amount:
        description: This is a default description.
        type: post
      currency_code:
        description: This is a default description.
        type: post
  v1Order:
    properties:
      btc_price_satoshi:
        description: This is a default description.
        type: post
      btc_receive_address:
        description: This is a default description.
        type: post
      buyer_email:
        description: This is a default description.
        type: post
      buyer_note:
        description: This is a default description.
        type: post
      canceled_note:
        description: This is a default description.
        type: post
      completed_note:
        description: This is a default description.
        type: post
      created_at:
        description: This is a default description.
        type: post
      errors:
        description: This is a default description.
        type: post
      expires_at:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
  v1OrderHistoryEntry:
    properties:
      action:
        description: This is a default description.
        type: post
      created_at:
        description: This is a default description.
        type: post
  v1Page:
    properties:
      cells:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      name:
        description: This is a default description.
        type: post
      page_index:
        description: This is a default description.
        type: post
  v1PageCell:
    properties:
      column:
        description: This is a default description.
        type: post
      object_id:
        description: This is a default description.
        type: post
      object_type:
        description: This is a default description.
        type: post
      page_id:
        description: This is a default description.
        type: post
      placeholder_type:
        description: This is a default description.
        type: post
      row:
        description: This is a default description.
        type: post
  v1Payment:
    properties:
      additive_tax:
        description: This is a default description.
        type: post
      created_at:
        description: This is a default description.
        type: post
      creator_id:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      inclusive_tax:
        description: This is a default description.
        type: post
      itemizations:
        description: This is a default description.
        type: post
      merchant_id:
        description: This is a default description.
        type: post
      payment_url:
        description: This is a default description.
        type: post
      receipt_url:
        description: This is a default description.
        type: post
      refunds:
        description: This is a default description.
        type: post
  v1PaymentDiscount:
    properties:
      discount_id:
        description: This is a default description.
        type: post
      name:
        description: This is a default description.
        type: post
  v1PaymentItemDetail:
    properties:
      category_name:
        description: This is a default description.
        type: post
      item_id:
        description: This is a default description.
        type: post
      item_variation_id:
        description: This is a default description.
        type: post
      sku:
        description: This is a default description.
        type: post
  v1PaymentItemization:
    properties:
      discounts:
        description: This is a default description.
        type: post
      item_variation_name:
        description: This is a default description.
        type: post
      itemization_type:
        description: This is a default description.
        type: post
      modifiers:
        description: This is a default description.
        type: post
      name:
        description: This is a default description.
        type: post
      notes:
        description: This is a default description.
        type: post
      quantity:
        description: This is a default description.
        type: post
      taxes:
        description: This is a default description.
        type: post
  v1PaymentModifier:
    properties:
      modifier_option_id:
        description: This is a default description.
        type: post
      name:
        description: This is a default description.
        type: post
  v1PaymentTax:
    properties:
      errors:
        description: This is a default description.
        type: post
      fee_id:
        description: This is a default description.
        type: post
      inclusion_type:
        description: This is a default description.
        type: post
      name:
        description: This is a default description.
        type: post
      rate:
        description: This is a default description.
        type: post
  v1PhoneNumber:
    properties:
      calling_code:
        description: This is a default description.
        type: post
      number:
        description: This is a default description.
        type: post
  v1Refund:
    properties:
      created_at:
        description: This is a default description.
        type: post
      merchant_id:
        description: This is a default description.
        type: post
      payment_id:
        description: This is a default description.
        type: post
      processed_at:
        description: This is a default description.
        type: post
      reason:
        description: This is a default description.
        type: post
      type:
        description: This is a default description.
        type: post
  v1Settlement:
    properties:
      bank_account_id:
        description: This is a default description.
        type: post
      entries:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      initiated_at:
        description: This is a default description.
        type: post
      status:
        description: This is a default description.
        type: post
  v1SettlementEntry:
    properties:
      payment_id:
        description: This is a default description.
        type: post
      type:
        description: This is a default description.
        type: post
  v1Tender:
    properties:
      card_brand:
        description: This is a default description.
        type: post
      employee_id:
        description: This is a default description.
        type: post
      entry_method:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      name:
        description: This is a default description.
        type: post
      pan_suffix:
        description: This is a default description.
        type: post
      payment_note:
        description: This is a default description.
        type: post
      receipt_url:
        description: This is a default description.
        type: post
      type:
        description: This is a default description.
        type: post
  v1Timecard:
    properties:
      clockin_location_id:
        description: This is a default description.
        type: post
      clockin_time:
        description: This is a default description.
        type: post
      clockout_location_id:
        description: This is a default description.
        type: post
      clockout_time:
        description: This is a default description.
        type: post
      created_at:
        description: This is a default description.
        type: post
      deleted:
        description: This is a default description.
        type: post
      employee_id:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      updated_at:
        description: This is a default description.
        type: post
  v1TimecardEvent:
    properties:
      clockin_time:
        description: This is a default description.
        type: post
      clockout_time:
        description: This is a default description.
        type: post
      created_at:
        description: This is a default description.
        type: post
      event_type:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
  v1UpdateModifierListRequest:
    properties:
      name:
        description: This is a default description.
        type: post
      selection_type:
        description: This is a default description.
        type: post
  v1UpdateOrderRequest:
    properties:
      action:
        description: This is a default description.
        type: post
      canceled_note:
        description: This is a default description.
        type: post
      completed_note:
        description: This is a default description.
        type: post
      refunded_note:
        description: This is a default description.
        type: post
      shipped_tracking_number:
        description: This is a default description.
        type: post
  v1Variation:
    properties:
      id:
        description: This is a default description.
        type: post
      inventory_alert_threshold:
        description: This is a default description.
        type: post
      inventory_alert_type:
        description: This is a default description.
        type: post
      item_id:
        description: This is a default description.
        type: post
      name:
        description: This is a default description.
        type: post
      ordinal:
        description: This is a default description.
        type: post
      pricing_type:
        description: This is a default description.
        type: post
      sku:
        description: This is a default description.
        type: post
      track_inventory:
        description: This is a default description.
        type: post
      user_data:
        description: This is a default description.
        type: post
  CreateOrderRequestOrder:
    properties:
      line_items:
        description: This is a default description.
        type: post
      reference_id:
        description: This is a default description.
        type: post
x-collection-name: Square
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