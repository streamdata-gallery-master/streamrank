{
  "info": {
    "name": "Stack Exchange Search",
    "_postman_id": "4150d76b-e3d6-484e-8329-1c6a837c3b8e",
    "description": "Searches a site for any questions which fit the given criteria.\n \nThis method is intentionally quite limited. For more general searching, you should use a proper internet search engine restricted to the domain of the site in question.\n \nAt least one of tagged or intitle must be set on this method. nottagged is only used if tagged is also set, for performance reasons.\n \ntagged and nottagged are semi-colon delimited list of tags. At least 1 tag in tagged will be on each returned question if it is passed, making it the OR equivalent of the AND version of tagged on /questions.\n \nThe sorts accepted by this method operate on the follow fields of the question object:\n - activity - last_activity_date\n - creation - creation_date\n - votes - score\n - relevance - matches the relevance tab on the site itself Does not accept min or max\n  activity is the default sort.\n \n It is possible to create moderately complex queries using sort, min, max, fromdate, and todate.\n \nThis method returns a list of questions.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "search",
      "item": [
        {
          "id": "b75bb29b-bd54-40cd-bb8c-49d1600c3138",
          "name": "searches-a-site-for-any-questions-which-fit-the-given-criteria-this-method-is-intentionally-quite-li",
          "request": {
            "url": "http://api.stackexchange.com/2.2/search?callback=%7B%7D&filter=%7B%7D&fromdate=%7B%7D&intitle=%7B%7D&max=%7B%7D&min=%7B%7D&nottagged=%7B%7D&order=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D&sort=%7B%7D&tagged=%7B%7D&todate=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Searches a site for any questions which fit the given criteria"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "2f57aa13-f3d9-43c0-9b48-69c5c71685dd"
            }
          ]
        }
      ]
    }
  ]
}