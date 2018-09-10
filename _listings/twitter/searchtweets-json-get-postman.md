{
  "info": {
    "name": "Twitter Search Tweets",
    "_postman_id": "e0233fac-d631-4857-9034-ebfad325acd9",
    "description": "returns collection of relevant Tweets matching query",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "social",
      "item": [
        {
          "id": "fb5a3d96-d1eb-4df0-948f-f4c5024ae81c",
          "name": "returns-collection-of-relevant-tweets-matching-query",
          "request": {
            "url": "http://api.twitter.com/1.1/search/tweets.json?callback=%7B%7D&count=%7B%7D&geocode=%7B%7D&include_entities=%7B%7D&lang=%7B%7D&locale=%7B%7D&max_id=%7B%7D&q=%7B%7D&result_type=%7B%7D&since_id=%7B%7D&until=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "returns collection of relevant Tweets matching query"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "59b0f083-f111-492f-b1a4-754d489fcad5"
            }
          ]
        }
      ]
    }
  ]
}