{
  "info": {
    "name": "Github Get Orgs Org Events",
    "_postman_id": "85da2c42-4127-4b5c-bc4c-dc1c53b096b0",
    "description": "List public events for an organization.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "orgs",
      "item": [
        {
          "id": "0a80f10b-b295-4d60-af7b-d7a2a6ae536c",
          "name": "list-public-events-for-an-organization",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.github.com",
              "path": [
                "orgs/:org/events"
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
                  "id": "org",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "{}",
                "description": "Is used to set specified media type",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "List public events for an organization"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "fe0f2200-a3c1-4060-bc59-11637c658c3f"
            }
          ]
        }
      ]
    }
  ]
}