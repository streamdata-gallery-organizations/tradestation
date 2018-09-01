---
swagger: "2.0"
x-collection-name: TradeStation
x-complete: 0
info:
  title: TradeStation Get Account Positions
  description: Returns the Positions for the given accounts
  termsOfService: http://elasticbeanstalk-us-east-1-525856068889.s3.amazonaws.com/wp-content/uploads/2014/03/Guidelines_For_Acceptance.pdf
  contact:
    name: TradeStation API Team
    url: https://developer.tradestation.com/webapi
    email: webapi@tradestation.com
  version: 1.0.0
host: api.tradestation.com
basePath: /v2
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /data/symbol/{symbol}:
    get:
      summary: Get Symbol Info
      description: |-
        Finds the given symbol and returns a collection of fields describing the
        symbol, its origin exchange, and other pertinant information.
      operationId: getSymbol
      x-api-path-slug: datasymbolsymbol-get
      parameters:
      - in: query
        name: access_token
        description: A valid OAuth2 token used to authorize access to the resource
      - in: path
        name: symbol
        description: Symbol to lookup
      responses:
        200:
          description: Successful response
      tags:
      - Symbol
      - Info
  /data/symbols/suggest/{text}:
    get:
      summary: Suggest Symbols
      description: |-
        Suggests symbols semantically based upon partial input of symbol name,
        company name, or description
      operationId: suggestsymbols
      x-api-path-slug: datasymbolssuggesttext-get
      parameters:
      - in: query
        name: $filter
        description: An OData filter to apply to the results
      - in: query
        name: $top
        description: The top number of results to return
      - in: query
        name: access_token
        description: A valid OAuth2 token used to authorize access to the resource
      - in: path
        name: text
        description: Symbol text for suggestion
      responses:
        200:
          description: Successful response
      tags:
      - Suggest
      - Symbols
  /data/symbols/search/{criteria}:
    get:
      summary: Search for Symbols
      description: |-
        Searches symbols based upon input criteria including Name, Category and
        Country.
      operationId: searchSymbols
      x-api-path-slug: datasymbolssearchcriteria-get
      parameters:
      - in: query
        name: access_token
        description: A valid OAuth2 token used to authorize access to the resource
      - in: path
        name: criteria
        description: 'Criteria are represented as Key/value pairs (`&` separated):`N`:
          Name of Symbol'
      responses:
        200:
          description: Successful response
      tags:
      - SearchSymbols
  /data/quote/{symbols}:
    get:
      summary: Get Quote
      description: Gets the latest Level2 Quote for the given Symbol
      operationId: getQuotes
      x-api-path-slug: dataquotesymbols-get
      parameters:
      - in: query
        name: access_token
        description: A valid OAuth2 token used to authorize access to the resource
      - in: path
        name: symbols
        description: 1 or more Symbol Names (comma-separated)
      responses:
        200:
          description: Successful response
      tags:
      - Quote
  /stream/quote/changes/{symbols}:
    get:
      summary: Stream Quote Changes
      description: |-
        Streams the latest Quote information for the given Symbols. The first chunk in the stream is a full quote snapshot - subsequent chunks only contain fields of the quote object that have changed since the last chunk.

        An invalid symbol name will result in a response of this form - {"Symbol":"BADEXAMPLESYMBOL","Error":"FAILED, EX_INVALID_SYMBOL"}

        If the user is not entitled for the symbol requested, response will be of this form - {"Symbol":"EXAMPLESYMBOL","Error":"FAILED, EX_NOT_ENTITLED"}
      operationId: streamQuotesChanges
      x-api-path-slug: streamquotechangessymbols-get
      parameters:
      - in: query
        name: access_token
        description: A valid OAuth2 token used to authorize access to the resource
      - in: path
        name: symbols
        description: 1 or more Symbol Names (comma-separated)
      - in: header
        name: Transfer-Encoding
        description: a header with the value of `Chunked` must be passed to streaming
          resources
      responses:
        200:
          description: Successful response
      tags:
      - Stream
      - Quote
      - Changes
  /stream/quote/snapshots/{symbols}:
    get:
      summary: Stream Quote Snapshots
      description: |-
        Streams the latest Quote for the given Symbols. Each chunk is a full quote object.

        An invalid symbol name will result in a response of this form - {"Symbol":"BADSYMBOLEXAMPLE","Error":"FAILED, EX_INVALID_SYMBOL"}

        If the user is not entitled for the symbol requested, response will be of this form - {"Symbol":"EXAMPLESYMBOL","Error":"FAILED, EX_NOT_ENTITLED"}
      operationId: streamQuotesSnapshots
      x-api-path-slug: streamquotesnapshotssymbols-get
      parameters:
      - in: query
        name: access_token
        description: A valid OAuth2 token used to authorize access to the resource
      - in: path
        name: symbols
        description: 1 or more Symbol Names (comma-separated)
      responses:
        200:
          description: Successful response
      tags:
      - Stream
      - Quote
      - Snapshots
  /stream/barchart/{symbol}/{interval}/{unit}/{startDate}:
    get:
      summary: Stream BarChart - Starting on Date
      description: Streams barchart data starting from startDate, each bar filling
        quantity of unit.
      operationId: streamBarchartsFromStartDate
      x-api-path-slug: streambarchartsymbolintervalunitstartdate-get
      parameters:
      - in: query
        name: access_token
        description: A valid OAuth2 token used to authorize access to the resource
      - in: path
        name: interval
        description: Interval that each bar will consist of
      - in: query
        name: SessionTemplate
        description: United States (US) stock market session templates, that extend
          bars returned to include those outside of the regular trading session
      - in: path
        name: startDate
        description: The starting date to begin streaming bars from
      - in: path
        name: symbol
        description: A Symbol Name
      - in: path
        name: unit
        description: Unit of time for each bar interval
      responses:
        200:
          description: Successful response
      tags:
      - Stream
      - BarChart
      - '-'
      - Starting
      - "On"
      - Date
  /stream/barchart/{symbol}/{interval}/{unit}/{startDate}/{endDate}:
    get:
      summary: Stream BarChart - Date Range
      description: Streams barchart data starting from startDate to end date, each
        bar filling interval of unit.
      operationId: streamBarchartsFromStartDateToEndDate
      x-api-path-slug: streambarchartsymbolintervalunitstartdateenddate-get
      parameters:
      - in: query
        name: access_token
        description: A valid OAuth2 token used to authorize access to the resource
      - in: path
        name: endDate
        description: The ending date for bars streamed
      - in: path
        name: interval
        description: Interval that each bar will consist of
      - in: query
        name: SessionTemplate
        description: United States (US) stock market session templates, that extend
          bars returned to include those outside of the regular trading session
      - in: path
        name: startDate
        description: The starting date to begin streaming bars from
      - in: path
        name: symbol
        description: A Symbol Name
      - in: path
        name: unit
        description: Unit of time for each bar interval
      responses:
        200:
          description: Successful response
      tags:
      - Stream
      - BarChart
      - '-'
      - Date
      - Range
  /stream/barchart/{symbol}/{interval}/{unit}/{barsBack}/{lastDate}/...:
    get:
      summary: Stream BarChart - Bars Back
      description: Streams barchart data starting from a number of bars back from
        last date, each bar filling interval of unit.
      operationId: streamBarchartsBarsBack
      x-api-path-slug: streambarchartsymbolintervalunitbarsbacklastdate----get
      parameters:
      - in: query
        name: access_token
        description: A valid OAuth2 token used to authorize access to the resource
      - in: path
        name: barsBack
        description: The number of bars to stream, going back from time 00:00:00 of
          the day specified in lastDate
      - in: path
        name: interval
        description: Interval that each bar will consist of
      - in: path
        name: lastDate
        description: The date to use as the end point when getting bars back
      - in: query
        name: SessionTemplate
        description: United States (US) stock market session templates, that extend
          bars returned to include those outside of the regular trading session
      - in: path
        name: symbol
        description: A Symbol Name
      - in: path
        name: unit
        description: Unit of time for each bar interval
      responses:
        200:
          description: Successful response
      tags:
      - Stream
      - BarChart
      - '-'
      - Bars
      - Back
  /stream/barchart/{symbol}/{interval}/{unit}:
    get:
      summary: Stream BarChart - Days Back
      description: Streams barchart data starting from a number of days back from
        last date, each bar filling interval of unit.
      operationId: streamBarchartsDaysBack
      x-api-path-slug: streambarchartsymbolintervalunit-get
      parameters:
      - in: query
        name: access_token
        description: A valid OAuth2 token used to authorize access to the resource
      - in: query
        name: daysBack
        description: The number of bars to stream, going back from time 00:00:00 of
          the day specified in lastDate
      - in: path
        name: interval
        description: Interval that each bar will consist of
      - in: query
        name: lastDate
        description: The date to use as the end point when getting days back
      - in: query
        name: SessionTemplate
        description: United States (US) stock market session templates, that extend
          bars returned to include those outside of the regular trading session
      - in: path
        name: symbol
        description: A Symbol Name
      - in: path
        name: unit
        description: Unit of time for each bar interval
      responses:
        200:
          description: Successful response
      tags:
      - Stream
      - BarChart
      - '-'
      - Days
      - Back
  /stream/tickbars/{symbol}/{interval}/{barsBack}:
    get:
      summary: Stream Tick Bars
      description: Streams tick bars data from a number of bars back, each bar returned
        separated by interval number of ticks.
      operationId: streamTickBars
      x-api-path-slug: streamtickbarssymbolintervalbarsback-get
      parameters:
      - in: query
        name: access_token
        description: A valid OAuth2 token used to authorize access to the resource
      - in: path
        name: barsBack
        description: The number of bars to stream, going back from current time
      - in: path
        name: interval
        description: Interval for each bar returned (in ticks)
      - in: path
        name: symbol
        description: A Symbol Name
      responses:
        200:
          description: Successful response
      tags:
      - Stream
      - Tick
      - Bars
  /data/symbollists:
    get:
      summary: Get all Symbol Lists
      description: Gets a list of all Symbol Lists
      operationId: getSymbolLists
      x-api-path-slug: datasymbollists-get
      parameters:
      - in: query
        name: access_token
        description: A valid OAuth2 token used to authorize access to the resource
      responses:
        200:
          description: Successful response
      tags:
      - Symbol
      - Lists
  /data/symbollists/{symbol_list_id}:
    get:
      summary: Get Symbol List
      description: Gets a specific Symbol List
      operationId: getSymbolListByID
      x-api-path-slug: datasymbollistssymbol-list-id-get
      parameters:
      - in: query
        name: access_token
        description: A valid OAuth2 token used to authorize access to the resource
      - in: path
        name: symbol_list_id
        description: A valid Symbol List ID
      responses:
        200:
          description: Successful response
      tags:
      - Symbol
      - List
  /data/symbollists/{symbol_list_id}/symbols:
    get:
      summary: Get Symbols in a Symbol List
      description: Gets the Symbols for a specific Symbol List
      operationId: getSymbolListSymbolsByID
      x-api-path-slug: datasymbollistssymbol-list-idsymbols-get
      parameters:
      - in: query
        name: access_token
        description: A valid OAuth2 token used to authorize access to the resource
      - in: path
        name: symbol_list_id
        description: A valid Symbol List ID
      responses:
        200:
          description: Successful response
      tags:
      - Symbols
      - In
      - Symbol
      - List
  /users/{user_id}/accounts:
    get:
      summary: Get User Accounts
      description: Returns all accounts for the given user
      operationId: getAccountsByUserID
      x-api-path-slug: usersuser-idaccounts-get
      parameters:
      - in: query
        name: access_token
        description: A valid OAuth2 token used to authorize access to the resource
      - in: path
        name: user_id
        description: User ID for Accounts Lookup
      responses:
        200:
          description: Successful response
      tags:
      - User
      - Accounts
  /accounts/{account_keys}/balances:
    get:
      summary: Get Account Balances
      description: Returns the Balance for the given accounts
      operationId: getBalancesByAccounts
      x-api-path-slug: accountsaccount-keysbalances-get
      parameters:
      - in: query
        name: access_token
        description: A valid OAuth2 token used to authorize access to the resource
      - in: path
        name: account_keys
        description: 1 or more Account Keys
      responses:
        200:
          description: Successful response
      tags:
      - Account
      - Balances
  /accounts/{account_keys}/positions:
    get:
      summary: Get Account Positions
      description: Returns the Positions for the given accounts
      operationId: getPositionsByAccounts
      x-api-path-slug: accountsaccount-keyspositions-get
      parameters:
      - in: query
        name: $filter
        description: An OData v2
      - in: query
        name: access_token
        description: A valid OAuth2 token used to authorize access to the resource
      - in: path
        name: account_keys
        description: 1 or more Account Keys
      responses:
        200:
          description: Successful response
      tags:
      - Account
      - Positions
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---