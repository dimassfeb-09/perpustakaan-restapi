## POST Officer
- End Point URL: `/officer/add`
    - Method: `POST`
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
              "name": "Ratu Elizabeth II",
              "position": "staff",
              "phone": "08239012313",
              "address": "Jalan Inggris Ganti Pemimpin"
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