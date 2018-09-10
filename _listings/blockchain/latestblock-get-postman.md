{
  "info": {
    "name": "Blockchain Info Latest Block",
    "_postman_id": "5af8b698-3c2d-4e0b-8c5e-95fa9b899c88",
    "description": "Gets the latest block.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Blockchain",
      "item": [
        {
          "id": "ac8a3806-d175-4e73-9830-ec32e3751993",
          "name": "getLatestBlock",
          "request": {
            "url": "http://blockchain.info/latestblock?format=format",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets the latest block."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d7e13a75-b6f7-4925-b176-5b7e49784b3a"
            }
          ]
        }
      ]
    }
  ]
}