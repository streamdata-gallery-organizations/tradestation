{
  "info": {
    "name": "TradeStation Get all Symbol Lists",
    "_postman_id": "e8d9e1de-c92a-4b85-9125-94194ac760ce",
    "description": "Gets a list of all Symbol Lists",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Symbol",
      "item": [
        {
          "id": "85f72624-12fa-4f42-a98c-292db3d7efbb",
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
              "id": "0758b2ad-7c9d-42cd-bc24-502c2982fdcb"
            }
          ]
        },
        {
          "id": "33587734-5231-4cf5-8d9d-a15947f76bae",
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
              "id": "06f2e2aa-a704-4273-836d-3176af2ff46d"
            }
          ]
        }
      ]
    },
    {
      "name": "Suggest",
      "item": [
        {
          "id": "3c27be14-c9b0-456e-af1a-350b71e15e34",
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
              "id": "5b68c377-a75b-4d8d-baa2-83cb2ab63ca8"
            }
          ]
        }
      ]
    },
    {
      "name": "SearchSymbols",
      "item": [
        {
          "id": "6fde5d42-ba1c-4410-be60-67b414260c3b",
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
              "id": "d98120dc-56b3-47cc-a071-a31508958595"
            }
          ]
        }
      ]
    },
    {
      "name": "Quote",
      "item": [
        {
          "id": "448891a9-f522-4c74-9299-42f1291d6dab",
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
              "id": "05cb2274-be7e-4d26-ad60-2826627c597d"
            }
          ]
        }
      ]
    },
    {
      "name": "Stream",
      "item": [
        {
          "id": "ddaf81b9-17e3-49f5-9aae-e9c4ce4d187e",
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
              "id": "58294b90-52bb-4d0b-99e8-2fa4bc4b407b"
            }
          ]
        },
        {
          "id": "7c8c2715-85ce-492b-9106-be04fa85c193",
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
              "id": "3410b9f5-2cc7-4548-ac93-fbaf383279bd"
            }
          ]
        },
        {
          "id": "10967a54-dd9a-46dd-bc98-a3a28d739ef6",
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
              "id": "13dab836-97cb-4a51-8a35-00812f7e3288"
            }
          ]
        },
        {
          "id": "61bf96b4-55ef-4b80-9b1f-24e892dde115",
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
              "id": "b1ecd0d3-19ed-4b62-a46c-e77b648b06a7"
            }
          ]
        },
        {
          "id": "aaa57846-03d1-4a5a-a893-44c4239b63e7",
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
              "id": "08f3fe6c-3788-4e7a-a222-eea8e46c0d6c"
            }
          ]
        },
        {
          "id": "7de0c540-e8cd-4cc7-952f-c50a16a0bfef",
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
              "id": "b52f1bcc-b267-47d7-bbe4-254e3a5ac1f1"
            }
          ]
        },
        {
          "id": "f009a21e-3012-4dc4-85c1-0a06436c7f4f",
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
              "id": "069ee62d-dc5f-4a14-a38a-ff4feaa25d1e"
            }
          ]
        }
      ]
    }
  ]
}