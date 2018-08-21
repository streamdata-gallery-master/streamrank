{
  "info": {
    "name": "Github Get Events",
    "_postman_id": "d61174ec-c583-499c-8da9-77037da1c0bc",
    "description": "List public events.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "events",
      "item": [
        {
          "id": "6411383f-1652-47f7-b7ae-2d8cc9baf5ab",
          "name": "list-public-events",
          "request": {
            "url": "http://api.github.com/events?access_token=%7B%7D",
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
            "description": "List public events"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b1a666d4-7f89-4b57-a101-0ba34f1588ed"
            }
          ]
        }
      ]
    }
  ]
}