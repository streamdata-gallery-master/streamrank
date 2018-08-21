{
  "info": {
    "name": "Stack Exchange",
    "_postman_id": "c3268ef6-9f78-4244-9b99-06d9f312e147",
    "description": "Stack Exchange is a network of 130+ Q&amp;A communities including Stack Overflow.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "answers",
      "item": [
        {
          "id": "a26cd26e-bc42-4360-b7f6-a27c18aaf758",
          "name": "returns-all-the-undeleted-answers-in-the-system-the-sorts-accepted-by-this-method-operate-on-the-fol",
          "request": {
            "url": "http://api.stackexchange.com/2.2/answers?callback=%7B%7D&filter=%7B%7D&fromdate=%7B%7D&max=%7B%7D&min=%7B%7D&order=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D&sort=%7B%7D&todate=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns all the undeleted answers in the system"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b018188c-dc4b-426d-a979-4ce3e2349ae9"
            }
          ]
        }
      ]
    }
  ]
}