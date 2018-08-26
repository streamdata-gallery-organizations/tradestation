{
  "info": {
    "name": "TradeStation Get Account Orders",
    "_postman_id": "34ca04e1-753f-4be2-bc2e-f3e0a21578b5",
    "description": "Returns the Orders for the given accounts sorted descending, most recent order first.\n\n#### Stateless Connection\nSince the web-API provides a stateless connection, it only supports fetching the current state of Orders. If it is needed to display the intermediate state changes, it should be executed at client level.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Symbol",
      "item": [
        {
          "id": "46719734-4eb6-4576-a61d-343cd4043e8d",
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
              "id": "26411b11-4487-4ef5-b417-d2c8895c72fc"
            }
          ]
        },
        {
          "id": "248c2669-797e-49ec-a99f-0261c0cba614",
          "name": "getSymbolLists",
          "request": {
            "url": "http://api.tradestation.com/v2/data/symbollists?access_token=%7B%7D",
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
            "description": "Gets a list of all Symbol Lists"
          },
          "response": [
            {
              "status": "Successful response",
              "code": 200,
              "name": "Response_200",
              "id": "1e897b72-10d3-4699-9ad2-5aeb58a3e55f"
            }
          ]
        },
        {
          "id": "566ac159-b5d3-4623-bc17-791f37d71504",
          "name": "getSymbolListByID",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.tradestation.com",
              "path": [
                "v2",
                "data/symbollists/:symbol_list_id"
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
                  "id": "symbol_list_id",
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
            "description": "Gets a specific Symbol List"
          },
          "response": [
            {
              "status": "Successful response",
              "code": 200,
              "name": "Response_200",
              "id": "15196d13-7bde-41cf-9742-ecb4e45d7596"
            }
          ]
        }
      ]
    },
    {
      "name": "Suggest",
      "item": [
        {
          "id": "f6eb6da9-738e-4a40-980e-e271fbcb7b3f",
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
              "id": "842820eb-1a9a-4232-b854-2cda793e9b59"
            }
          ]
        }
      ]
    },
    {
      "name": "SearchSymbols",
      "item": [
        {
          "id": "2e09cd64-1a67-41ea-add5-d7859fd543e4",
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
              "id": "07e034d7-c940-4fe0-b73b-a0415431b4d6"
            }
          ]
        }
      ]
    },
    {
      "name": "Quote",
      "item": [
        {
          "id": "fd43a992-30e8-4280-9840-9a3881d0fc11",
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
              "id": "ff3572bb-4911-43bb-bbf5-0cad65a37724"
            }
          ]
        }
      ]
    },
    {
      "name": "Stream",
      "item": [
        {
          "id": "f26ed08f-672b-462e-83ff-2228f30ac4aa",
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
              "id": "48db76d7-022a-4191-a125-8ddbec1c6d0f"
            }
          ]
        },
        {
          "id": "c74de5bf-593e-45e2-852a-af98b060e17a",
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
              "id": "4045d3cb-8f80-4aed-9cff-37e8e2c5f9c9"
            }
          ]
        },
        {
          "id": "53b39be2-720d-48a0-b39c-cd4eb64f5a61",
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
              "id": "c5c54b1b-e2da-482b-a835-3090faa623db"
            }
          ]
        },
        {
          "id": "05eed388-c67f-48e4-acf4-aa5ae60d770a",
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
              "id": "0fa85437-63b0-4852-a645-2f8f29e708fd"
            }
          ]
        },
        {
          "id": "031009b2-ab66-414b-a007-49e3f42cfc4d",
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
              "id": "6c8fbd34-b334-497b-8f0a-223c1ac8023d"
            }
          ]
        },
        {
          "id": "4ee234c4-2f01-4119-a845-3d6ead2dc6c0",
          "name": "streamBarchartsDaysBack",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.tradestation.com",
              "path": [
                "v2",
                "stream/barchart/:symbol/:interval/:unit"
              ],
              "query": [
                {
                  "key": "access_token",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "daysBack",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "lastDate",
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
            "description": "Streams barchart data starting from a number of days back from last date, each bar filling interval of unit."
          },
          "response": [
            {
              "status": "Successful response",
              "code": 200,
              "name": "Response_200",
              "id": "2dca3ba4-6084-4b80-9926-abba6a182cce"
            }
          ]
        },
        {
          "id": "c238b897-9d14-45a5-b7bb-df842dee54ba",
          "name": "streamTickBars",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.tradestation.com",
              "path": [
                "v2",
                "stream/tickbars/:symbol/:interval/:barsBack"
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
            "description": "Streams tick bars data from a number of bars back, each bar returned separated by interval number of ticks."
          },
          "response": [
            {
              "status": "Successful response",
              "code": 200,
              "name": "Response_200",
              "id": "1f56320b-9b0f-41bd-a65b-f61b9e3f4126"
            }
          ]
        }
      ]
    },
    {
      "name": "Symbols",
      "item": [
        {
          "id": "3c26ed20-f762-455e-9b5f-47245249a694",
          "name": "getSymbolListSymbolsByID",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.tradestation.com",
              "path": [
                "v2",
                "data/symbollists/:symbol_list_id/symbols"
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
                  "id": "symbol_list_id",
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
            "description": "Gets the Symbols for a specific Symbol List"
          },
          "response": [
            {
              "status": "Successful response",
              "code": 200,
              "name": "Response_200",
              "id": "33fed80d-d126-44d5-943c-ee7d77082ebb"
            }
          ]
        }
      ]
    },
    {
      "name": "User",
      "item": [
        {
          "id": "e563cf6a-9e3e-41fc-a517-7619521a4e6e",
          "name": "getAccountsByUserID",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.tradestation.com",
              "path": [
                "v2",
                "users/:user_id/accounts"
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
                  "id": "user_id",
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
            "description": "Returns all accounts for the given user"
          },
          "response": [
            {
              "status": "Successful response",
              "code": 200,
              "name": "Response_200",
              "id": "17af5b7f-6952-4243-9349-806b37c773df"
            }
          ]
        }
      ]
    },
    {
      "name": "Account",
      "item": [
        {
          "id": "5c3e94a5-a289-4291-977c-6d0edd4f3814",
          "name": "getBalancesByAccounts",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.tradestation.com",
              "path": [
                "v2",
                "accounts/:account_keys/balances"
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
                  "id": "account_keys",
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
            "description": "Returns the Balance for the given accounts"
          },
          "response": [
            {
              "status": "Successful response",
              "code": 200,
              "name": "Response_200",
              "id": "a9ca30c7-095b-4f73-9621-6d170d5a6aca"
            }
          ]
        },
        {
          "id": "5c04433e-d9a3-49ee-a018-d21adce8fae4",
          "name": "getPositionsByAccounts",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.tradestation.com",
              "path": [
                "v2",
                "accounts/:account_keys/positions"
              ],
              "query": [
                {
                  "key": "$filter",
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
                  "id": "account_keys",
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
            "description": "Returns the Positions for the given accounts"
          },
          "response": [
            {
              "status": "Successful response",
              "code": 200,
              "name": "Response_200",
              "id": "584d9f63-4c0d-4420-96f6-52c5d8691382"
            }
          ]
        },
        {
          "id": "42ab53ee-80b3-419b-976c-9ee714a93d2c",
          "name": "getOrdersByAccounts",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.tradestation.com",
              "path": [
                "v2",
                "accounts/:account_keys/orders"
              ],
              "query": [
                {
                  "key": "access_token",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "pageNum",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "pageSize",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "since",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "account_keys",
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
            "description": "Returns the Orders for the given accounts sorted descending, most recent order first.\n\n#### Stateless Connection\nSince the web-API provides a stateless connection, it only supports fetching the current state of Orders. If it is needed to display the intermediate state changes, it should be executed at client level."
          },
          "response": [
            {
              "status": "Successful response",
              "code": 200,
              "name": "Response_200",
              "id": "8c9208c8-52bb-448d-8e4f-7b0b6d3381cf"
            }
          ]
        }
      ]
    }
  ]
}