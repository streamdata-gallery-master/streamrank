{
  "info": {
    "name": "Github Get Orgs Org Issues",
    "_postman_id": "2c34bf8c-6928-4c7b-9f63-bead1179e7ef",
    "description": "List issues.\nList all issues for a given organization for the authenticated user.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "orgs",
      "item": [
        {
          "id": "80ff0cae-6e9d-4751-813d-c71783d25abb",
          "name": "list-issueslist-all-issues-for-a-given-organization-for-the-authenticated-user",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.github.com",
              "path": [
                "orgs/:org/issues"
              ],
              "query": [
                {
                  "key": "access_token",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "direction",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "filter",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "labels",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "since",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "sort",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "state",
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
            "description": "List issues"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ee85bb6e-61e9-4abc-b933-741308abd684"
            }
          ]
        }
      ]
    }
  ]
}