{
  "info": {
    "name": "Stack Exchange Get Tags",
    "_postman_id": "eb0d91c3-db33-4b47-8257-ba5586c5ecfb",
    "description": "Returns the tags found on a site.\n \nThe inname parameter lets a consumer filter down to tags that contain a certain substring. For example, inname=own would return both \"download\" and \"owner\" amongst others.\n \nThis method returns a list of tags.\n \nThe sorts accepted by this method operate on the follow fields of the tag object:\n - popular - count\n - activity - the creation_date of the last question asked with the tag\n - name - name\n  popular is the default sort.\n \n It is possible to create moderately complex queries using sort, min, max, fromdate, and todate.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "tags",
      "item": [
        {
          "id": "3b02a367-aa04-429a-94a8-082c11ecec93",
          "name": "returns-the-tags-found-on-a-site-the-inname-parameter-lets-a-consumer-filter-down-to-tags-that-conta",
          "request": {
            "url": "http://api.stackexchange.com/2.2/tags?callback=%7B%7D&filter=%7B%7D&fromdate=%7B%7D&inname=%7B%7D&max=%7B%7D&min=%7B%7D&order=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D&sort=%7B%7D&todate=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the tags found on a site"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8168a775-9e86-4404-8729-ca5b118585f4"
            }
          ]
        }
      ]
    }
  ]
}