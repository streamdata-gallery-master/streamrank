{
  "info": {
    "name": "Github Get Search Code",
    "_postman_id": "bbc441b1-8369-4255-96b9-27b9de8984f3",
    "description": "Search code.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "search",
      "item": [
        {
          "id": "bfdf7510-22e7-4447-a461-6cbc522e7e77",
          "name": "search-code",
          "request": {
            "url": "http://api.github.com/search/code?access_token=%7B%7D&order=%7B%7D&q=%7B%7D&sort=%7B%7D",
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
            "description": "Search code"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a0fbcd7f-b5e1-4e5d-a6d3-3230fec70f5b"
            }
          ]
        }
      ]
    }
  ]
}