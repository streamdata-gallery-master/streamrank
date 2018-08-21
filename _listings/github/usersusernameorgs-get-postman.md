{
  "info": {
    "name": "Github Get Users Username Orgs",
    "_postman_id": "77d568b3-f718-45d9-bf6b-4a32fa397eda",
    "description": "List all public organizations for a user.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "users",
      "item": [
        {
          "id": "1f7932c5-3343-43b2-96a3-1b498e552de8",
          "name": "list-all-public-organizations-for-a-user",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.github.com",
              "path": [
                "users/:username/orgs"
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
                  "id": "username",
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
            "description": "List all public organizations for a user"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "5c9e49f1-75e1-4081-97b7-84916c343bc6"
            }
          ]
        }
      ]
    }
  ]
}