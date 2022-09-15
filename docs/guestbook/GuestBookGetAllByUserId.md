## GET All GuestBook By User ID
- End Point URL: `/guestbook/user/{userId}`
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
              "id": 20,
              "name": "Ratu Elizabeth II",
              "book_name": "Motivasi Bertahan Hidup",
              "category_name": "Kehidupan"
            },
            {
              "id": 31,
              "name": "Ratu Elizabeth II",
              "book_name": "Pelajaran Hari Ini",
              "category_name": "Kehidupan"
            },
         ]
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
