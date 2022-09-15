## POST Book
- End Point URL: `/book/add`
    - Method: `POST`
    - Accept: `multipart/form-data`
    - Content-Type: `application/json`
    - Header:
      | Header 	| Type     | Description                |
      | :-------- | :------- | :------------------------- |
      | `X-API-KEY` | `string` | **Required**. Your API key |
      - Post Form Body
        | Key               | Type     | Description                  | Referred    |
        | :--------         | :------- | :-------------------------   | :--------   |
        | `name`            | `string` | **Required**. Full Name      | None        |
        | `category_id`     | `string` | **Required**. Category ID    | [Category ID](../category/CategoryGetById.md) |  
        | `stock`           | `int`    | **Required**. Stock          | None |
        | `products_status` | `string` | **Required**. Product Status | None |
        | `img_url`         | `string` | **Required**. IMG Url        | None |
    - Response Body
      ```json
      {
          "code": 200,
          "status": "OK",
          "data": {
              "id": 37,
              "name": "Buku Kita",
              "category_id": 6,
              "stock": 10,
              "products_status": "in_stock",
              "img_url": "https://i.picsum.photos/id/128/200/300.jpg"
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
              "error": "Book dengan ID 10 tidak ditemukan"
          }
      }
      ```
        - Bad Request
      ```json
      {
          "code": 400,
          "status": "Bad Request",
          "data": {
              "error": "Book tidak boleh kosong"
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