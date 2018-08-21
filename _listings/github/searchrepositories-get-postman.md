{
  "info": {
    "name": "Github Get Search Repositories",
    "_postman_id": "8f6c19ea-ffda-4afb-8079-1505923f7ca5",
    "description": "Search repositories.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "search",
      "item": [
        {
          "id": "59d2507f-d9bc-4aa0-9b30-3e61623d87c6",
          "name": "search-repositories",
          "request": {
            "url": "http://api.github.com/search/repositories?access_token=%7B%7D&order=%7B%7D&q=%7B%7D&sort=%7B%7D",
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
            "description": "Search repositories"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "7cfdbc82-acdb-4387-a761-16bdf72d001d"
            }
          ]
        }
      ]
    }
  ]
}