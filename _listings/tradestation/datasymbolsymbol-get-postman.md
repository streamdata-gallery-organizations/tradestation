{
  "info": {
    "name": "TradeStation Get Symbol Info",
    "_postman_id": "37cd574b-1009-4287-a1fe-9d6ddeb53e1d",
    "description": "Finds the given symbol and returns a collection of fields describing the\nsymbol, its origin exchange, and other pertinant information.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Symbol",
      "item": [
        {
          "id": "1ec55c04-2048-419b-a53c-a7842591d483",
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
              "id": "2669910e-287b-4f10-8bac-e34feb8e35f1"
            }
          ]
        }
      ]
    }
  ]
}