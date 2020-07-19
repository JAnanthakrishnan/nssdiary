# END POINTS IN STUDENT ROUTE

- `api/my`

  > GET Request.

  > Get completed hours

  > Access Private (Token must be given in header)

  Sample Response

  ```
  {
      "CompletedHours":"7"
  }
  ```

  Error Message

  ```
  {
      errors:[
          {
              "msg": "Invalid Token,Authorization denied"
          }
      ]
  }
  ```

* `api/my`

  > POST Request.

  > Add work hours

  > Access Private (Token must be given in header)

  Sample Query

  ```
    {
      "farmWork":"3",
      "socialWork":"8"
    }
  ```

  Sample Response

  ```
  {
      "msg":"Updated hours"
  }
  ```

  Error Message

  ```
  {
      errors:[
          {
              "msg": "Invalid Token,Authorization denied"
          }
      ]
  }
  ```
