{
  "info": {
    "name": "Github Get Search Issues",
    "_postman_id": "adeb581b-32d0-4730-8149-f743ead0f725",
    "description": "Find issues by state and keyword. (This method returns up to 100 results per page.)",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "search",
      "item": [
        {
          "id": "37b3e006-d4e7-45a0-bf9d-119c5f58b637",
          "name": "find-issues-by-state-and-keyword-this-method-returns-up-to-100-results-per-page",
          "request": {
            "url": "http://api.github.com/search/issues?access_token=%7B%7D&order=%7B%7D&q=%7B%7D&sort=%7B%7D",
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
            "description": "Find issues by state and keyword"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "7ddd8336-1dda-44f1-b7b8-8bbcc6c82fd1"
            }
          ]
        }
      ]
    }
  ]
}