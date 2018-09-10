swagger: "2.0"
x-collection-name: CoinMarketCap
x-complete: 1
info:
  title: CoinMarketCap Professional API Documentation
  description: -introductionthe-coinmarketcap-professional-api-is-a-suite-of-highperformance-restful-json-endpoints-that-are-specifically-designed-to-meet-the-missioncritical-demands-of-application-developers-data-scientists-and-enterprise-business-platforms-this-api-reference-includes-all-technical-documentation-developers-need-to-integrate-thirdparty-applications-and-platforms--additional-answers-to-common-questions-can-be-found-in-the-coinmarketcap-professional-api-faqhttpspro-coinmarketcap-comfaq-note-if-youre-using-the-coinmarketcap-public-api-youll-want-to-access-the-public-api-documentationhttpscoinmarketcap-comapi-the-professional-api-is-an-entirely-separate-api-product--if-youre-uncertain-of-which-you-need-for-your-needs-check-the-feature-comparison-matrixhttpspro-coinmarketcap-comfaq--quick-start-guidefor-developers-eager-to-hit-the-ground-running-with-the-professional-api-here-are-3-quick-steps-to-make-your-first-call-with-the-professional-api-1--sign-up--sign-up-for-an-api-key-in-one-of-our-two-professional-api-environments-sandbox-coinmarketcap-comhttpssandbox-coinmarketcap-com--this-testing-sandbox-has-free-access-to-all-endpoints-and-all-subscription-plans-to-test-with-a-snapshot-of-our-market-data----pro-coinmarketcap-comhttpspro-coinmarketcap-com--this-is-our-live-production-environment-with-the-latest-market-data--select-the-free-starter-plan-if-it-meets-your-needs-or-upgrade-to-a-paid-tier-----2--get-your-api-key--once-you-sign-up-youll-land-on-your-developer-portal-account-dashboard--copy-your-api-from-the-api-key-box-in-the-top-left-panel-3--make-a-test-call-using-your-key--here-is-an-example-fetch-all-active-cryptocurrencies-by-market-cap-and-return-market-values-in-usd-and-euroshttpsproapi-coinmarketcap-comv1cryptocurrencylistingslateststart0limit5000convertusdeur-replace-api-key-in-querystring-with-your-own-this-basic-example-is-in-node-js-es5var-xhr--new-xmlhttprequestxhr-setrequestheaderxcmc-pro-api-key-b54bcf4d1bca4e8e9a2422ff2c3d462cxhr-responsetype--jsonxhr-setrequestheaderaccept-applicationjsonxhr-openget-httpsproapi-coinmarketcap-comv1cryptocurrencylistingslateststart0limit5000convertusdeurxhr-onreadystatechange--function-handler---if-xhr-readystate--4--xhr-status--200-----console-logxhr-response--xhr-send4--implement-your-application--now-that-youve-confirmed-your-api-key-is-working-get-familiar-with-the-api-by-reading-the-rest-of-this-api-reference-and-commence-building-your-applicationnote-making-http-requests-on-the-client-side-with-javascript-is-currently-prohibited-through-cors-configuration--this-is-to-protect-your-api-key-which-should-not-be-visible-to-users-of-your-application-so-your-api-key-is-not-stolen--secure-your-api-key-by-routing-calls-through-your-own-backend-service--authentication-acquiring-an-api-keyall-http-requests-made-against-the-professional-api-must-be-validated-with-an-api-key--if-you-dont-have-an-api-key-yet-visit-the-professional-api-developer-portalhttpspro-coinmarketcap-com-to-register-for-one--using-your-api-keyyou-may-use-any-server-side-programming-language-that-can-make-http-requests-to-target-the-professional-api--all-requests-should-target-domain-httpsproapi-coinmarketcap-com-you-can-supply-your-api-key-in-rest-api-calls-in-one-of-two-ways1--preferred-method-via-a-custom-header-named-xcmc-pro-api-key2--convenience-method-via-a-query-string-parameter-named-cmc-pro-api-keysecurity-warning-its-important-to-secure-your-api-key-against-public-access--the-custom-header-option-is-strongly-recommended-over-the-querystring-option-for-passing-your-api-key-in-a-production-environment--api-key-usage-creditsmost-plans-include-a-monthly-limit-or-hard-cap-to-the-number-of-data-calls-that-can-be-made--this-limit-is-tied-to-your-api-keys-usage-tierhttpspro-coinmarketcap-compricing-and-resets-at-midnight-utc-at-the-beginning-of-each-calendar-month-an-api-keys-monthly-usage-limit-is-tracked-as-api-call-credits-which-are-incremented-11-against-successful-http-status-200-data-calls-made-with-your-key-with-these-exceptions-account-management-endpoints-usage-stats-endpoints-and-error-responses-are-not-included-in-this-monthly-limit--paginated-endpoints-listbased-endpoints-track-an-additional-call-credit-for-every-100-data-points-returned-rounded-up-beyond-our-100-data-point-defaults--our-lightweight-map-endpoints-are-not-included-in-this-limit-and-always-count-as-1-credit--bundled-api-calls-many-endpoints-support-resource-and-currency-conversion-bundlingsectionstandardsandconventions--bundled-resources-are-also-tracked-as-1-call-credit-for-every-100-resources-returned-rounded-up--optional-currency-conversion-bundling-using-the-convert-parameter-also-increment-an-additional-api-call-credit-for-every-conversion-requested-beyond-the-first-you-can-log-in-to-the-developer-portalhttpspro-coinmarketcap-com-to-view-live-stats-on-your-api-key-usage-and-limits-including-the-number-of-credits-used-for-each-call--you-can-also-find-call-credit-usage-in-the-json-response-for-each-api-call--see-the-status-objectsectionstandardsandconventions-for-details--endpoint-overview-the-professional-api-is-divided-into-4-toplevel-categoriesendpoint-category---descriptioncryptocurrencytagcryptocurrency--endpoints-that-return-data-around-cryptocurrencies-such-as-ordered-cryptocurrency-lists-or-price-and-volume-data-exchangetagexchange--endpoints-that-return-data-around-cryptocurrency-exchanges-such-as-ordered-exchange-lists-and-market-pair-data-globalmetricstagglobalmetrics--endpoints-that-return-aggregate-market-data-such-as-global-market-cap-and-btc-dominance-toolstagtools---useful-utilities-such-as-cryptocurrencytofiat-price-conversions--endpoint-paths-follow-a-pattern-matching-the-type-of-data-providedendpoint-path---endpoint-type--descriptionlatest--latest-market-data--latest-market-ticker-quotes-and-averages-for-cryptocurrencies-and-exchanges-historical--historical-market-data--intervals-of-historic-market-data-like-ohlcv-data-or-data-for-use-in-charting-libraries-info--metadata--cryptocurrency-and-exchange-metadata-like-block-explorer-urls-and-logos-map--id-maps--utility-endpoints-to-get-a-map-of-resources-to-coinmarketcap-ids---cryptocurrency-and-exchange-endpoints-provide-2-different-ways-of-accessing-data-depending-on-purpose-listing-endpoints-flexible-paginated-listings-endpoints-allow-you-to-sort-and-filter-lists-of-data-like-cryptocurrencies-by-market-cap-or-exchanges-by-volume--item-endpoints-convenient-idbased-resource-endpoints-like-quotes-and-marketpairs-allow-you-to-bundle-several-ids-for-example-this-allows-you-to-get-latest-market-quotes-for-a-specific-set-of-cryptocurrencies-in-one-call--full-endpoint-listclick-on-the-endpoint-for-detailed-documentation-about-each-endpoint-type--endpoint---description--example-callcryptocurrency--v1cryptocurrencyinfooperationgetv1cryptocurrencyinfo--get-cryptocurrency-metadata--httpsproapi-coinmarketcap-comv1cryptocurrencyinfoid1210cryptocurrency--v1cryptocurrencymapoperationgetv1cryptocurrencymap--get-cryptocurrency-coinmarketcap-id-map--httpsproapi-coinmarketcap-comv1cryptocurrencymaplisting-statusactivestart0limit100cryptocurrency--v1cryptocurrencylistingslatestoperationgetv1cryptocurrencylistingslatest--list-all-cryptocurrencies-latest-httpsproapi-coinmarketcap-comv1cryptocurrencylistingslatestsortmarket-capstart0limit10cryptocurrency-typetokensconvertusdbtccryptocurrency--v1cryptocurrencymarketpairslatestoperationgetv1cryptocurrencymarketpairslatest--get-cryptocurrency-market-pairs-latest--httpsproapi-coinmarketcap-comv1cryptocurrencymarketpairslatestid1convertltcethcryptocurrency--v1cryptocurrencyohlcvhistoricaloperationgetv1cryptocurrencyohlcvhistorical--get-cryptocurrency-ohlcv-values-historical--httpsproapi-coinmarketcap-comv1cryptocurrencyohlcvhistoricaltime-start20170101id1time-start20170101time-end20180101interval7dcount12convertcadcryptocurrency--v1cryptocurrencyquoteslatestoperationgetv1cryptocurrencyquoteslatest--get-cryptocurrency-market-quotes-latest--httpsproapi-coinmarketcap-comv1cryptocurrencyquoteslatestsymbolbtcethxrpbcheosltcxlmconvertbtcetheurcryptocurrency--v1cryptocurrencyquoteshistoricaloperationgetv1cryptocurrencyquoteshistorical--get-cryptocurrency-market-quotes-historical--httpsproapi-coinmarketcap-comv1cryptocurrencyquoteshistoricalid1time-start2017time-end2018interval30dcount12exchange--v1exchangeinfooperationgetv1exchangeinfo--get-exchange-metadata--httpsproapi-coinmarketcap-comv1exchangeinfoid1210exchange--v1exchangemapoperationgetv1exchangemap--get-exchange-to-coinmarketcap-id-map--httpsproapi-coinmarketcap-comv1exchangemaplisting-statusactivestart0limit100exchange--v1exchangelistingslatestoperationgetv1exchangelistingslatest--list-all-exchanges-latest--httpsproapi-coinmarketcap-comv1exchangelistingslatestlimit10market-typeno-feesconvertusdexchange--v1exchangemarketpairslatestoperationgetv1exchangemarketpairslatest--get-exchange-market-pairs-latest--httpsproapi-coinmarketcap-comv1exchangemarketpairslatestsluggdaxconvertltcxrpeurexchange--v1exchangequoteslatestoperationgetv1exchangequoteslatest--get-exchange-market-quotes-latest--httpsproapi-coinmarketcap-comv1exchangequoteslatestid216convertusdbtcltceurexchange--v1exchangequoteshistoricaloperationgetv1exchangequoteshistorical--get-exchange-market-quotes-historical--httpsproapi-coinmarketcap-comv1exchangequoteshistoricalid270time-start20180101time-end20180501interval30dcount12global-metrics--v1globalmetricsquoteslatestoperationgetv1globalmetricsquoteslatest--get-aggregate-market-metrics-latest--httpsproapi-coinmarketcap-comv1globalmetricsquoteslatestconvertbtcethltceurglobal-metrics--v1globalmetricsquoteshistoricaloperationgetv1globalmetricsquoteshistorical--get-aggregate-market-metrics-historical--httpsproapi-coinmarketcap-comv1globalmetricsquoteshistoricalintervalmonthlycount100tools--v1toolspriceconversionoperationgetv1toolspriceconversion--price-conversion-tool--httpsproapi-coinmarketcap-comv1toolspriceconversionsymbolbtcamount50convertusdgbpltc-standards-and-conventionseach-http-request-must-contain-the-header-accept-applicationjson--you-should-also-send-an-acceptencoding-deflate-gzip-header-to-receive-data-fast-and-efficiently--endpoint-response-payload-formatall-endpoints-return-data-in-json-format-with-the-results-of-your-query-under-data-if-the-call-is-successful-a-status-object-is-always-included-for-both-successful-calls-and-failures-when-possible--the-status-object-always-includes-the-current-time-on-the-server-when-the-call-was-executed-as-timestamp-the-number-of-api-call-credits-this-call-utilized-as-credit-count-and-the-number-of-milliseconds-it-took-to-process-the-request-as-elapsed--any-details-about-errors-encountered-can-be-found-under-the-error-code-and-error-message--see-errors-and-rate-limitssectionerrorsandratelimits-for-details-on-errors---data-------------status-----timestamp-20180606t075227-273z----error-code-400----error-message-invalid-value-for-id----elapsed-0----credit-count-0---cryptocurrency-exchange-and-fiat-currency-identifiers-cryptocurrencies-may-be-identified-in-endpoints-using-either-the-cryptocurrencys-unique-coinmarketcap-id-as-id-eg--id1-for-bitcoin-or-the-cryptocurrencys-symbol-eg--symbolbtc-for-bitcoin--for-a-current-list-of-supported-cryptocurrencies-use-our-cryptocurrencymap-calloperationgetv1cryptocurrencymap--exchanges-may-be-identified-in-endpoints-using-either-the-exchanges-unique-coinmarketcap-id-as-id-eg--id270-for-binance-or-the-exchanges-web-slug-eg--slugbinance-for-binance--for-a-current-list-of-supported-exchanges-use-our-exchangemap-calloperationgetv1exchangemap--all-fiat-currency-options-use-the-standard-iso-8601httpswww-iso-orgiso8601dateandtimeformat-html-currency-code-eg--usd-for-the-us-dollar--unless-otherwise-stated-endpoints-with-fiat-currency-options-support-these-32-major-currency-codescurrency--currency-codeunited-states-dollar---usdaustralian-dollar---audbrazilian-real-r--brlcanadian-dollar---cadswiss-franc-fr--chfchilean-peso---clpchinese-yuan---cnyczech-koruna-k--czkdanish-krone-kr--dkkeuro---eurbritish-pound---gbphong-kong-dollar---hkdhungarian-forint-ft--hufindonesian-rupiah---rp--idrisraeli-new-shekel---ilsindian-rupee---inrjapanese-yen---jpysouth-korean-won---krwmexican-peso---mxnmalaysian-ringgit-rm--myrnorwegian-krone-kr--noknew-zealand-dollar---nzdphilippine-piso---phppakistani-rupee---pkrpolish-zoty-z--plnrussian-ruble---rubswedish-krona-kr--seksingapore-dollar---sgdthai-baht---thbturkish-lira---trynew-taiwan-dollar---twdsouth-african-rand-r--zarnote-using-coinmarketcap-ids-is-always-recommended-as-cryptocurrency-symbols-are-not-always-unique-and-can-change-with-a-cryptocurrency-rebrand--if-a-symbol-is-used-the-api-will-always-default-to-the-cryptocurrency-with-the-highest-market-cap--you-may-use-the-convenient-map-endpoints-to-quickly-find-the-corresponding-coinmarketcap-id-for-a-cryptocurrency-or-exchange--bundling-api-calls-many-endpoints-support-id-and-cryptofiat-currency-conversion-bundling--this-means-you-can-pass-multiple-commaseparated-values-to-an-endpoint-to-query-or-convert-several-items-at-once--check-the-id-symbol-slug-and-convert-query-parameter-descriptions-in-the-endpoint-documentation-to-see-if-this-is-supported-for-an-endpoint--endpoints-that-support-bundling-return-data-as-an-object-map-instead-of-an-array--each-keyvalue-pair-will-use-the-identifier-you-passed-in-as-the-key-for-example-if-you-passed-symbolbtceth-to-v1cryptocurrencyquoteslatest-you-would-receivedata------btc-------------------eth---------------or-if-you-passed-id11027-you-would-receivedata------1-------------------1027---------------price-conversions-that-are-returned-inside-endpoint-responses-behave-in-the-same-fashion--these-are-enclosed-in-a-quote-object--date-and-time-formats-all-endpoints-that-require-datetime-parameters-allow-timestamps-to-be-passed-in-either-iso-8601httpswww-iso-orgiso8601dateandtimeformat-html-format-eg--20180606t014640z-or-in-unix-time-eg--1528249600--timestamps-that-are-passed-in-iso-8601-format-support-basic-and-extended-notations-if-a-timezone-is-not-included-utc-will-be-the-default--all-timestamps-returned-in-json-payloads-are-returned-in-utc-time-using-humanreadable-iso-8601-format-which-follows-this-pattern-yyyymmddthhmmss-mmmz--the-final--mmm-designates-milliseconds--per-the-iso-8601-spec-the-final-z-is-a-constant-that-represents-utc-time--data-is-collected-recorded-and-reported-in-utc-time-unless-otherwise-specified--versioningthe-professional-api-is-versioned-to-guarantee-new-features-and-updates-are-nonbreaking--the-latest-version-of-this-api-is-v1--errors-and-rate-limits-api-request-throttlinguse-of-the-professional-api-is-subject-to-api-call-rate-limiting-or-request-throttling-that-scales-with-the-usage-tierhttpspro-coinmarketcap-compricing-tied-to-your-api-key--free--trial-plans-are-limited-to-10-calls-a-minute--paid-subscription-tiers-are-limited-to-60-calls-a-minute--custom-enterprise-subscription-tiers-may-have-a-higher-limit--http-status-codesthe-api-uses-standard-http-status-codes-to-indicate-the-success-or-failure-of-an-api-call--400-bad-request-the-server-could-not-process-the-request-likely-due-to-an-invalid-argument--401-unauthorized-the-request-lacks-valid-authentication-credentials-likely-an-issue-with-your-api-key--403-forbidden-the-request-was-rejected-due-to-a-permission-issue-likely-a-restriction-on-the-api-keys-associated-service-plan--429-too-many-requests-the-api-keys-rate-limit-was-exceeded-consider-slowing-down-your-api-request-frequency-if-this-is-a-request-throttling-error--consider-upgrading-your-service-plan-if-you-have-reached-your-monthly-api-credit-limit--500-internal-server-error-an-unexpected-server-issue-was-encountered--error-response-codesa-status-object-is-always-included-in-the-json-response-payload-for-both-successful-calls-and-failures-when-possible--you-may-check-this-object-for-additional-details-about-any-errors-encountered-under-the-error-code-and-error-message-properties--best-practicesthis-section-contains-a-few-recommendations-on-how-to-efficiently-utilize-the-professional-api-for-your-enterprise-application-especially-if-you-already-have-a-large-base-of-users-for-your-application--creating-a-robust-api-integrationwhenever-implementing-any-3rd-party-api-service-its-highly-recommended-to-implement-a-retry-with-exponential-backoff-coding-pattern-for-your-rest-api-call-logic--this-means-if-your-api-call-happens-to-get-rate-limited-http-429-or-encounters-an-unexpected-server-side-condition-http-5xx-your-code-would-automatically-recover-and-try-again-using-an-intelligent-recovery-scheme--you-may-use-one-of-the-many-libraries-available-for-example-a-target-blank-hrefhttpsgithub-comlitlbackoffthis-onea-for-python--implement-a-caching-strategythere-are-standard-legal-data-safeguards-built-into-the-a-hrefhttpspro-coinmarketcap-comuseragreementcommercial-target-blankcommercial-user-termsa-that-application-developers-should-keep-in-mind--these-terms-help-prevent-unauthorized-scraping-and-redistributing-of-cmc-data-but-are-intentionally-worded-to-allow-legitimate-local-caching-of-market-data-to-support-the-operation-of-your-application--if-your-application-has-a-significant-user-base-and-you-are-concerned-with-staying-within-the-call-credit-and-api-throttling-limits-of-your-subscription-plan-consider-implementing-a-data-caching-strategy---for-example-instead-of-making-a-cryptocurrencyquoteslatest-call-every-time-one-of-your-applications-users-needs-to-fetch-market-rates-for-specific-cryptocurrencies-you-could-prefetch-and-cache-the-latest-market-data-for-every-cryptocurrency-in-your-applications-local-database-every-60-seconds--this-would-only-require-1-api-call-cryptocurrencylistingslatestlimit5000-every-60-seconds--then-anytime-one-of-your-applications-users-need-to-load-a-custom-list-of-cryptocurrencies-you-could-simply-pull-this-latest-market-data-from-your-local-cache-without-the-overhead-of-additional-calls--this-kind-of-optimization-is-practical-for-customers-with-large-demanding-user-bases--reach-out-and-upgrade-your-planif-youre-uncertain-how-to-best-implement-the-professional-api-in-your-application-you-can-reach-out-to-apicoinmarketcap-com--if-your-current-or-future-needs-outgrow-our-current-selfserve-subscription-tiers-please-contact-us--well-review-your-needs-and-budget-and-may-be-able-to-tailor-a-custom-enterprise-plan-that-is-right-for-you-
  termsOfService: https://coinmarketcap.com/terms/
  version: 1.0.0
host: pro-api.coinmarketcap.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v1/cryptocurrency/info:
    get:
      summary: Get metadata
      description: |-
        Returns all static metadata for one or more cryptocurrencies including name, symbol, logo, and its various registered URLs.

        **This endpoint is available on the following API plans:**
        - Starter
        - Hobbyist
        - Standard
        - Professional
        - Enterprise

        **Cache / Update frequency:** Static data is updated only as needed, every 30 seconds.
      operationId: getV1CryptocurrencyInfo
      x-api-path-slug: v1cryptocurrencyinfo-get
      parameters:
      - in: query
        name: id
        description: One or more comma-separated CoinMarketCap cryptocurrency IDs
      - in: query
        name: symbol
        description: Alternatively pass one or more comma-separated cryptocurrency
          symbols
      responses:
        200:
          description: OK
      tags:
      - Blockchain
      - Metadata
  /v1/cryptocurrency/listings/latest:
    get:
      summary: List all cryptocurrencies (latest)
      description: "Get a paginated list of all cryptocurrencies with latest market
        data. You can configure this call to sort by market cap or another market
        ranking field. Use the \"convert\" option to return market values in multiple
        fiat and cryptocurrency conversions in the same call.   \n\n\nCryptocurrencies
        are listed by CoinMarketCap Rank by default. You may optionally sort against
        any of the following:\n**name**: The cryptocurrency name.\n**symbol**: The
        cryptocurrency symbol.\n**date_added**: Date cryptocurrency was added to the
        system.\n**market_cap**: market cap (latest trade price x circulating supply).\n**price**:
        latest average trade price across markets.\n**circulating_supply**: approximate
        number of coins currently in circulation.\n**total_supply**: approximate total
        amount of coins in existence right now (minus any coins that have been verifiably
        burned).\n**max_supply**: our best approximation of the maximum amount of
        coins that will ever exist in the lifetime of the currency.\n**num_market_pairs**:
        number of market pairs across all exchanges trading each currency.\n**volume_24h**:
        24 hour trading volume for each currency.\n**percent_change_1h**: 1 hour trading
        price percentage change for each currency.\n**percent_change_24h**: 24 hour
        trading price percentage change for each currency.\n**percent_change_7d**:
        7 day trading price percentage change for each currency.\n\n  **This endpoint
        is available on the following API plans:**\n  - Starter\n  - Hobbyist\n  -
        Standard\n  - Professional\n  - Enterprise\n\n**Cache / Update frequency:**
        Every ~1 minute. \n  \n*NOTE: Use this endpoint if you need a sorted and paginated
        list of cryptocurrencies. If you want to query for market data on a few specific
        cryptocurrencies use /v1/cryptocurrency/quotes/latest which is optimized for
        that purpose. The response data between these endpoints is otherwise the same.*"
      operationId: getV1CryptocurrencyListingsLatest
      x-api-path-slug: v1cryptocurrencylistingslatest-get
      parameters:
      - in: query
        name: convert
        description: Optionally calculate market quotes in up to 32 currencies at
          once by passing a comma-separated list of cryptocurrency or fiat currency
          symbols
      - in: query
        name: cryptocurrency_type
        description: The type of cryptocurrency to include
      - in: query
        name: limit
        description: Optionally specify the number of results to return
      - in: query
        name: sort
        description: What field to sort the list of cryptocurrencies by
      - in: query
        name: sort_dir
        description: The direction in which to order cryptocurrencies against the
          specified sort
      - in: query
        name: start
        description: Optionally offset the start (1-based index) of the paginated
          list of items to return
      responses:
        200:
          description: OK
      tags:
      - Blockchain
      - List
      - ""
      - Cryptocurrencies
      - (latest)
  /v1/cryptocurrency/quotes/latest:
    get:
      summary: Get market quotes (latest)
      description: |-
        Get the latest market quote for 1 or more cryptocurrencies. Use the "convert" option to return market values in multiple fiat and cryptocurrency conversions in the same call.

        **This endpoint is available on the following API plans:**
        - Starter
        - Hobbyist
        - Standard
        - Professional
        - Enterprise

        **Cache / Update frequency:** Every ~1 minute.
      operationId: getV1CryptocurrencyQuotesLatest
      x-api-path-slug: v1cryptocurrencyquoteslatest-get
      parameters:
      - in: query
        name: convert
        description: Optionally calculate market quotes in up to 32 currencies at
          once by passing a comma-separated list of cryptocurrency or fiat currency
          symbols
      - in: query
        name: id
        description: One or more comma-separated cryptocurrency CoinMarketCap IDs
      - in: query
        name: symbol
        description: Alternatively pass one or more comma-separated cryptocurrency
          symbols
      responses:
        200:
          description: OK
      tags:
      - Blockchain
      - Market
      - Quotes
      - (latest)