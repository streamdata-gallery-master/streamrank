{
  "info": {
    "name": "Pinboard Get Popular Tags",
    "_postman_id": "870728ea-0a30-4b1b-98ad-9a7d1ff18088",
    "description": "Returns a list of popular tags and recommended tags for a given URL. Popular tags are tags used site-wide for the url; recommended tags are drawn from the user's own tags.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Posts",
      "item": [
        {
          "id": "59e10418-c5a1-433d-9f52-6f665d155df6",
          "name": "posts.update.get",
          "request": {
            "url": "http://api.pinboard.in/v1/posts/update",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the most recent time a bookmark was added, updated or deleted. Use this before calling posts/all to see if the data has changed since the last fetch."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "5d29230e-f19c-4150-a404-2f0672274219"
            }
          ]
        },
        {
          "id": "69bd3e66-4353-47df-93b6-74d5105c3465",
          "name": "posts.add.get",
          "request": {
            "url": "http://api.pinboard.in/v1/posts/add",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Add a new bookmark."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "683e7390-96e2-404a-9567-f465fb9520cd"
            }
          ]
        },
        {
          "id": "6204df3a-3433-4a7b-a2af-5dd2093747c6",
          "name": "posts.delete.get",
          "request": {
            "url": "http://api.pinboard.in/v1/posts/delete",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Delete a bookmark."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "72b97ef2-4163-4597-af80-6aaa558d2ec5"
            }
          ]
        },
        {
          "id": "99b834df-1983-485d-98aa-816324001182",
          "name": "posts.get.get",
          "request": {
            "url": "http://api.pinboard.in/v1/posts/get",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns one or more posts on a single day matching the arguments. If no date or url is given, date of most recent bookmark will be used."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "4b18750b-5545-444f-9738-40b393c947d3"
            }
          ]
        },
        {
          "id": "9ae38cae-f19d-46c7-93fa-e3c999ce8768",
          "name": "posts.dates.get",
          "request": {
            "url": "http://api.pinboard.in/v1/posts/dates",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns a list of dates with the number of posts at each date."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "014eed5c-de15-4f03-bfbd-c43b66fa4e16"
            }
          ]
        },
        {
          "id": "5b17dd1f-75a7-47c1-b8b0-4c5d68e19295",
          "name": "posts.recent.get",
          "request": {
            "url": "http://api.pinboard.in/v1/posts/recent?count=count&tag=tag",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns a list of the user's most recent posts, filtered by tag."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "bcc99472-64b5-4e05-9934-a5f0fd650662"
            }
          ]
        },
        {
          "id": "2a25f183-f0a6-40fd-ae8a-155f85b11d10",
          "name": "posts.all.get",
          "request": {
            "url": "http://api.pinboard.in/v1/posts/all?fromdt=fromdt&meta=meta&results=results&start=start&tag=tag&todt=todt",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns all bookmarks in the user's account."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "307ca801-54da-4b7a-b307-2942c0aa4f62"
            }
          ]
        },
        {
          "id": "47bf34b2-4b29-4282-982f-704f36a736ce",
          "name": "posts.suggest.get",
          "request": {
            "url": "http://api.pinboard.in/v1/posts/suggest?format=format&url=url",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns a list of popular tags and recommended tags for a given URL. Popular tags are tags used site-wide for the url; recommended tags are drawn from the user's own tags."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3cb11341-2413-4fe8-b653-64cddab16f33"
            }
          ]
        }
      ]
    }
  ]
}