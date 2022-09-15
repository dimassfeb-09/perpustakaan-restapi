## GET Users
- End Point URL: `/user`
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
              "id": 72,
              "name": "Ilman",
              "username": "ilman",
              "email": "ilma@gmail.com",
              "level": "Mahasiswa"
            },
            {
              "id": 74,
              "name": "Dimas",
              "username": "dimas",
              "email": "dimas@gmail.com",
              "level": "mahasiswa"
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
