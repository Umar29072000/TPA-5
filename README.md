# Node.js + MongoDB: JWT Authentication & Authorization

### Project TPA-5 Skillvul

## Features
- Register user,admin, moderator
- Login user, admin, moderator
- Authenticated user will get a token
- User can't access someone else's todo
- Get all 
- Show by ID
- Create 
- Update by ID
- Delete by ID
- Delete all

## API Documentation
URL: 

### Register
* #### URL
  /register

* #### Method:
  `POST`

*  #### URL Params
   None

* #### Request body
  ```sh
    {
    "username": "Afif",
    "email": "afiftajir@gmail.com",
    "password": "290700",
    "roles": ["user"]
    }
  ```

* #### Success Response:
  * ##### Code:
    200
  * ##### Content: 
    `{"message": "User was registered successfully!"}`

* #### Error Response:
  * ##### Code:
    400 CONFLICT
  * ##### Content:
    `{ message: "Failed! Username is already in use!" }`

### Login
* #### URL
  /login

* #### Method:
  `POST`
  
* #### URL Params
  None

* #### Request header
  None

* #### Request body
  ```sh
    {
    "username": "Afif",
    "password": "290700"
    }
  ```

* #### Success Response:
  * ##### Code:
    200
  * ##### Content: 
    ```sh
    {
        "accessToken": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...."
    }
    ```

* #### Error Response:
  * ##### Code:
    401 Unauthorized
  * ##### Content:
    `{ "message": "Invalid Password!" }`


