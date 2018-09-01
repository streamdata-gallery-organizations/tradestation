---
name: TradeStation
x-slug: tradestation
description: Whether you trade stocks, ETFs, options or futures, TradeStation???s
  award-winning tools and brokerage services can give you the confidence to achieve
  your goals.
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/tradestation_logo_285x40.png
x-kinRank: "7"
x-alexaRank: "37688"
tags: TradeStation
created: "2018-08-31"
modified: "2018-08-31"
url: https://raw.githubusercontent.com/streamdata-gallery-organizations/tradestation/master/_listings/tradestation/apis.md
specificationVersion: "0.14"
apis:
- name: Tradestation API - Get Symbol Info
  x-api-slug: datasymbolsymbol-get
  description: |-
    Finds the given symbol and returns a collection of fields describing the
    symbol, its origin exchange, and other pertinant information.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/tradestation_logo_285x40.png
  humanURL: http://www.tradestation.com
  baseURL: https://api.tradestation.com//v2
  tags: Technology, Financial Services, Financial, General Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/tradestation/master/_listings/tradestation/datasymbolsymbol-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/tradestation/master/_listings/tradestation/datasymbolsymbol-get-openapi.md
- name: Tradestation API - Suggest Symbols
  x-api-slug: datasymbolssuggesttext-get
  description: |-
    Suggests symbols semantically based upon partial input of symbol name,
    company name, or description
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/tradestation_logo_285x40.png
  humanURL: http://www.tradestation.com
  baseURL: https://api.tradestation.com//v2
  tags: Technology, Financial Services, Financial, General Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/tradestation/master/_listings/tradestation/datasymbolssuggesttext-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/tradestation/master/_listings/tradestation/datasymbolssuggesttext-get-openapi.md
- name: Tradestation API - Search for Symbols
  x-api-slug: datasymbolssearchcriteria-get
  description: |-
    Searches symbols based upon input criteria including Name, Category and
    Country.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/tradestation_logo_285x40.png
  humanURL: http://www.tradestation.com
  baseURL: https://api.tradestation.com//v2
  tags: Technology, Financial Services, Financial, General Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/tradestation/master/_listings/tradestation/datasymbolssearchcriteria-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/tradestation/master/_listings/tradestation/datasymbolssearchcriteria-get-openapi.md
- name: Tradestation API - Get Quote
  x-api-slug: dataquotesymbols-get
  description: Gets the latest Level2 Quote for the given Symbol
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/tradestation_logo_285x40.png
  humanURL: http://www.tradestation.com
  baseURL: https://api.tradestation.com//v2
  tags: Technology, Financial Services, Financial, General Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/tradestation/master/_listings/tradestation/dataquotesymbols-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/tradestation/master/_listings/tradestation/dataquotesymbols-get-openapi.md
- name: Tradestation API - Stream Quote Changes
  x-api-slug: streamquotechangessymbols-get
  description: |-
    Streams the latest Quote information for the given Symbols. The first chunk in the stream is a full quote snapshot - subsequent chunks only contain fields of the quote object that have changed since the last chunk.

    An invalid symbol name will result in a response of this form - {"Symbol":"BADEXAMPLESYMBOL","Error":"FAILED, EX_INVALID_SYMBOL"}

    If the user is not entitled for the symbol requested, response will be of this form - {"Symbol":"EXAMPLESYMBOL","Error":"FAILED, EX_NOT_ENTITLED"}
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/tradestation_logo_285x40.png
  humanURL: http://www.tradestation.com
  baseURL: https://api.tradestation.com//v2
  tags: Technology, Financial Services, Financial, General Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/tradestation/master/_listings/tradestation/streamquotechangessymbols-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/tradestation/master/_listings/tradestation/streamquotechangessymbols-get-openapi.md
- name: Tradestation API - Stream Quote Snapshots
  x-api-slug: streamquotesnapshotssymbols-get
  description: |-
    Streams the latest Quote for the given Symbols. Each chunk is a full quote object.

    An invalid symbol name will result in a response of this form - {"Symbol":"BADSYMBOLEXAMPLE","Error":"FAILED, EX_INVALID_SYMBOL"}

    If the user is not entitled for the symbol requested, response will be of this form - {"Symbol":"EXAMPLESYMBOL","Error":"FAILED, EX_NOT_ENTITLED"}
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/tradestation_logo_285x40.png
  humanURL: http://www.tradestation.com
  baseURL: https://api.tradestation.com//v2
  tags: Technology, Financial Services, Financial, General Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/tradestation/master/_listings/tradestation/streamquotesnapshotssymbols-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/tradestation/master/_listings/tradestation/streamquotesnapshotssymbols-get-openapi.md
- name: Tradestation API - Stream BarChart - Starting on Date
  x-api-slug: streambarchartsymbolintervalunitstartdate-get
  description: Streams barchart data starting from startDate, each bar filling quantity
    of unit.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/tradestation_logo_285x40.png
  humanURL: http://www.tradestation.com
  baseURL: https://api.tradestation.com//v2
  tags: Technology, Financial Services, Financial, General Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/tradestation/master/_listings/tradestation/streambarchartsymbolintervalunitstartdate-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/tradestation/master/_listings/tradestation/streambarchartsymbolintervalunitstartdate-get-openapi.md
- name: Tradestation API - Stream BarChart - Date Range
  x-api-slug: streambarchartsymbolintervalunitstartdateenddate-get
  description: Streams barchart data starting from startDate to end date, each bar
    filling interval of unit.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/tradestation_logo_285x40.png
  humanURL: http://www.tradestation.com
  baseURL: https://api.tradestation.com//v2
  tags: Technology, Financial Services, Financial, General Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/tradestation/master/_listings/tradestation/streambarchartsymbolintervalunitstartdateenddate-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/tradestation/master/_listings/tradestation/streambarchartsymbolintervalunitstartdateenddate-get-openapi.md
- name: Tradestation API - Stream BarChart - Bars Back
  x-api-slug: streambarchartsymbolintervalunitbarsbacklastdate----get
  description: Streams barchart data starting from a number of bars back from last
    date, each bar filling interval of unit.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/tradestation_logo_285x40.png
  humanURL: http://www.tradestation.com
  baseURL: https://api.tradestation.com//v2
  tags: Technology, Financial Services, Financial, General Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/tradestation/master/_listings/tradestation/streambarchartsymbolintervalunitbarsbacklastdate----get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/tradestation/master/_listings/tradestation/streambarchartsymbolintervalunitbarsbacklastdate----get-openapi.md
- name: Tradestation API - Stream BarChart - Days Back
  x-api-slug: streambarchartsymbolintervalunit-get
  description: Streams barchart data starting from a number of days back from last
    date, each bar filling interval of unit.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/tradestation_logo_285x40.png
  humanURL: http://www.tradestation.com
  baseURL: https://api.tradestation.com//v2
  tags: Technology, Financial Services, Financial, General Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/tradestation/master/_listings/tradestation/streambarchartsymbolintervalunit-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/tradestation/master/_listings/tradestation/streambarchartsymbolintervalunit-get-openapi.md
- name: Tradestation API - Stream Tick Bars
  x-api-slug: streamtickbarssymbolintervalbarsback-get
  description: Streams tick bars data from a number of bars back, each bar returned
    separated by interval number of ticks.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/tradestation_logo_285x40.png
  humanURL: http://www.tradestation.com
  baseURL: https://api.tradestation.com//v2
  tags: Technology, Financial Services, Financial, General Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/tradestation/master/_listings/tradestation/streamtickbarssymbolintervalbarsback-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/tradestation/master/_listings/tradestation/streamtickbarssymbolintervalbarsback-get-openapi.md
- name: Tradestation API - Get all Symbol Lists
  x-api-slug: datasymbollists-get
  description: Gets a list of all Symbol Lists
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/tradestation_logo_285x40.png
  humanURL: http://www.tradestation.com
  baseURL: https://api.tradestation.com//v2
  tags: Technology, Financial Services, Financial, General Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/tradestation/master/_listings/tradestation/datasymbollists-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/tradestation/master/_listings/tradestation/datasymbollists-get-openapi.md
- name: Tradestation API - Get Symbol List
  x-api-slug: datasymbollistssymbol-list-id-get
  description: Gets a specific Symbol List
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/tradestation_logo_285x40.png
  humanURL: http://www.tradestation.com
  baseURL: https://api.tradestation.com//v2
  tags: Technology, Financial Services, Financial, General Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/tradestation/master/_listings/tradestation/datasymbollistssymbol-list-id-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/tradestation/master/_listings/tradestation/datasymbollistssymbol-list-id-get-openapi.md
- name: Tradestation API - Get Symbols in a Symbol List
  x-api-slug: datasymbollistssymbol-list-idsymbols-get
  description: Gets the Symbols for a specific Symbol List
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/tradestation_logo_285x40.png
  humanURL: http://www.tradestation.com
  baseURL: https://api.tradestation.com//v2
  tags: Technology, Financial Services, Financial, General Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/tradestation/master/_listings/tradestation/datasymbollistssymbol-list-idsymbols-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/tradestation/master/_listings/tradestation/datasymbollistssymbol-list-idsymbols-get-openapi.md
- name: Tradestation API - Get User Accounts
  x-api-slug: usersuser-idaccounts-get
  description: Returns all accounts for the given user
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/tradestation_logo_285x40.png
  humanURL: http://www.tradestation.com
  baseURL: https://api.tradestation.com//v2
  tags: Technology, Financial Services, Financial, General Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/tradestation/master/_listings/tradestation/usersuser-idaccounts-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/tradestation/master/_listings/tradestation/usersuser-idaccounts-get-openapi.md
- name: Tradestation API - Get Account Balances
  x-api-slug: accountsaccount-keysbalances-get
  description: Returns the Balance for the given accounts
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/tradestation_logo_285x40.png
  humanURL: http://www.tradestation.com
  baseURL: https://api.tradestation.com//v2
  tags: Technology, Financial Services, Financial, General Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/tradestation/master/_listings/tradestation/accountsaccount-keysbalances-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/tradestation/master/_listings/tradestation/accountsaccount-keysbalances-get-openapi.md
- name: Tradestation API - Get Account Positions
  x-api-slug: accountsaccount-keyspositions-get
  description: Returns the Positions for the given accounts
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/tradestation_logo_285x40.png
  humanURL: http://www.tradestation.com
  baseURL: https://api.tradestation.com//v2
  tags: Technology, Financial Services, Financial, General Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/tradestation/master/_listings/tradestation/accountsaccount-keyspositions-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/tradestation/master/_listings/tradestation/accountsaccount-keyspositions-get-openapi.md
- name: Tradestation API - Get Account Orders
  x-api-slug: accountsaccount-keysorders-get
  description: |-
    Returns the Orders for the given accounts sorted descending, most recent order first.

    #### Stateless Connection
    Since the web-API provides a stateless connection, it only supports fetching the current state of Orders. If it is needed to display the intermediate state changes, it should be executed at client level.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/tradestation_logo_285x40.png
  humanURL: http://www.tradestation.com
  baseURL: https://api.tradestation.com//v2
  tags: Technology, Financial Services, Financial, General Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/tradestation/master/_listings/tradestation/accountsaccount-keysorders-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/tradestation/master/_listings/tradestation/accountsaccount-keysorders-get-openapi.md
- name: Tradestation API - Confirm Order
  x-api-slug: ordersconfirm-post
  description: |-
    Returns estimated cost and commission information for an order without the order actually being placed. The fields that are returned in the response depend on the order type.
    The following shows the different fields that will be returned.

    **Base Confirmation**  (All confirmations will have these fields)
    * Route
    * Duration
    * Account
    * SummaryMessage
    * OrderConfirmId

    **Equity Confirmation** (Base Confirmation fields + the following)
    * EstimatedPrice
    * EstimatedPriceDisplay
    * EstimatedCost
    * EstimatedCostDisplay
    * EstimatedCommission
    * EstimatedCommissionDisplay
    * DebitCreditEstimatedCost
    * DebitCreditEstimatedCostDisplay

    **Forex Confirmation** (Base Confirmation fields + the following)
    * BaseCurrency
    * CounterCurrency
    * InitialMarginDisplay

    **Futures Confirmation** (Base Confirmation fields + the following)
    * ProductCurrency
    * AccountCurrency
    * EstimatedCost
    * EstimatedPrice
    * EstimatedPriceDisplay
    * InitialMarginDisplay
    * EstimatedCommission
    * EstimatedCommissionDisplay
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/tradestation_logo_285x40.png
  humanURL: http://www.tradestation.com
  baseURL: https://api.tradestation.com//v2
  tags: Technology, Financial Services, Financial, General Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/tradestation/master/_listings/tradestation/ordersconfirm-post-openapi.md
- name: Tradestation API - Submit Order
  x-api-slug: orders-post
  description: Submits 1 or more orders
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/tradestation_logo_285x40.png
  humanURL: http://www.tradestation.com
  baseURL: https://api.tradestation.com//v2
  tags: Technology, Financial Services, Financial, General Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/tradestation/master/_listings/tradestation/orders-post-openapi.md
- name: Tradestation API - Cancel Order
  x-api-slug: ordersorder-id-delete
  description: Cancels an open order. You cannot cancel an order that has been filled.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/tradestation_logo_285x40.png
  humanURL: http://www.tradestation.com
  baseURL: https://api.tradestation.com//v2
  tags: Technology, Financial Services, Financial, General Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/tradestation/master/_listings/tradestation/ordersorder-id-delete-openapi.md
- name: Tradestation API - Update Order
  x-api-slug: ordersorder-id-put
  description: |-
    Updates (Cancels & Replaces) an open order. You cannot update an order
    that has been filled.

    Rules:

     | Original order type              | Fields to update                 | Can only change order type to |
     | -------------------------------- | -------------------------------- | ----------------------------- |
     | Limit Orders                     | Quantity, Stop Price             | Market                        |
     | Stop Orders                      | Quantity, Stop Price             | Market                        |
     | Stop Limit Orders                | Quantity, Stop Price, Stop Limit | Market                        |
     | Stop Market Trailing Stop Orders | Quantity                         | Market                        |
     | Trailing Stop Orders             | Offset type and value            | Market                        |
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/tradestation_logo_285x40.png
  humanURL: http://www.tradestation.com
  baseURL: https://api.tradestation.com//v2
  tags: Technology, Financial Services, Financial, General Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/tradestation/master/_listings/tradestation/ordersorder-id-put-openapi.md
- name: Tradestation API - Confirm Group Order
  x-api-slug: ordersgroupsconfirm-post
  description: |-
    Returns estimated cost and commission information for a group of orders (OCO, BRK) without the orders actually being placed

    **Base Confirmation**  (All confirmations will have these fields)
    * Route
    * Duration
    * Account
    * SummaryMessage
    * OrderConfirmId

    **Equity Confirmation** (Base Confirmation fields + the following)
    * EstimatedPrice
    * EstimatedPriceDisplay
    * EstimatedCost
    * EstimatedCostDisplay
    * EstimatedCommission
    * EstimatedCommissionDisplay

    **Forex Confirmation** (Base Confirmation fields + the following)
    * BaseCurrency
    * CounterCurrency
    * InitialMarginDisplay

    **Futures Confirmation** (Base Confirmation fields + the following)
    * ProductCurrency
    * AccountCurrency
    * EstimatedCost
    * EstimatedPrice
    * EstimatedPriceDisplay
    * InitialMarginDisplay
    * EstimatedCommission
    * EstimatedCommissionDisplay
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/tradestation_logo_285x40.png
  humanURL: http://www.tradestation.com
  baseURL: https://api.tradestation.com//v2
  tags: Technology, Financial Services, Financial, General Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/tradestation/master/_listings/tradestation/ordersgroupsconfirm-post-openapi.md
- name: Tradestation API - Submit Group Order
  x-api-slug: ordersgroups-post
  description: "Submits a group order such as Bracket and OCO Orders.\n\n#### Order
    Cancels Order (OCO)\nAn OCO order is a group of orders whereby if one of the orders
    is filled\nor partially-filled, then all of the other orders in the group are\ncancelled.\n\n####
    Bracket OCO Orders\nA bracket order is a special instance of an OCO (Order Cancel
    Order).\nBracket orders are used to exit an existing position. They are designed\nto
    limit loss and lock in profit by ???bracketing??? an order with a\nsimultaneous
    stop and limit order.\n\nBracket orders are limited so that the orders are all
    for the same\nsymbol and are on the same side of the market (either all to sell
    or\nall to cover), and they are restricted to closing transactions.\n\nThe reason
    that they follow these rules is because the orders need to be\nable to auto decrement
    when a partial fill occurs with one of the orders.\nFor example, if the customer
    has a sell limit order for 1000 shares and\na sell stop order for 1000 shares,
    and the limit order is partially\nfilled for 500 shares, then the customer would
    want the stop to remain\nopen, but it should automatically decrement the order
    to 500 shares to\nmatch the remaining open position.\n\n### Errors\nWhen a submitted
    order fails, it can be seen in two different ways:\n-\tImmediately rejected during
    submit to the Orders API with a 400 HTTP status code.\n-\tAccepted by the API
    with a 200 HTTP status code, but you will see the order with a status of ???REJ???
    (rejected) when you fetch the Order from the /v2/accounts/{id}/orders API\n\n####
    NOTE\nWhen a group order is submitted, the order execution system treats each
    sibling order as an individual order. Thus, the system does not validate that
    each order has the same Quantity, and currently it is not able to update a bracket
    order as one transaction, instead you must update each order within a bracket.\n\nIn
    order to prevent errors, please validate the data on the client side."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/tradestation_logo_285x40.png
  humanURL: http://www.tradestation.com
  baseURL: https://api.tradestation.com//v2
  tags: Technology, Financial Services, Financial, General Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/tradestation/master/_listings/tradestation/ordersgroups-post-openapi.md
- name: Tradestation API - Request Available Activation Triggers
  x-api-slug: orderexecutionactivationtriggers-get
  description: To place orders with activation triggers, a valid TriggerKey must be
    sent with the order.  This resource provides the available trigger methods with
    their corresponding key.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/tradestation_logo_285x40.png
  humanURL: http://www.tradestation.com
  baseURL: https://api.tradestation.com//v2
  tags: Technology, Financial Services, Financial, General Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/tradestation/master/_listings/tradestation/orderexecutionactivationtriggers-get-openapi.md
x-common:
- type: x-website
  url: http://www.tradestation.com
- type: x-api-gallery
  url: http://tigertext.api.gallery.streamdata.io
- type: x-api-stack
  url: http://tradestation.stack.network
- type: x-crunchbase
  url: https://crunchbase.com/organization/tradestation-technologies
- type: x-developer
  url: https://developer.tradestation.com/
- type: x-documentation
  url: https://tradestation.github.io/api-docs/
- type: x-faq
  url: https://www.tradestation.com/faq/
- type: x-github
  url: https://github.com/tradestation
- type: x-openapi
  url: https://tradestation.github.io/api-docs/swagger.json
- type: x-pricing
  url: https://www.tradestation.com/pricing/
- type: x-twitter
  url: https://twitter.com/TradeStation
- type: x-website
  url: https://www.tradestation.com
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---