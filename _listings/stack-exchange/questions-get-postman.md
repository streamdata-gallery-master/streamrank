{
  "info": {
    "name": "Stack Exchange Get Questions",
    "_postman_id": "692634c3-be1f-409d-b649-af67029e1be3",
    "description": "Gets all the questions on the site.\n \nThis method allows you make fairly flexible queries across the entire corpus of questions on a site. For example, getting all questions asked in the the week of Jan 1st 2011 with scores of 10 or more is a single query with parameters sort=votes&min=10&fromdate=1293840000&todate=1294444800.\n \nTo constrain questions returned to those with a set of tags, use the tagged parameter with a semi-colon delimited list of tags. This is an and contraint, passing tagged=c;java will return only those questions with both tags. As such, passing more than 5 tags will always return zero results.\n \nThe sorts accepted by this method operate on the follow fields of the question object:\n - activity - last_activity_date\n - creation - creation_date\n - votes - score\n - hot - by the formula ordering the hot tab Does not accept min or max\n - week - by the formula ordering the week tab Does not accept min or max\n - month - by the formula ordering the month tab Does not accept min or max\n  activity is the default sort.\n \n It is possible to create moderately complex queries using sort, min, max, fromdate, and todate.\n \nThis method returns a list of questions.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Authentication",
      "item": [
        {
          "id": "387c6607-4724-4810-a436-e7bef741aa70",
          "name": "reads-the-properties-for-a-set-of-access-tokens-accesstokens-can-contain-up-to-20-access-tokens-thes",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.stackexchange.com",
              "path": [
                "2.2",
                "access-tokens/:accessTokens"
              ],
              "query": [
                {
                  "key": "callback",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "filter",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "page",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "pagesize",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "accessTokens",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Reads the properties for a set of access tokens.\n \n{accessTokens} can contain up to 20 access tokens. These are obtained by authenticating a user using OAuth 2.0.\n \nThis method returns a list of access_tokens."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c6fee120-7e5e-4209-b156-3b1acc0ae783"
            }
          ]
        },
        {
          "id": "c5592a84-256f-4cd9-85c3-e21a4ccb4a22",
          "name": "immediately-expires-the-access-tokens-passed-this-method-is-meant-to-allow-an-application-to-discard",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.stackexchange.com",
              "path": [
                "2.2",
                "access-tokens/:accessTokens/invalidate"
              ],
              "query": [
                {
                  "key": "callback",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "filter",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "page",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "pagesize",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "accessTokens",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Immediately expires the access tokens passed. This method is meant to allow an application to discard any active access tokens it no longer needs.\n \n{accessTokens} can contain up to 20 access tokens. These are obtained by authenticating a user using OAuth 2.0.\n \nThis method returns a list of access_tokens."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "2bb872a3-20be-4ef8-a4e6-3a35dd3663d5"
            }
          ]
        },
        {
          "id": "825baadf-ab3e-4181-a8f4-2d3be01c8f86",
          "name": "passing-valid-access-tokens-to-this-method-causes-the-application-that-created-them-to-be-deauthoriz",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.stackexchange.com",
              "path": [
                "2.2",
                "apps/:accessTokens/de-authenticate"
              ],
              "query": [
                {
                  "key": "callback",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "filter",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "page",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "pagesize",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "accessTokens",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Passing valid access_tokens to this method causes the application that created them to be de-authorized by the user associated with each access_token. This will remove the application from their apps tab, and cause all other existing access_tokens to be destroyed.\n \nThis method is meant for uninstalling applications, recovering from access_token leaks, or simply as a stronger form of /access-tokens/{accessTokens}/invalidate.\n \nNothing prevents a user from re-authenticate to an application that has de-authenticated itself, the user will be prompted to approve the application again however.\n \n{accessTokens} can contain up to 20 access tokens. These are obtained by authenticating a user using OAuth 2.0.\n \nThis method returns a list of access_tokens."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f0fbdbd2-acd4-49b8-9a5f-df391dfcc145"
            }
          ]
        }
      ]
    },
    {
      "name": "Answers",
      "item": [
        {
          "id": "eb31527d-b400-44f8-ba43-ccc916c87752",
          "name": "returns-all-the-undeleted-answers-in-the-system-the-sorts-accepted-by-this-method-operate-on-the-fol",
          "request": {
            "url": "http://api.stackexchange.com/2.2/answers?callback=%7B%7D&filter=%7B%7D&fromdate=%7B%7D&max=%7B%7D&min=%7B%7D&order=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D&sort=%7B%7D&todate=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns all the undeleted answers in the system.\n \nThe sorts accepted by this method operate on the follow fields of the answer object:\n - activity - last_activity_date\n - creation - creation_date\n - votes - score\n  activity is the default sort.\n \n It is possible to create moderately complex queries using sort, min, max, fromdate, and todate.\n \nThis method returns a list of answers."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "fc2203d8-8bd8-43cf-892a-fd29c210ab18"
            }
          ]
        },
        {
          "id": "144d4cf7-f65a-46d7-995f-a3f09a562026",
          "name": "gets-the-set-of-answers-identified-by-ids-this-is-meant-for-batch-fetcing-of-questions-a-useful-tric",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.stackexchange.com",
              "path": [
                "2.2",
                "answers/:ids"
              ],
              "query": [
                {
                  "key": "callback",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "filter",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "fromdate",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "max",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "min",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "order",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "page",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "pagesize",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "site",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "sort",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "todate",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "ids",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets the set of answers identified by ids.\n \nThis is meant for batch fetcing of questions. A useful trick to poll for updates is to sort by activity, with a minimum date of the last time you polled.\n \n{ids} can contain up to 100 semicolon delimited ids, to find ids programatically look for answer_id on answer objects.\n \nThe sorts accepted by this method operate on the follow fields of the answer object:\n - activity - last_activity_date\n - creation - creation_date\n - votes - score\n  activity is the default sort.\n \n It is possible to create moderately complex queries using sort, min, max, fromdate, and todate.\n \nThis method returns a list of answers."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a6070806-e5af-48d4-bcd2-a758d7ad3179"
            }
          ]
        },
        {
          "id": "cee27f02-1cb9-4583-90ac-3690a1ca8c16",
          "name": "gets-the-comments-on-a-set-of-answers-if-you-know-that-you-have-an-answer-id-and-need-the-comments-u",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.stackexchange.com",
              "path": [
                "2.2",
                "answers/:ids/comments"
              ],
              "query": [
                {
                  "key": "callback",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "filter",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "fromdate",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "max",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "min",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "order",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "page",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "pagesize",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "site",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "sort",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "todate",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "ids",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets the comments on a set of answers.\n \nIf you know that you have an answer id and need the comments, use this method. If you know you have a question id, use /questions/{id}/comments. If you are unsure, use /posts/{id}/comments.\n \n{ids} can contain up to 100 semicolon delimited ids, to find ids programatically look for answer_id on answer objects.\n \nThe sorts accepted by this method operate on the follow fields of the comment object:\n - creation - creation_date\n - votes - score\n  creation is the default sort.\n \n It is possible to create moderately complex queries using sort, min, max, fromdate, and todate.\n \nThis method returns a list of comments."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "27e796cf-1a31-4f20-bea0-6963ce6e78e6"
            }
          ]
        },
        {
          "id": "ddf91b4f-4921-4ab7-9f62-fad1cdac24c4",
          "name": "returns-the-answers-owned-by-the-user-associated-with-the-given-access-token-this-method-returns-a-l",
          "request": {
            "url": "http://api.stackexchange.com/2.2/me/answers?callback=%7B%7D&filter=%7B%7D&fromdate=%7B%7D&max=%7B%7D&min=%7B%7D&order=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D&sort=%7B%7D&todate=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the answers owned by the user associated with the given access_token.\n \nThis method returns a list of answers."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "01d29015-4d09-4cbb-93cd-5ed8658d34ac"
            }
          ]
        }
      ]
    },
    {
      "name": "Badges",
      "item": [
        {
          "id": "2c4c1bd5-f2fa-4cb4-b665-53f03662e7bf",
          "name": "returns-all-the-badges-in-the-system-badge-sorts-are-a-tad-complicated-for-the-purposes-of-sorting-a",
          "request": {
            "url": "http://api.stackexchange.com/2.2/badges?callback=%7B%7D&filter=%7B%7D&fromdate=%7B%7D&inname=%7B%7D&max=%7B%7D&min=%7B%7D&order=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D&sort=%7B%7D&todate=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns all the badges in the system.\n \nBadge sorts are a tad complicated. For the purposes of sorting (and min/max) tag_based is considered to be greater than named.\n \nThis means that you can get a list of all tag based badges by passing min=tag_based, and conversely all the named badges by passing max=named, with sort=type.\n \nFor ranks, bronze is greater than silver which is greater than gold. Along with sort=rank, set max=gold for just gold badges, max=silver&min=silver for just silver, and min=bronze for just bronze.\n \nrank is the default sort.\n \nThis method returns a list of badges."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "228d0f5e-5d84-4c82-b84f-abbf5c26789d"
            }
          ]
        },
        {
          "id": "300979f4-5658-4fd4-9ba5-fae6936d859d",
          "name": "gets-all-explicitly-named-badges-in-the-system-a-named-badged-stands-in-opposition-to-a-tagbased-bad",
          "request": {
            "url": "http://api.stackexchange.com/2.2/badges/name?callback=%7B%7D&filter=%7B%7D&fromdate=%7B%7D&inname=%7B%7D&max=%7B%7D&min=%7B%7D&order=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D&sort=%7B%7D&todate=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets all explicitly named badges in the system.\n \nA named badged stands in opposition to a tag-based badge. These are referred to as general badges on the sites themselves.\n \nFor the rank sort, bronze is greater than silver which is greater than gold. Along with sort=rank, set max=gold for just gold badges, max=silver&min=silver for just silver, and min=bronze for just bronze.\n \nrank is the default sort.\n \nThis method returns a list of badges."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ee65ee9f-fc93-40dc-9cbc-03c751aef6f8"
            }
          ]
        },
        {
          "id": "fbb9285a-13c5-48f2-95e6-450ec4f2ad08",
          "name": "returns-recently-awarded-badges-in-the-system-as-these-badges-have-been-awarded-they-will-have-the-b",
          "request": {
            "url": "http://api.stackexchange.com/2.2/badges/recipients?callback=%7B%7D&filter=%7B%7D&fromdate=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D&todate=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns recently awarded badges in the system.\n \nAs these badges have been awarded, they will have the badge.user property set.\n \nThis method returns a list of badges."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "18bbc575-06c4-45f8-a537-f29e8259d46a"
            }
          ]
        },
        {
          "id": "72d46bb8-2306-47b6-8996-f03ea67b679d",
          "name": "returns-the-badges-that-are-awarded-for-participation-in-specific-tags-for-the-rank-sort-bronze-is-g",
          "request": {
            "url": "http://api.stackexchange.com/2.2/badges/tags?callback=%7B%7D&filter=%7B%7D&fromdate=%7B%7D&inname=%7B%7D&max=%7B%7D&min=%7B%7D&order=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D&sort=%7B%7D&todate=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the badges that are awarded for participation in specific tags.\n \nFor the rank sort, bronze is greater than silver which is greater than gold. Along with sort=rank, set max=gold for just gold badges, max=silver&min=silver for just silver, and min=bronze for just bronze.\n \nrank is the default sort.\n \nThis method returns a list of badges."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "1146247a-38c0-4fb1-ba44-b5d7a1663d6d"
            }
          ]
        },
        {
          "id": "9d4de824-5fe2-4e2f-bd98-e066fcc28060",
          "name": "gets-the-badges-identified-in-id-note-that-badge-ids-are-not-constant-across-sites-and-thus-should-b",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.stackexchange.com",
              "path": [
                "2.2",
                "badges/:ids"
              ],
              "query": [
                {
                  "key": "callback",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "filter",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "fromdate",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "max",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "min",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "order",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "page",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "pagesize",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "site",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "sort",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "todate",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "ids",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets the badges identified in id.\n \nNote that badge ids are not constant across sites, and thus should be looked up via the /badges method. A badge id on a single site is, however, guaranteed to be stable.\n \nBadge sorts are a tad complicated. For the purposes of sorting (and min/max) tag_based is considered to be greater than named.\n \nThis means that you can get a list of all tag based badges by passing min=tag_based, and conversely all the named badges by passing max=named, with sort=type.\n \nFor ranks, bronze is greater than silver which is greater than gold. Along with sort=rank, set max=gold for just gold badges, max=silver&min=silver for just silver, and min=bronze for just bronze.\n \nrank is the default sort.\n \n{ids} can contain up to 100 semicolon delimited ids, to find ids programatically look for badge_id on badge objects.\n \nThis method returns a list of badges."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "73a791df-f1c2-4bb3-a54f-d0582edf71e5"
            }
          ]
        },
        {
          "id": "dbb673fe-2546-4b50-b0dd-8d8a895ccdee",
          "name": "returns-recently-awarded-badges-in-the-system-constrained-to-a-certain-set-of-badges-as-these-badges",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.stackexchange.com",
              "path": [
                "2.2",
                "badges/:ids/recipients"
              ],
              "query": [
                {
                  "key": "callback",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "filter",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "fromdate",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "page",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "pagesize",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "site",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "todate",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "ids",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns recently awarded badges in the system, constrained to a certain set of badges.\n \nAs these badges have been awarded, they will have the badge.user property set.\n \n{ids} can contain up to 100 semicolon delimited ids, to find ids programatically look for badge_id on badge objects.\n \nThis method returns a list of badges."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "82902964-e5f7-4ccd-b00b-5a42bfd7538c"
            }
          ]
        },
        {
          "id": "901cab98-eb92-45d4-8df5-5c2469587c14",
          "name": "returns-the-badges-earned-by-the-user-associated-with-the-given-access-token-this-method-returns-a-l",
          "request": {
            "url": "http://api.stackexchange.com/2.2/me/badges?callback=%7B%7D&filter=%7B%7D&fromdate=%7B%7D&max=%7B%7D&min=%7B%7D&order=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D&sort=%7B%7D&todate=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the badges earned by the user associated with the given access_token.\n \nThis method returns a list of badges."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "9682b91c-4aff-4a30-a8c4-f488f4f029f3"
            }
          ]
        }
      ]
    },
    {
      "name": "Comments",
      "item": [
        {
          "id": "12ba47e1-da40-42af-9360-47cde0201a4f",
          "name": "gets-all-the-comments-on-the-site-if-youre-filtering-for-interesting-comments-by-score-creation-date",
          "request": {
            "url": "http://api.stackexchange.com/2.2/comments?callback=%7B%7D&filter=%7B%7D&fromdate=%7B%7D&max=%7B%7D&min=%7B%7D&order=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D&sort=%7B%7D&todate=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets all the comments on the site.\n \nIf you're filtering for interesting comments (by score, creation date, etc.) make use of the sort paramter with appropriate min and max values.\n \nIf you're looking to query conversations between users, instead use the /users/{ids}/mentioned and /users/{ids}/comments/{toid} methods.\n \nThe sorts accepted by this method operate on the follow fields of the comment object:\n - creation - creation_date\n - votes - score\n  creation is the default sort.\n \n It is possible to create moderately complex queries using sort, min, max, fromdate, and todate.\n \nThis method returns a list of comments."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ee803c15-f6c5-4d0a-bb38-9675cd65000a"
            }
          ]
        },
        {
          "id": "862a3711-5e30-4746-847c-b0a1c5ee21d6",
          "name": "gets-the-comments-identified-in-id-this-method-is-most-useful-if-you-have-a-cache-of-comment-ids-obt",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.stackexchange.com",
              "path": [
                "2.2",
                "comments/:ids"
              ],
              "query": [
                {
                  "key": "callback",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "filter",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "fromdate",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "max",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "min",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "order",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "page",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "pagesize",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "site",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "sort",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "todate",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "ids",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets the comments identified in id.\n \nThis method is most useful if you have a cache of comment ids obtained through other means (such as /questions/{id}/comments) but suspect the data may be stale.\n \n{ids} can contain up to 100 semicolon delimited ids, to find ids programatically look for comment_id on comment objects.\n \nThe sorts accepted by this method operate on the follow fields of the comment object:\n - creation - creation_date\n - votes - score\n  creation is the default sort.\n \n It is possible to create moderately complex queries using sort, min, max, fromdate, and todate.\n \nThis method returns a list of comments."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8d5c3c2f-da7e-4f91-82a6-7b5552316d50"
            }
          ]
        },
        {
          "id": "8a43bc64-893c-4cde-aa31-380a8f4d8a82",
          "name": "deletes-a-comment-use-an-access-token-with-write-access-to-delete-a-comment-in-practice-this-method-",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.stackexchange.com",
              "path": [
                "2.2",
                "comments/:id/delete"
              ],
              "query": [
                {
                  "key": "callback",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "filter",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "preview",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "site",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "Deletes a comment.\n \nUse an access_token with write_access to delete a comment.\n \nIn practice, this method will never return an object."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "dd620ac5-cecd-40af-9864-310e8333277d"
            }
          ]
        },
        {
          "id": "f0cc22ed-7ebe-4c24-849c-2b46a38f9d5c",
          "name": "edit-an-existing-comment-use-an-access-token-with-write-access-to-edit-an-existing-comment-this-meth",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.stackexchange.com",
              "path": [
                "2.2",
                "comments/:id/edit"
              ],
              "query": [
                {
                  "key": "body",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "callback",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "filter",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "preview",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "site",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "Edit an existing comment.\n \nUse an access_token with write_access to edit an existing comment.\n \nThis method return the created comment."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8c78aa31-2714-41de-9c2d-bc37e55bb34d"
            }
          ]
        },
        {
          "id": "058b5311-4936-4642-9638-62bdb6479922",
          "name": "returns-the-comments-owned-by-the-user-associated-with-the-given-access-token-this-method-returns-a-",
          "request": {
            "url": "http://api.stackexchange.com/2.2/me/comments?callback=%7B%7D&filter=%7B%7D&fromdate=%7B%7D&max=%7B%7D&min=%7B%7D&order=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D&sort=%7B%7D&todate=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the comments owned by the user associated with the given access_token.\n \nThis method returns a list of comments."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "594e8a39-9d3f-45f8-9b38-49347870ce76"
            }
          ]
        },
        {
          "id": "45153201-42d2-4ef4-bb92-ad84855ad5bc",
          "name": "returns-the-comments-owned-by-the-user-associated-with-the-given-access-token-that-are-in-reply-to-t",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.stackexchange.com",
              "path": [
                "2.2",
                "me/comments/:toId"
              ],
              "query": [
                {
                  "key": "callback",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "filter",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "fromdate",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "max",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "min",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "order",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "page",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "pagesize",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "site",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "sort",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "todate",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "toId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the comments owned by the user associated with the given access_token that are in reply to the user identified by {toId}.\n \nThis method returns a list of comments."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8c1e072c-54ca-4bf0-94c3-6904024bacfe"
            }
          ]
        }
      ]
    },
    {
      "name": "Errors",
      "item": [
        {
          "id": "20f7b928-12e4-4c05-98bf-e5a8f816b64b",
          "name": "returns-the-various-error-codes-that-can-be-produced-by-the-api-this-method-is-provided-for-discover",
          "request": {
            "url": "http://api.stackexchange.com/2.2/errors?callback=%7B%7D&filter=%7B%7D&page=%7B%7D&pagesize=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the various error codes that can be produced by the API.\n \nThis method is provided for discovery, documentation, and testing purposes, it is not expected many applications will consume it during normal operation.\n \nFor testing purposes, look into the /errors/{id} method which simulates errors given a code.\n \nThis method returns a list of errors."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ea0c8ad4-460e-45bd-a9b5-f97134600619"
            }
          ]
        },
        {
          "id": "4843a4b9-4b40-4bce-8e59-e3233df3ba0c",
          "name": "this-method-allows-you-to-generate-an-error-this-method-is-only-intended-for-use-when-testing-an-app",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.stackexchange.com",
              "path": [
                "2.2",
                "errors/:id"
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "This method allows you to generate an error.\n \nThis method is only intended for use when testing an application or library. Unlike other methods in the API, its contract is not frozen, and new error codes may be added at any time.\n \nThis method results in an error, which will be expressed with a 400 HTTP status code and setting the error* properties on the wrapper object."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "44c40347-1312-4449-9e85-64f56cdddc55"
            }
          ]
        }
      ]
    },
    {
      "name": "Events",
      "item": [
        {
          "id": "9379b911-bbc2-4517-a015-c11bf7526d93",
          "name": "returns-a-stream-of-events-that-have-occurred-on-the-site-the-api-considers-the-following-events--po",
          "request": {
            "url": "http://api.stackexchange.com/2.2/events?callback=%7B%7D&filter=%7B%7D&page=%7B%7D&pagesize=%7B%7D&since=%7B%7D&site=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns a stream of events that have occurred on the site.\n \nThe API considers the following \"events\":\n - posting a question\n - posting an answer\n - posting a comment\n - editing a post\n - creating a user\n  \n \nEvents are only accessible for 15 minutes after they occurred, and by default only events in the last 5 minutes are returned. You can specify the age of the oldest event returned by setting the since parameter.\n \nIt is advised that developers batch events by ids and make as few subsequent requests to other methods as possible.\n \nThis method returns a list of events."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "da5c05c5-0f89-42d9-bd4e-75715d8376b0"
            }
          ]
        }
      ]
    },
    {
      "name": "Files",
      "item": [
        {
          "id": "66adde9c-a00a-425e-8747-add79cc080f4",
          "name": "creates-a-new-filter-given-a-list-of-includes-excludes-a-base-filter-and-whether-or-not-this-filter-",
          "request": {
            "url": "http://api.stackexchange.com/2.2/filters/create?base=%7B%7D&exclude=%7B%7D&include=%7B%7D&unsafe=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Creates a new filter given a list of includes, excludes, a base filter, and whether or not this filter should be \"unsafe\".\n \nFilter \"safety\" is defined as follows. Any string returned as a result of an API call with a safe filter will be inline-able into HTML without script-injection concerns. That is to say, no additional sanitizing (encoding, HTML tag stripping, etc.) will be necessary on returned strings. Applications that wish to handle sanitizing themselves should create an unsafe filter. All filters are safe by default, under the assumption that double-encoding bugs are more desirable than script injections.\n \nIf no base filter is specified, the default filter is assumed. When building a filter from scratch, the none built-in filter is useful.\n \nWhen the size of the parameters being sent to this method grows to large, problems can occur. This method will accept POST requests to mitigate this.\n \nIt is not expected that many applications will call this method at runtime, filters should be pre-calculated and \"baked in\" in the common cases. Furthermore, there are a number of built-in filters which cover common use cases.\n \nThis method returns a single filter."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "14dc2141-6f76-4ca1-a66e-75900be458e9"
            }
          ]
        },
        {
          "id": "7a459290-1a06-4274-8d5d-cfa44552e471",
          "name": "returns-the-fields-included-by-the-given-filters-and-the-safeness-of-those-filters-it-is-not-expecte",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.stackexchange.com",
              "path": [
                "2.2",
                "filters/:filters"
              ],
              "variable": [
                {
                  "id": "filters",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the fields included by the given filters, and the \"safeness\" of those filters.\n \nIt is not expected that this method will be consumed by many applications at runtime, it is provided to aid in debugging.\n \n{filters} can contain up to 20 semicolon delimited filters. Filters are obtained via calls to /filters/create, or by using a built-in filter.\n \nThis method returns a list of filters."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3965ae2e-4c29-43cc-af88-aa8a4c6b45e1"
            }
          ]
        }
      ]
    },
    {
      "name": "Email",
      "item": [
        {
          "id": "75e085d6-dc4d-4aa7-a610-7cf50ccee305",
          "name": "returns-a-users-inbox-this-method-requires-an-access-token-with-a-scope-containing-read-inbox-this-m",
          "request": {
            "url": "http://api.stackexchange.com/2.2/inbox?callback=%7B%7D&filter=%7B%7D&page=%7B%7D&pagesize=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns a user's inbox.\n \nThis method requires an access_token, with a scope containing \"read_inbox\".\n \nThis method returns a list of inbox items."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a34aa87d-14de-407b-b911-496a2cdc00e6"
            }
          ]
        },
        {
          "id": "ce1b4c5b-ea84-45fa-a865-0755428da8e0",
          "name": "returns-the-unread-items-in-a-users-inbox-this-method-requires-an-access-token-with-a-scope-containi",
          "request": {
            "url": "http://api.stackexchange.com/2.2/inbox/unread?callback=%7B%7D&filter=%7B%7D&page=%7B%7D&pagesize=%7B%7D&since=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the unread items in a user's inbox.\n \nThis method requires an access_token, with a scope containing \"read_inbox\".\n \nThis method returns a list of inbox items."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "94bedc0e-7949-4e33-be0c-1267295e61cf"
            }
          ]
        },
        {
          "id": "75110a16-afe9-424d-bc7b-8da8647385ad",
          "name": "returns-the-user-identified-by-access-tokens-inbox-this-method-requires-an-access-token-with-a-scope",
          "request": {
            "url": "http://api.stackexchange.com/2.2/me/inbox?callback=%7B%7D&filter=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the user identified by access_token's inbox.\n \nThis method requires an access_token, with a scope containing \"read_inbox\".\n \nThis method returns a list of inbox items."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "976bdd4e-5507-425b-bdb5-b65daaa5ceed"
            }
          ]
        },
        {
          "id": "339e99dd-7d6d-4d66-a845-666f985bfbe4",
          "name": "returns-the-unread-items-in-the-user-identified-by-access-tokens-inbox-this-method-requires-an-acces",
          "request": {
            "url": "http://api.stackexchange.com/2.2/me/inbox/unread?callback=%7B%7D&filter=%7B%7D&page=%7B%7D&pagesize=%7B%7D&since=%7B%7D&site=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the unread items in the user identified by access_token's inbox.\n \nThis method requires an access_token, with a scope containing \"read_inbox\".\n \nThis method returns a list of inbox items."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "dcb8d17a-5b51-40bd-85b5-54fdc22f2ba9"
            }
          ]
        }
      ]
    },
    {
      "name": "Information",
      "item": [
        {
          "id": "4dce9ec7-5dcf-43f1-8799-4da679a61f1c",
          "name": "returns-a-collection-of-statistics-about-the-site-data-to-facilitate-persite-customization-discover-",
          "request": {
            "url": "http://api.stackexchange.com/2.2/info?site=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns a collection of statistics about the site.\n \nData to facilitate per-site customization, discover related sites, and aggregate statistics is all returned by this method.\n \nThis data is cached very aggressively, by design. Query sparingly, ideally no more than once an hour.\n \nThis method returns an info object."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8970354d-9bbd-4a58-afdf-58b4ff4da796"
            }
          ]
        }
      ]
    },
    {
      "name": "Self",
      "item": [
        {
          "id": "68c7ef4b-75fd-478b-8cfe-5da04ef224b3",
          "name": "returns-the-user-associated-with-the-passed-access-token-this-method-returns-a-user",
          "request": {
            "url": "http://api.stackexchange.com/2.2/me?callback=%7B%7D&filter=%7B%7D&fromdate=%7B%7D&max=%7B%7D&min=%7B%7D&order=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D&sort=%7B%7D&todate=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the user associated with the passed access_token.\n \nThis method returns a user."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e2198f0e-88bc-46c7-9bd5-5896231427ab"
            }
          ]
        }
      ]
    },
    {
      "name": "Associated",
      "item": [
        {
          "id": "4423f2ad-cc75-45d2-b060-78b35acf2b61",
          "name": "returns-all-of-a-users-associated-accounts-given-an-access-token-for-them-this-method-returns-a-list",
          "request": {
            "url": "http://api.stackexchange.com/2.2/me/associated?callback=%7B%7D&filter=%7B%7D&page=%7B%7D&pagesize=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns all of a user's associated accounts, given an access_token for them.\n \nThis method returns a list of network users."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "6ae52756-89ce-4ffb-b88e-cea044c0336c"
            }
          ]
        }
      ]
    },
    {
      "name": "Favorites",
      "item": [
        {
          "id": "ecf8a516-e973-48a2-b331-0972c267bbb3",
          "name": "returns-the-questions-favorites-by-the-user-associated-with-the-given-access-token-this-method-retur",
          "request": {
            "url": "http://api.stackexchange.com/2.2/me/favorites?callback=%7B%7D&filter=%7B%7D&fromdate=%7B%7D&max=%7B%7D&min=%7B%7D&order=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D&sort=%7B%7D&todate=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the questions favorites by the user associated with the given access_token.\n \nThis method returns a list of questions."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "eb5f26ce-8fbb-49d9-a999-af57db86b1cb"
            }
          ]
        }
      ]
    },
    {
      "name": "Mentioned",
      "item": [
        {
          "id": "9ae819f2-d07e-4206-b725-897695efb9cb",
          "name": "returns-the-comments-mentioning-the-user-associated-with-the-given-access-token-this-method-returns-",
          "request": {
            "url": "http://api.stackexchange.com/2.2/me/mentioned?callback=%7B%7D&filter=%7B%7D&fromdate=%7B%7D&max=%7B%7D&min=%7B%7D&order=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D&sort=%7B%7D&todate=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the comments mentioning the user associated with the given access_token.\n \nThis method returns a list of comments."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c1449e5f-a064-4e74-9dd8-130ef43722a7"
            }
          ]
        }
      ]
    },
    {
      "name": "Merges",
      "item": [
        {
          "id": "06aee7b0-24ed-43f2-8c5f-dbd0b18c252f",
          "name": "returns-a-record-of-merges-that-have-occurred-involving-a-user-identified-by-an-access-token-this-me",
          "request": {
            "url": "http://api.stackexchange.com/2.2/me/merges?callback=%7B%7D&filter=%7B%7D&page=%7B%7D&pagesize=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns a record of merges that have occurred involving a user identified by an access_token.\n \nThis method allows you to take now invalid account ids and find what account they've become, or take currently valid account ids and find which ids were equivalent in the past.\n \nThis is most useful when confirming that an account_id is in fact \"new\" to an application.\n \nAccount merges can happen for a wide range of reasons, applications should not make assumptions that merges have particular causes.\n \nNote that accounts are managed at a network level, users on a site may be merged due to an account level merge but there is no guarantee that a merge has an effect on any particular site.\n \nThis method returns a list of account_merge."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c8e920ed-0235-4ac2-8154-1acba286bc9e"
            }
          ]
        }
      ]
    },
    {
      "name": "Notifications",
      "item": [
        {
          "id": "68e3f9c0-08ec-4310-b269-10a2d900e5ae",
          "name": "returns-a-users-notifications-given-an-access-token-this-method-requires-an-access-token-with-a-scop",
          "request": {
            "url": "http://api.stackexchange.com/2.2/me/notifications?callback=%7B%7D&filter=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns a user's notifications, given an access_token.\n \nThis method requires an access_token, with a scope containing \"read_inbox\".\n \nThis method returns a list of notifications."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "556b0dd4-4a4e-42b9-9b92-39a6fa928dcb"
            }
          ]
        },
        {
          "id": "333780f9-3700-41ba-a847-a0a4a6b98589",
          "name": "returns-a-users-unread-notifications-given-an-access-token-this-method-requires-an-access-token-with",
          "request": {
            "url": "http://api.stackexchange.com/2.2/me/notifications/unread?callback=%7B%7D&filter=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns a user's unread notifications, given an access_token.\n \nThis method requires an access_token, with a scope containing \"read_inbox\".\n \nThis method returns a list of notifications."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3bc9b213-394f-426d-a6cb-595dba7d313d"
            }
          ]
        },
        {
          "id": "9b2afc7f-17f8-4621-b131-78c1d7fdf60b",
          "name": "returns-a-users-notifications-this-method-requires-an-access-token-with-a-scope-containing-read-inbo",
          "request": {
            "url": "http://api.stackexchange.com/2.2/notifications?callback=%7B%7D&filter=%7B%7D&page=%7B%7D&pagesize=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns a user's notifications.\n \nThis method requires an access_token, with a scope containing \"read_inbox\".\n \nThis method returns a list of notifications."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "7fbbfed7-b265-402e-982b-d176ba94ef04"
            }
          ]
        },
        {
          "id": "438ec89f-455e-403e-afcd-054708d4c518",
          "name": "returns-a-users-unread-notifications-this-method-requires-an-access-token-with-a-scope-containing-re",
          "request": {
            "url": "http://api.stackexchange.com/2.2/notifications/unread?callback=%7B%7D&filter=%7B%7D&page=%7B%7D&pagesize=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns a user's unread notifications.\n \nThis method requires an access_token, with a scope containing \"read_inbox\".\n \nThis method returns a list of notifications."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "05caeb2d-2394-4541-8483-481662073a09"
            }
          ]
        }
      ]
    },
    {
      "name": "Privileges",
      "item": [
        {
          "id": "93aa1fe8-ebd6-4424-86de-63f5884be266",
          "name": "returns-the-privileges-the-user-identified-by-access-token-has-this-method-returns-a-list-of-privile",
          "request": {
            "url": "http://api.stackexchange.com/2.2/me/privileges?callback=%7B%7D&filter=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the privileges the user identified by access_token has.\n \nThis method returns a list of privileges."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "395e46ec-9a77-4d66-a42b-5787874c394c"
            }
          ]
        },
        {
          "id": "af675eb0-38a5-408c-82b9-69e735aee66c",
          "name": "returns-the-earnable-privileges-on-a-site-privileges-define-abilities-a-user-can-earn-via-reputation",
          "request": {
            "url": "http://api.stackexchange.com/2.2/privileges?callback=%7B%7D&filter=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the earnable privileges on a site.\n \nPrivileges define abilities a user can earn (via reputation) on any Stack Exchange site.\n \nWhile fairly stable, over time they do change. New ones are introduced with new features, and the reputation requirements change as a site matures.\n \nThis method returns a list of privileges."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "17fae00c-4bbf-4e60-a63a-90311d326cd4"
            }
          ]
        }
      ]
    },
    {
      "name": "Questions",
      "item": [
        {
          "id": "9cac8995-2f62-4328-9834-c705a0d66647",
          "name": "returns-the-questions-owned-by-the-user-associated-with-the-given-access-token-this-method-returns-a",
          "request": {
            "url": "http://api.stackexchange.com/2.2/me/questions?callback=%7B%7D&filter=%7B%7D&fromdate=%7B%7D&max=%7B%7D&min=%7B%7D&order=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D&sort=%7B%7D&todate=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the questions owned by the user associated with the given access_token.\n \nThis method returns a list of questions."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "7e129cf7-7d18-450d-a615-5c1acbbb3479"
            }
          ]
        },
        {
          "id": "e7215245-2dec-42e5-a20a-9ce477c99a0c",
          "name": "returns-the-questions-that-have-active-bounties-offered-by-the-user-associated-with-the-given-access",
          "request": {
            "url": "http://api.stackexchange.com/2.2/me/questions/featured?callback=%7B%7D&filter=%7B%7D&fromdate=%7B%7D&max=%7B%7D&min=%7B%7D&order=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=