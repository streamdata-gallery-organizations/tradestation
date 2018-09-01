{
  "info": {
    "name": "TradeStation Stream BarChart - Date Range",
    "_postman_id": "f1baea13-750c-44a7-9458-d66f65d15aaf",
    "description": "Streams barchart data starting from startDate to end date, each bar filling interval of unit.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Symbol",
      "item": [
        {
          "id": "76d2b53e-ab9f-4b84-8126-962828ad3b8b",
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
              "id": "32193fea-6648-4598-af9e-0104d692a276"
            }
          ]
        }
      ]
    },
    {
      "name": "Suggest",
      "item": [
        {
          "id": "46c6e477-0ea6-4124-b519-3be8106b06bc",
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
              "id": "ebd31710-7cd4-457c-9798-a46280e406a4"
            }
          ]
        }
      ]
    },
    {
      "name": "SearchSymbols",
      "item": [
        {
          "id": "8e5a62ec-ff83-4063-bba9-d30fd3cde138",
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
              "id": "58abdad1-9662-47ad-81a9-d12e20ac9bee"
            }
          ]
        }
      ]
    },
    {
      "name": "Quote",
      "item": [
        {
          "id": "dff74770-c1a7-44db-8b7f-f086f0ac4719",
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
              "id": "2ae52ed2-7ee5-4f4a-8cca-cb2943c141da"
            }
          ]
        }
      ]
    },
    {
      "name": "Stream",
      "item": [
        {
          "id": "10d5627a-bccc-4f48-a7ee-8997f1a9bcda",
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
              "id": "92e75f38-5ae4-4231-82bf-e04a0fc937b1"
            }
          ]
        },
        {
          "id": "7298d7a2-ca03-440c-86fc-08e6d734665e",
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
              "id": "5163df49-d0c2-4edd-8d71-750ed2f1bd80"
            }
          ]
        },
        {
          "id": "b1c46c01-fafd-440e-95c0-59edad85bbbd",
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
              "id": "e93eca29-b212-4d18-95c3-5216aac9f916"
            }
          ]
        },
        {
          "id": "b04b2fa7-4818-44c5-9b6c-e8a0830eb53d",
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
              "id": "0b588684-1b4f-4662-b3e8-b8359518c33a"
            }
          ]
        }
      ]
    }
  ]
}