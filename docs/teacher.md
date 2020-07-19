# END POINTS IN TEACHER ROUTE

- `api/students`

  > GET Request.

  > Get all students

  > Access Private (Token must be given in header)

  Sample success response

  ```
  {
  [
  {
    "ID": "1",
    "Name": "Senpai",
    "ScheduleTime": "7_7_8_13.01_13.375_15.5_16_17.25_99_99",
    "ScheduleDestination": "Spawn_Locker_Hangout_Seat_LunchSpot_Seat_Clean_Hangout_Locker_Exit",
    "ScheduleAction": "Stand_Stand_Read_Sit_Eat_Sit_Clean_Read_Shoes_Stand",
    "Info": "An average student. \n \n Average grades, average looks, average life... \n \n I'm not sure what you see in him."
  },
  {
    "ID": "2",
    "Name": "Yui Rio",

    "ScheduleTime": "7_7_8_13_13.375_15.5_16_17.25_99_99",
    "ScheduleDestination": "Spawn_Locker_Hangout_Seat_LunchSpot_Seat_Clean_Club_Locker_Exit",
    "ScheduleAction": "Stand_Stand_Socialize_Sit_Socialize_Sit_Clean_SocialSit_Shoes_Stand",
    "Info": ""
  },
  {
    "ID": "3",
    "Name": "Yuna Hina",
    "ScheduleTime": "7_7_8_13_13.375_15.5_16_17.25_99_99",
    "ScheduleDestination": "Spawn_Locker_Hangout_Seat_LunchSpot_Seat_Clean_Club_Locker_Exit",
    "ScheduleAction": "Stand_Stand_Socialize_Sit_Socialize_Sit_Clean_SocialSit_Shoes_Stand",
    "Info": ""
  },
  {
    "ID": "4",
    "Name": "Koharu Hinata",
    "ScheduleTime": "7_7_8_13.0001_13.375_15.5001_16_17.25_99_99",
    "ScheduleDestination": "Spawn_Locker_Hangout_Seat_LunchSpot_Seat_Clean_Club_Locker_Exit",
    "ScheduleAction": "Stand_Stand_Socialize_Sit_Socialize_Sit_Clean_SocialSit_Shoes_Stand",
    "Info": ""
  },
  {
    "ID": "5",
    "Name": "Mei Mio",
    "ScheduleTime": "7_7_8_13_13.375_15.5_16_17.25_99_99",
    "ScheduleDestination": "Spawn_Locker_Hangout_Seat_LunchSpot_Seat_Clean_Club_Locker_Exit",
    "ScheduleAction": "Stand_Stand_Socialize_Sit_Socialize_Sit_Clean_SocialSit_Shoes_Stand",
    "Info": ""
  },
  {
    "ID": "6",
    "Name": "Saki Miyu",
    "ScheduleTime": "7_7_8_13.01_13.375_15.5_16_17.25_99_99",
    "ScheduleDestination": "Spawn_Locker_Hangout_Seat_LunchSpot_Seat_Clean_Club_Locker_Exit",
    "ScheduleAction": "Stand_Stand_Socialize_Sit_Socialize_Sit_Clean_SocialSit_Shoes_Stand",
    "Info": "Kokona Haruka's best friend and closest confidant. Kokona is likely to discuss personal matters with this girl."
  },
  {
    "ID": "7",
    "Name": "Kokona Haruka",
    "ScheduleTime": "7_7_8_13.01_13.375_15.51_16_17.25_99_99",
    "ScheduleDestination": "Spawn_Locker_Hangout_Seat_LunchSpot_Seat_Clean_Club_Locker_Exit",
    "ScheduleAction": "Stand_Stand_Socialize_Sit_Socialize_Sit_Clean_SocialSit_Shoes_Stand",
    "Info": ""
  },
  {
    "ID": "8",
    "Name": "Haruto Yuto",
    "ScheduleTime": "7_7_8_13_13.375_15.5_16_16.5_99",
    "ScheduleDestination": "Spawn_Locker_Hangout_Seat_LunchSpot_Seat_Clean_Locker_Exit",
    "ScheduleAction": "Stand_Stand_Socialize_Sit_Socialize_Sit_Clean_Shoes_Stand",
    "Info": ""
  },
  {
    "ID": "9",
    "Name": "Sota Yuki",
    "ScheduleTime": "7_7_8_13_13.375_15.5_16_16.5_99",
    "ScheduleDestination": "Spawn_Locker_Hangout_Seat_LunchSpot_Seat_Clean_Locker_Exit",
    "ScheduleAction": "Stand_Stand_Socialize_Sit_Socialize_Sit_Clean_Shoes_Stand",
    "Info": ""
  },
  {
    "ID": "10",
    "Name": "Hayato Haruki",
    "ScheduleTime": "7_7_8_13.0002_13.375_15.5002_16_16.5_99",
    "ScheduleDestination": "Spawn_Locker_Hangout_Seat_LunchSpot_Seat_Clean_Locker_Exit",
    "ScheduleAction": "Stand_Stand_Socialize_Sit_Socialize_Sit_Clean_Shoes_Stand",
    "Info": ""
  },
  {
    "ID": "11",
    "Name": "Ryusei Koki",
    "ScheduleTime": "7_7_8_13_13.375_15.5_16_16.5_99",
    "ScheduleDestination": "Spawn_Locker_Hangout_Seat_LunchSpot_Seat_Clean_Locker_Exit",
    "ScheduleAction": "Stand_Stand_Socialize_Sit_Socialize_Sit_Clean_Shoes_Stand",
    "Info": ""
  }]
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

* `api/students`

  > POST Request.

  > Add new student

  > Access Private (Token must be given in header)

  Sample Query

  ```
  {
  "name":"techguyinfo@gmail.com",
  "class":"",
  "rollNo":"",
  "ScheduleTime":"",
  "ScheduleDestination":"",
  "ScheduleAction":"",
  "Info":""
  }
  ```

  Success Message

  ```
  {
      "msg":"student added successfully"
  }
  ```

  Sample Error responses

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
      errors:[
          {
              "msg": "Invalid Token,Authorization denied"
          }
      ]
  }
  ```

- `api/students/:student_id`

  > GET Request.

  > View student hours

  > Access Private (Token must be given in header)

  Sample Success reponse

  ```
  {
      "name":"John Doe",
      "rollNo":"11111",
      "HoursCompleted":"0"
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

* `api/students/:student_id`

  > POST Request.

  > Approve or decline work

  > Access Private (Token must be given in header)

  Sample Query

  ```
  {
      "rollNo":"11111",
      "approved":"true"
  }
  ```

  Success Response

  ```
  {
      "msg":"Success"
  }
  ```

  Sample Error responses

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
      errors:[
          {
              "msg": "Invalid Token,Authorization denied"
          }
      ]
  }
  ```
