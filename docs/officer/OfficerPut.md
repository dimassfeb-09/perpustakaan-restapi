## PUT Officer
- End Point URL: `/officer/update/{officerId}`
    - Method: `PUT`
    - Accept: `multipart/form-data`
    - Content-Type: `application/json`
    - Header:
      | Header 	| Type     | Description                |
      | :-------- | :------- | :------------------------- |
      | `X-API-KEY` | `string` | **Required**. Your API key |
    - Post Form Body:
      | Header 	| Type     | Description                |
      | :-------- | :------- | :------------------------- |
      | `name` | `string` | **Required**. FulL Name |
      | `position` | `string` | **Required**. Position |
      | `phone` | `string` | **Required**. Phone |
      | `address` | `string` | **Required**. Address |
    - Response Body
      ```json
      {
          "code": 200,
          "status": "OK",
          "data": {
              "id": 1,
              "name": "Bjorkan NISM",
              "position": "staff",
              "phone": "0823123xxx",
              "address": "Jalan Hackel Nganggur"
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
              "error": "Officer dengan ID 10 tidak ditemukan"
          }
      }
      ```
        - Bad Request
      ```json
      {
          "code": 400,
          "status": "Bad Request",
          "data": {
              "error": "Officer tidak boleh kosong"
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