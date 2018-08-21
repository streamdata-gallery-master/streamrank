{
  "info": {
    "name": "Reddit Get Best",
    "_postman_id": "feb51978-0647-4576-8c87-2d1fce9c1e08",
    "description": "This endpoint is a listing.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Best",
      "item": [
        {
          "id": "7f54bb31-4087-4afc-ad78-4857a3d637c9",
          "name": "get&nbsp;Best",
          "request": {
            "url": "http://www.reddit.com/best.json?after=after&before=before&count=count&limit=limit&show=show&sr_detail=sr_detail",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "This endpoint is a listing."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "52674936-b808-4f58-acd0-eec5b0c79274"
            }
          ]
        }
      ]
    }
  ]
}