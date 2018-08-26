{
  "info": {
    "name": "TradeStation Stream BarChart - Bars Back",
    "_postman_id": "a9ac81b6-f670-41d1-b815-8a1dab3cfc49",
    "description": "Streams barchart data starting from a number of bars back from last date, each bar filling interval of unit.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Symbol",
      "item": [
        {
          "id": "d6c13d84-0af9-465c-a6d0-887b8e01c8ef",
          "name": "getSymbol",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.tradestation.com",
              "path": [
                "v2",
                "data/symbol/:symbol"
              ],
              "query": [
                {
                  "key": "access_token",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "symbol",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Finds the given symbol and returns a collection of fields describing the\nsymbol, its origin exchange, and other pertinant information."
          },
          "response": [
            {
              "status": "Successful response",
              "code": 200,
              "name": "Response_200",
              "id": "ffd54445-e520-4afa-a109-87c30c6c2a05"
            }
          ]
        }
      ]
    },
    {
      "name": "Suggest",
      "item": [
        {
          "id": "2ee2b326-afc4-4b23-8518-ccc34aafbdb5",
          "name": "suggestsymbols",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.tradestation.com",
              "path": [
                "v2",
                "data/symbols/suggest/:text"
              ],
              "query": [
                {
                  "key": "$filter",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "$top",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "access_token",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "text",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Suggests symbols semantically based upon partial input of symbol name,\ncompany name, or description"
          },
          "response": [
            {
              "status": "Successful response",
              "code": 200,
              "name": "Response_200",
              "id": "c381d41d-f801-4225-bc86-dbe04437a3dd"
            }
          ]
        }
      ]
    },
    {
      "name": "SearchSymbols",
      "item": [
        {
          "id": "c7918232-8393-41ee-90ae-c7037d56b47d",
          "name": "searchSymbols",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.tradestation.com",
              "path": [
                "v2",
                "data/symbols/search/:criteria"
              ],
              "query": [
                {
                  "key": "access_token",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "criteria",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Searches symbols based upon input criteria including Name, Category and\nCountry."
          },
          "response": [
            {
              "status": "Successful response",
              "code": 200,
              "name": "Response_200",
              "id": "7d1b44d1-3329-47c8-adab-eac1409906c3"
            }
          ]
        }
      ]
    },
    {
      "name": "Quote",
      "item": [
        {
          "id": "dae69faa-2739-4c32-a10c-a0beac7a6c2f",
          "name": "getQuotes",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.tradestation.com",
              "path": [
                "v2",
                "data/quote/:symbols"
              ],
              "query": [
                {
                  "key": "access_token",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "symbols",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Gets the latest Level2 Quote for the given Symbol"
          },
          "response": [
            {
              "status": "Successful response",
              "code": 200,
              "name": "Response_200",
              "id": "f5ea4167-799d-4424-8421-340b54669ae4"
            }
          ]
        }
      ]
    },
    {
      "name": "Stream",
      "item": [
        {
          "id": "c2b6e8e9-4b29-49b3-bc6b-b7beff8fe646",
          "name": "streamQuotesChanges",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.tradestation.com",
              "path": [
                "v2",
                "stream/quote/changes/:symbols"
              ],
              "query": [
                {
                  "key": "access_token",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "symbols",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Transfer-Encoding",
                "value": "{}",
                "description": "a header with the value of `Chunked` must be passed to streaming resources",
                "disabled": false
              },
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Streams the latest Quote information for the given Symbols. The first chunk in the stream is a full quote snapshot - subsequent chunks only contain fields of the quote object that have changed since the last chunk.\n\nAn invalid symbol name will result in a response of this form - {\"Symbol\":\"BADEXAMPLESYMBOL\",\"Error\":\"FAILED, EX_INVALID_SYMBOL\"}\n\nIf the user is not entitled for the symbol requested, response will be of this form - {\"Symbol\":\"EXAMPLESYMBOL\",\"Error\":\"FAILED, EX_NOT_ENTITLED\"}"
          },
          "response": [
            {
              "status": "Successful response",
              "code": 200,
              "name": "Response_200",
              "id": "82d7281f-49af-4ccc-8ee5-2a61882eaad1"
            }
          ]
        },
        {
          "id": "a836d4e1-4748-4be1-b010-9c9f718db16f",
          "name": "streamQuotesSnapshots",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.tradestation.com",
              "path": [
                "v2",
                "stream/quote/snapshots/:symbols"
              ],
              "query": [
                {
                  "key": "access_token",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "symbols",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Streams the latest Quote for the given Symbols. Each chunk is a full quote object.\n\nAn invalid symbol name will result in a response of this form - {\"Symbol\":\"BADSYMBOLEXAMPLE\",\"Error\":\"FAILED, EX_INVALID_SYMBOL\"}\n\nIf the user is not entitled for the symbol requested, response will be of this form - {\"Symbol\":\"EXAMPLESYMBOL\",\"Error\":\"FAILED, EX_NOT_ENTITLED\"}"
          },
          "response": [
            {
              "status": "Successful response",
              "code": 200,
              "name": "Response_200",
              "id": "99cf2a82-dfb5-4485-91cd-583bba54c75f"
            }
          ]
        },
        {
          "id": "3d1292bd-2598-4c27-9686-ee9d766dec58",
          "name": "streamBarchartsFromStartDate",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.tradestation.com",
              "path": [
                "v2",
                "stream/barchart/:symbol/:interval/:unit/:startDate"
              ],
              "query": [
                {
                  "key": "access_token",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "SessionTemplate",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "interval",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "startDate",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "symbol",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "unit",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Streams barchart data starting from startDate, each bar filling quantity of unit."
          },
          "response": [
            {
              "status": "Successful response",
              "code": 200,
              "name": "Response_200",
              "id": "7371eba9-80a5-4f10-af9e-f4197b4df9c2"
            }
          ]
        },
        {
          "id": "04a7ad7d-78f4-4a4f-a11e-75bb19003e13",
          "name": "streamBarchartsFromStartDateToEndDate",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.tradestation.com",
              "path": [
                "v2",
                "stream/barchart/:symbol/:interval/:unit/:startDate/:endDate"
              ],
              "query": [
                {
                  "key": "access_token",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "SessionTemplate",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "endDate",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "interval",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "startDate",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "symbol",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "unit",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Streams barchart data starting from startDate to end date, each bar filling interval of unit."
          },
          "response": [
            {
              "status": "Successful response",
              "code": 200,
              "name": "Response_200",
              "id": "d7be9a8a-c373-455d-8487-078d55a4adcc"
            }
          ]
        },
        {
          "id": "82354a3f-1cdb-490e-8fe8-9319fcd164fd",
          "name": "streamBarchartsBarsBack",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.tradestation.com",
              "path": [
                "v2",
                "stream/barchart/:symbol/:interval/:unit/:barsBack/:lastDate/..."
              ],
              "query": [
                {
                  "key": "access_token",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "SessionTemplate",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "barsBack",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "interval",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "lastDate",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "symbol",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "unit",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Streams barchart data starting from a number of bars back from last date, each bar filling interval of unit."
          },
          "response": [
            {
              "status": "Successful response",
              "code": 200,
              "name": "Response_200",
              "id": "3be79722-8bf1-4720-bfbd-30f2a7d3a70a"
            }
          ]
        }
      ]
    }
  ]
}