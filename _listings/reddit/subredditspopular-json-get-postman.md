{
  "info": {
    "name": "Reddit Get Subreddits Where",
    "_postman_id": "d7dd6de5-da6e-45dd-b3ac-de31741381a1",
    "description": "Get all subreddits.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Best",
      "item": [
        {
          "id": "1f87c311-11b0-4e52-bccd-a24cb7d900a7",
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
              "id": "6d415108-8343-488b-91ba-92d5a2a62eaa"
            }
          ]
        }
      ]
    },
    {
      "name": "Names",
      "item": [
        {
          "id": "071cd6a4-30cd-475f-8af2-f1e34e95b139",
          "name": "get&nbsp;ByNames",
          "request": {
            "url": "http://www.reddit.com/by_id/names?names=names",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Get a listing of links by fullname."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "9f5cc623-a691-46e2-ab32-e289a5668d50"
            }
          ]
        }
      ]
    },
    {
      "name": "Subreddit",
      "item": [
        {
          "id": "f2e45690-7697-4bc4-b867-32acce1d4056",
          "name": "get&nbsp;RSubredditHot",
          "request": {
            "url": {
              "protocol": "http",
              "host": "www.reddit.com",
              "path": [
                ":/r/subreddit/hot.json"
              ],
              "query": [
                {
                  "key": "after",
                  "value": "after",
                  "disabled": false
                },
                {
                  "key": "before",
                  "value": "before",
                  "disabled": false
                },
                {
                  "key": "count",
                  "value": "count",
                  "disabled": false
                },
                {
                  "key": "g",
                  "value": "g",
                  "disabled": false
                },
                {
                  "key": "limit",
                  "value": "limit",
                  "disabled": false
                },
                {
                  "key": "show",
                  "value": "show",
                  "disabled": false
                },
                {
                  "key": "sr_detail",
                  "value": "sr_detail",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "/r/subreddit",
                  "value": "/r/subreddit",
                  "type": "string"
                }
              ]
            },
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
              "id": "36701773-8210-4d93-b5df-164b8b2abce6"
            }
          ]
        },
        {
          "id": "c04c823b-dd5c-4d80-8766-85a8f676c2ae",
          "name": "get&nbsp;RSubredditNew",
          "request": {
            "url": {
              "protocol": "http",
              "host": "www.reddit.com",
              "path": [
                ":/r/subreddit/new.json"
              ],
              "query": [
                {
                  "key": "after",
                  "value": "after",
                  "disabled": false
                },
                {
                  "key": "before",
                  "value": "before",
                  "disabled": false
                },
                {
                  "key": "count",
                  "value": "count",
                  "disabled": false
                },
                {
                  "key": "limit",
                  "value": "limit",
                  "disabled": false
                },
                {
                  "key": "show",
                  "value": "show",
                  "disabled": false
                },
                {
                  "key": "sr_detail",
                  "value": "sr_detail",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "/r/subreddit",
                  "value": "/r/subreddit",
                  "type": "string"
                }
              ]
            },
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
              "id": "7e213e47-3712-45e9-8fbd-6c79d5e588ea"
            }
          ]
        },
        {
          "id": "281edbbd-3297-4494-8f52-0ddb28aeaf23",
          "name": "get&nbsp;RSubredditRandom",
          "request": {
            "url": {
              "protocol": "http",
              "host": "www.reddit.com",
              "path": [
                ":/r/subreddit/random.json"
              ],
              "variable": [
                {
                  "id": "/r/subreddit",
                  "value": "/r/subreddit",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "The Serendipity button"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e6b888be-47ba-4ed0-8c88-eb65d49adbee"
            }
          ]
        },
        {
          "id": "d76393bc-834a-430a-bcb8-6d9731c6eaef",
          "name": "get&nbsp;RSubredditRising",
          "request": {
            "url": {
              "protocol": "http",
              "host": "www.reddit.com",
              "path": [
                ":/r/subreddit/rising.json"
              ],
              "query": [
                {
                  "key": "after",
                  "value": "after",
                  "disabled": false
                },
                {
                  "key": "before",
                  "value": "before",
                  "disabled": false
                },
                {
                  "key": "count",
                  "value": "count",
                  "disabled": false
                },
                {
                  "key": "limit",
                  "value": "limit",
                  "disabled": false
                },
                {
                  "key": "show",
                  "value": "show",
                  "disabled": false
                },
                {
                  "key": "sr_detail",
                  "value": "sr_detail",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "/r/subreddit",
                  "value": "/r/subreddit",
                  "type": "string"
                }
              ]
            },
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
              "id": "02e586ee-4f41-48b5-945b-1dfbff6f5586"
            }
          ]
        },
        {
          "id": "9af698b8-3aa8-4776-8a95-607ecd55885f",
          "name": "get&nbsp;RSubredditSort",
          "request": {
            "url": "http://www.reddit.com/{/r/subreddit}/sort?after=after&before=before&count=count&limit=limit&show=show&sr_detail=sr_detail&t=t",
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
              "id": "0ac63001-1cd0-4fe8-9960-0d234969ec83"
            }
          ]
        },
        {
          "id": "5d5f923c-6049-4372-bbc3-a10401272090",
          "name": "get&nbsp;RSubredditStylesheet",
          "request": {
            "url": "http://www.reddit.com/{/r/subreddit}/stylesheet",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Redirect to the subreddit&#39;s stylesheet if one exists."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "20f084a2-cc71-4033-a83d-eba1677312aa"
            }
          ]
        },
        {
          "id": "d5d2fc2a-8a48-45c4-9bb9-0775576d49b7",
          "name": "get&nbsp;RSubredditSubmitText",
          "request": {
            "url": "http://www.reddit.com/{/r/subreddit}/submit_text",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Get the submission text for the subreddit."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c3882ea1-d59e-4dd0-a718-dc61f56191f1"
            }
          ]
        },
        {
          "id": "367d2c09-fb57-4a39-9c4b-a861221d3f51",
          "name": "get&nbsp;RSubredditSebar",
          "request": {
            "url": "http://www.reddit.com/{/r/subreddit}/sidebar",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Get the sidebar for the current subreddit"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "03b73f05-4311-4e6d-99c7-edd28b136d5d"
            }
          ]
        },
        {
          "id": "b29f3231-8058-4812-9edd-d85d805c3a9f",
          "name": "get&nbsp;RSubredditSticky",
          "request": {
            "url": "http://www.reddit.com/{/r/subreddit}/sticky?num=num",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Redirect to one of the posts stickied in the current subreddit"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "10912d7b-6301-44b8-a767-3dce6b8284f4"
            }
          ]
        }
      ]
    },
    {
      "name": "Search",
      "item": [
        {
          "id": "6a3adf8b-0182-48f2-9618-aa85aca15ed3",
          "name": "get&nbsp;SearchRedditNames",
          "request": {
            "url": "http://www.reddit.com/api/search_reddit_names.json?exact=exact&include_over_18=include_over_18&include_unadvertisable=include_unadvertisable&query=query",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "List subreddit names that begin with a query string."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8967eee9-fc30-4951-b109-4f1cb7f4fb8b"
            }
          ]
        }
      ]
    },
    {
      "name": "Subreddits",
      "item": [
        {
          "id": "a2a3a9a3-a390-43e7-bc55-206ed20d5584",
          "name": "getNewSubreddit",
          "request": {
            "url": "http://www.reddit.com/subreddits/new.json?query=query",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns new subreddits."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a81b088c-3207-4f9e-a193-0cf71914d664"
            }
          ]
        },
        {
          "id": "d2e11c49-4955-4489-a406-accc33eb93b6",
          "name": "get&nbsp;SubredditsSearch",
          "request": {
            "url": "http://www.reddit.com/subreddits/search.json?after=after&before=before&count=count&limit=limit&q=q&show=show&sort=sort&sr_detail=sr_detail",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Search subreddits by title and description."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "efbf30b7-f66b-4f0e-bb97-8b76c5c75c1f"
            }
          ]
        },
        {
          "id": "8c1268f5-98de-47fb-83e6-1e08dd21cd10",
          "name": "get&nbsp;SubredditsWhere",
          "request": {
            "url": "http://www.reddit.com/subreddits/popular.json?after=after&before=before&count=count&limit=limit&show=show&sr_detail=sr_detail",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Get all subreddits."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f7e38ded-067c-4428-9889-6d56e2898dd7"
            }
          ]
        }
      ]
    }
  ]
}