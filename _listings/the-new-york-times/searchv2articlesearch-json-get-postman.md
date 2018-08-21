{
  "info": {
    "name": "New York Times Article Search",
    "_postman_id": "2986826a-094b-4490-a230-febc5d77a375",
    "description": "Article SearchWith the Article Search API, you can search New York Times articles from Sept. 18, 1851 to today, retrieving headlines, abstracts, lead paragraphs, links to associated multimedia and other article.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "news",
      "item": [
        {
          "id": "7db31d21-5b44-42e5-a662-6a7291b9d1be",
          "name": "article-search-requests-use-the-following-uri-structure",
          "request": {
            "url": "http://api.nytimes.com/svc/search/v2/articlesearch.json?api-key=api-key&begin_date=%7B%7D&end_date=%7B%7D&facet_field=%7B%7D&facet_filter=%7B%7D&fl=%7B%7D&fq=%7B%7D&hl=%7B%7D&page=%7B%7D&q=%7B%7D&sort=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Article SearchWith the Article Search API, you can search New York Times articles from Sept"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "5daf87f7-7f68-4eaf-804b-8683d5c90d0b"
            }
          ]
        }
      ]
    }
  ]
}