---
swagger: "2.0"
x-collection-name: TradeStation
x-complete: 0
info:
  title: TradeStation Get Quote
  description: Gets the latest Level2 Quote for the given Symbol
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