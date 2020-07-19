# END POINTS IN ADMIN ROUTE

- `api/admins`

  > GET Request.

  > Get all admins

  > Access Private (Token must be given in header)

  Sample Success Response

  ```
  {
    [
        {
            "id":"111",
            "name":"Admin",
            "role":""
        }
    ]
  }
  ```

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

* `api/admins`

  > POST Request.

  > Add new admin

  > Access Private (Token must be given in header)

  Sample Query

  ```
  {
  "name":"xyz",
  "role":"aaa",
  "ScheduleTime":"",
  "ScheduleDestination":"",
  "ScheduleAction":"",
  "Info":""
  }
  ```

  Success Message

  ```
  {
      "msg":"Admin added successfully"
  }
  ```

  Error messages

  ```
  {
      errors:[
          {
              "msg":"Name is required"
          }
      ]
  }
  ```

  ```
  {
  "errors": [
      {
          "msg": "Invalid Token,Authorization denied"
      }
  ]

  }
  ```

* `api/classrooms`

  > GET Request.

  > Get all classrooms

  > Access Private (Token must be given in header)

  Sample Success Response

  ```
  {
    [
        {
            "id":"111",
            "name":"Classroom 1",
            "Teacher":"Aleena"
        },
        {
            "id":"132",
            "name":"Classroom 2",
            "Teacher":"Melina"
        },
        {
            "id":"151",
            "name":"Classroom 3",
            "Teacher":"Nelson"
        },
        {
            "id":"180",
            "name":"Classroom 4",
            "Teacher":"Bamboo"
        }
    ]
  }
  ```

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

* `api/classrooms`

  > POST Request.

  > Add new classroom

  > Access Private (Token must be given in header)

  Sample Query

  ```
  {
    "name":"Classroom 5",
    "Teacher":"Bubsa"
  }
  ```

  Success Message

  ```
  {
      "msg":"Classroom added successfully"
  }
  ```

  Error messages

  ```
  {
      errors:[
          {
              "msg":"Teacher is required"
          }
      ]
  }
  ```

  ```
  {
  "errors": [
      {
          "msg": "Invalid Token,Authorization denied"
      }
  ]

  }
  ```
