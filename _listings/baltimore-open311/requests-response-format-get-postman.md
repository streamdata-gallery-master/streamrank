{
  "info": {
    "name": "Baltimore Open311 Requests",
    "_postman_id": "383bcb60-6152-4879-a8ee-951854ce6b45",
    "description": "Query the current status of multiple requests.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "311",
      "item": [
        {
          "id": "96f441f4-3c18-422a-846d-0b75aa004f4b",
          "name": "get-the-service-request-id-from-a-temporary-token-this-is-unnecessary-if-the-response-from-creating-",
          "request": {
            "url": {
              "protocol": "http",
              "host": "311.baltimorecity.gov",
              "path": [
                "open311",
                "v2",
                "tokens/:token_id.:response_format"
              ],
              "query": [
                {
                  "key": "No Name",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "token_id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "response_format",
                  "value": "response_format",
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
            "description": "Get the service_request_id from a temporary token. This is unnecessary if the response from creating a service request does not contain a token."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8e25df69-12ce-4783-a067-cc4db35baa0d"
            }
          ]
        },
        {
          "id": "e9bcf0b2-64a0-4392-b7ae-d0afd0a929ac",
          "name": "define-attributes-associated-with-a-service-code-these-attributes-can-be-unique-to-the-cityjurisdict",
          "request": {
            "url": {
              "protocol": "http",
              "host": "311.baltimorecity.gov",
              "path": [
                "open311",
                "v2",
                "services/:service_code.:response_format"
              ],
              "query": [
                {
                  "key": "No Name",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "service_code",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "response_format",
                  "value": "response_format",
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
            "description": "Define attributes associated with a service code. These attributes can be unique to the city/jurisdiction."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b585b974-63f6-482e-8442-c52e2fb496c2"
            }
          ]
        },
        {
          "id": "b385f7cc-e15d-4f51-a99d-c71c2603fd96",
          "name": "list-acceptable-service-request-types-and-their-associated-service-codes-these-request-types-can-be-",
          "request": {
            "url": {
              "protocol": "http",
              "host": "311.baltimorecity.gov",
              "path": [
                "open311",
                "v2",
                "services.:response_format"
              ],
              "query": [
                {
                  "key": "No Name",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "response_format",
                  "value": "response_format",
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
            "description": "List acceptable service request types and their associated service codes. These request types can be unique to the city/jurisdiction."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "02ffbde9-d756-466b-aace-b7f60061d62e"
            }
          ]
        },
        {
          "id": "adc554ea-7faa-4ff7-8062-349239e112ff",
          "name": "query-the-current-status-of-an-individual-request",
          "request": {
            "url": {
              "protocol": "http",
              "host": "311.baltimorecity.gov",
              "path": [
                "open311",
                "v2",
                "request/:service_request_id.:response_format"
              ],
              "query": [
                {
                  "key": "No Name",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "service_request_id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "response_format",
                  "value": "response_format",
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
            "description": "Query the current status of an individual request"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "9c49db63-5645-4140-886a-59673d3804ba"
            }
          ]
        },
        {
          "id": "2bd91967-aed2-445d-bb0d-464ff2f6bfab",
          "name": "query-the-current-status-of-multiple-requests",
          "request": {
            "url": {
              "protocol": "http",
              "host": "311.baltimorecity.gov",
              "path": [
                "open311",
                "v2",
                "requests.:response_format"
              ],
              "query": [
                {
                  "key": "end_date",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "No Name",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "service_code",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "service_request_id",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "start_date",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "status",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "response_format",
                  "value": "response_format",
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
            "description": "Query the current status of multiple requests."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "bbba28ab-18c5-4bf3-b014-0d3d1a8c4516"
            }
          ]
        },
        {
          "id": "47b92e08-1c78-4ecc-b8aa-741329a0b40f",
          "name": "submit-a-new-request-for-with-specific-details-of-a-single-service-must-provide-a-location-via-latlo",
          "request": {
            "url": {
              "protocol": "http",
              "host": "311.baltimorecity.gov",
              "path": [
                "open311",
                "v2",
                "requests.:response_format"
              ],
              "query": [
                {
                  "key": "address_id",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "address_string",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "attribute",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "lat",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "long",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "No Name",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "service_code",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "response_format",
                  "value": "response_format",
                  "type": "string"
                }
              ]
            },
            "method": "POST",
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
            "description": "Submit a new request for with specific details of a single service. Must provide a location via lat/long or address_string or address_id"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "4d9eb8e2-2d83-4fdc-9745-f26d98b179d5"
            }
          ]
        }
      ]
    }
  ]
}