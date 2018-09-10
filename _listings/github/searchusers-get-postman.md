{
  "info": {
    "name": "Github Get Search Users",
    "_postman_id": "6b097ed2-2398-4a29-bed7-61bbcafe5139",
    "description": "Search users.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "search",
      "item": [
        {
          "id": "bfc8cafa-c495-4a5b-807e-f3da47bb60aa",
          "name": "search-users",
          "request": {
            "url": "http://api.github.com/search/users?access_token=%7B%7D&order=%7B%7D&q=%7B%7D&sort=%7B%7D",
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
            "description": "Search users"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c8660a7a-5329-42b5-adad-cac7ea21cf54"
            }
          ]
        }
      ]
    }
  ]
}