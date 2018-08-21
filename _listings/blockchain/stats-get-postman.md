{
  "info": {
    "name": "Blockchain Info Stats",
    "_postman_id": "a17545ea-e7d8-4f50-9356-879b50e566c9",
    "description": "This method can be used to get the data behind Blockchain.info's stats.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Blockchain",
      "item": [
        {
          "id": "de111121-5616-4409-b697-6c1c61d2fe20",
          "name": "getStats",
          "request": {
            "url": "http://blockchain.info/stats?format=format",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "This method can be used to get the data behind Blockchain.info's stats."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "420d9429-5c17-4f67-9ea4-3c270d7a8214"
            }
          ]
        }
      ]
    }
  ]
}