{
  "info": {
    "name": "Twitter List Statuses",
    "_postman_id": "edbcdb85-fcb1-4a95-97a7-9be85c2e936e",
    "description": "Returns a timeline of tweets authored by memebers of the specified list",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "social",
      "item": [
        {
          "id": "bda4e31d-a3a3-4002-9a2f-dc7806b017e6",
          "name": "returns-a-timeline-of-tweets-authored-by-memebers-of-the-specified-list",
          "request": {
            "url": "http://api.twitter.com/1.1/lists/statuses.json?count=%7B%7D&include_entities=%7B%7D&include_rts=%7B%7D&list_id=%7B%7D&max_id=%7B%7D&owner_id=%7B%7D&owner_screen_name=%7B%7D&since_id=%7B%7D&slug=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns a timeline of tweets authored by memebers of the specified list"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "4a52b2d7-1919-4e32-8b5b-594a8573f310"
            }
          ]
        }
      ]
    }
  ]
}