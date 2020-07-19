`Authentication is done using JSON WEB TOKENS`

# END POINTS IN AUTH ROUTE

- `api/auth`

  > GET Request.

  > For Getting Logged in user

  > Access Private

  Sample success response

  ```
  {
      token:"eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VyIjp7ImlkIjoiNWVkYjQyYjY4YmM5OTczZTJkOTI3Nzc5In0sImlhdCI6MTU5NDk4NDEyNiwiZXhwIjoxNTk1MDIwMTI2fQ.XfsyaiFLbD0BnxUA296eC8OlV1DyoESoo_mJ5gRbzdo"
  }

  ```

  (Token will be actually stored in header as 'x-auth-token')

  Error message

  ```
    {
    "errors": [
        {
            "msg": "Invalid Token,Authorization denied"
        }
    ]

  }
  ```

- `api/auth`

  > POST Request.

  > Authenticate user and get token

  > Access Public

  Sample Query

  ```
  {
  "email":"techguyinfo@gmail.com",
  "password":"codewithak"
  }
  ```

  Sample success response

  ```
  {
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VyIjp7ImlkIjoiNWVkYjQyYjY4YmM5OTczZTJkOTI3Nzc5In0sImlhdCI6MTU5NDk4NDEyNiwiZXhwIjoxNTk1MDIwMTI2fQ.XfsyaiFLbD0BnxUA296eC8OlV1DyoESoo_mJ5gRbzdo"
  }
  ```

  Sample error message

  ```
  {
    "errors": [
        {
            "msg": "Invalid Credentials"
        }
    ]
  }
  ```
