{
  "info": {
    "name": "TradeStation Get Symbol List",
    "_postman_id": "bc23704d-9251-4ba0-93d7-90352a4ff997",
    "description": "Gets a specific Symbol List",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Symbol",
      "item": [
        {
          "id": "fd55df37-0a17-4869-8a2e-0cfef731da58",
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
              "id": "5ffc7533-25b8-41b5-bcb7-9e3292031ade"
            }
          ]
        },
        {
          "id": "bdb7a558-01c4-44f8-9584-21041e3b3a1c",
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
              "id": "d39ae86a-9126-4235-b889-41009898669e"
            }
          ]
        },
        {
          "id": "0df2f65e-47de-4b63-ae3c-b135918c0726",
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
              "id": "a9e1862c-f0f0-45c5-86d4-e58432c56729"
            }
          ]
        }
      ]
    },
    {
      "name": "Suggest",
      "item": [
        {
          "id": "876e6959-ba16-43ba-92db-4d8b8a17b4fb",
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
              "id": "923d46e6-878b-435c-b9a2-10c7b33479af"
            }
          ]
        }
      ]
    },
    {
      "name": "SearchSymbols",
      "item": [
        {
          "id": "8d3c1aa2-0240-49b3-937a-dd49e32e986c",
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
              "id": "4da56313-3764-444d-960b-7e43592fdd21"
            }
          ]
        }
      ]
    },
    {
      "name": "Quote",
      "item": [
        {
          "id": "1b10144e-4781-4d8c-a6a3-dd208f84c86f",
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
              "id": "f2f6d96e-4e44-4964-8ce5-bcf8fc97a4f5"
            }
          ]
        }
      ]
    },
    {
      "name": "Stream",
      "item": [
        {
          "id": "0e1072df-0443-453d-b5af-bed83fcc437c",
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
              "id": "40cb9085-84ae-46ed-80fd-181ba729a7f2"
            }
          ]
        },
        {
          "id": "2bddf270-c79a-439d-b732-276b16f3c264",
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
              "id": "35cf7ed1-ce09-4da5-bcff-f8af7731fc5f"
            }
          ]
        },
        {
          "id": "1ec9b630-b724-4f2e-9de2-229b72e6970f",
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
              "id": "4a5b0080-01dd-40ec-ae3b-021e1d8c382a"
            }
          ]
        },
        {
          "id": "4ad8e0c5-2b1f-4ef4-9432-fec56fff169a",
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
              "id": "baa2544d-312a-449a-a3b6-a207a74c9eb7"
            }
          ]
        },
        {
          "id": "0b846fa2-09c9-4b35-bd7b-c5376c15f74e",
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
              "id": "a4a6a065-8533-4cc8-be45-e2e72a88d85d"
            }
          ]
        },
        {
          "id": "c4fd676a-277b-48d2-8b56-eea6319cecfc",
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
              "id": "e5518e40-7ac4-4081-85f9-917af6c01eda"
            }
          ]
        },
        {
          "id": "b46ba29b-d836-4641-99a3-3fabe4bc73b9",
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
              "id": "f4424623-24a3-4625-9298-d04db2230285"
            }
          ]
        }
      ]
    }
  ]
}