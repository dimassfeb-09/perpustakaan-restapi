## PUT User
- End Point URL: `/user/update/{userId}`
    - Method: `PUT`
    - Accept: `multipart/form-data`
    - Content-Type: `application/json`
    - Header:
      | Header 	| Type     | Description                |
      | :-------- | :------- | :------------------------- |
      | `X-API-KEY` | `string` | **Required**. Your API key |
    - Post Form:
      | Key 	    | Value     | Description                |
      | :-------- | :------- | :------------------------- |
      | `name` | `string` | **Required**. Full Name |
      | `username` | `string` | **Required**. Username |
      | `password` | `string` | **Required**. Password |
      | `email` | `string` | **Required**. Email |
      | `level` | `string` | **Required**. Level `Mahasiswa/Staff`|
    - Response Body
      ```json
      {
        "code": 200,
        "status": "OK",
        "data": {
          "id": 82,
          "name": "Buku Kita",
          "username": "dimas123123",
          "email": "qye@gmail.com",
          "level": "mahasiswa"
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
