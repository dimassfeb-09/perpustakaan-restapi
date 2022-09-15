## GET GuestBook By ID
- End Point URL: `/guestbook/{guestBookId}`
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
          "data": {
              "id": 20,
              "user_id": 75,
              "officer_id": 1,
              "book_id": 13,
              "start_date": "2022-09-15T12:30:31Z",
              "end_date": "2022-12-20T15:20:20Z"
	        }
      }
      ```
    - Response Error
        - Bad Not Found
      ```json
      {
          "code": 404,
          "status": "Bad Not Found",
          "data": {
              "error": "Data tidak ditemukan",
          }
      }
      ```
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