## GET Guest Books
- End Point URL: `/guestbook`
    - Method: `GET`
    - Content-Type: `application/json`
    - Header:
      | Header 	| Type     | Description                |
      | :-------- | :------- | :------------------------- |
      | `X-API-KEY` | `string` | **Required**. Your API key |
    - Response Body
      ```json
      {
         "code": 200,
         "status": "OK",
         "data": [
            {
              "id": 18,
              "user_id": 72,
              "officer_id": 1,
              "book_id": 10,
              "start_date": "2022-09-15T19:19:36Z",
              "end_date": "2022-12-05T15:20:20Z"
            },
            {
              "id": 19,
              "user_id": 74,
              "officer_id": 1,
              "book_id": 7,
              "start_date": "2022-09-15T12:30:21Z",
              "end_date": "2022-12-20T15:20:20Z"
            },
        ]
      }
      ```
    - Response Error
        - Internal Server Error
        ```json
        {
          "code": 500,
          "status": "Status Internal Server Error",
          "data": {
              "error": "Status Internal Server Error"
          }
        }
        ```
