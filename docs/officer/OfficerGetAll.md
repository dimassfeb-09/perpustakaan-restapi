## GET All Officers
- End Point URL: `/officer`
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
              "id": 1,
              "name": "Rahmini",
              "position": "staff",
              "phone": "082312371231",
              "address": "Jalan Mencari Jodoh"
            },
            {
              "id": 2,
              "name": "Ratu Elizabeth II",
              "position": "staff",
              "phone": "082312731213",
              "address": "Jalan Mencari Surga"
            }   
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