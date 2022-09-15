## PUT Guest Book
- End Point URL: `/user/update/{userId}`
    - Method: `PUT`
    - Accept: `multipart/form-data`
    - Content-Type: `application/json`
    - Header:
      | Header 	| Type     | Description                |
      | :-------- | :------- | :------------------------- |
      | `X-API-KEY` | `string` | **Required**. Your API key |
    - Post Form:
        | Key 	       | Value     | Description              | Referred                                       | Format             |
        | :--------    | :------- | :-------------------------|:--------------------------------------------   | :----------------- |
        | `user_id`    | `int`    | **Required**. User ID     |  [user_id](../user/UserGetById.md)             | None               |
        | `officer_id` | `int`    | **Required**. Officer ID  |  [officer_id](../officer/OfficerGetById.mdmd)  | None               |
        | `book_id`    | `int`    | **Required**. Book ID     |  [book_id](../book/BookGetById.md)             | None               |
        | `end_date`   | `string` | **Required**. Datetime    |  None                                          | yyyy-mm-dd HH-mm-ss|
    - Response Body:
      ```json
          {
            "code": 200,
            "status": "OK",
            "data": {
                "id": 35,
                "user_id": 72,
                "officer_id": 1,
                "book_id": 7,
                "start_date": "2022-09-15T20:50:37+07:00",
                "end_date": "2022-09-16T15:20:20Z"
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
        - Bad Request
      ```json
      {
          "code": 400,
          "status": "Bad Request",
          "data": {
              "error": "Username telah terdaftar"
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
