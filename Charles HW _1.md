## ﻿Charles HW Traffic capture

#### Ex_0: Focus on the following requests

Protocol: http

IP: 162.55.220.72

Port: 5005

#### Ex_1: 

Method: GET

EndPoint: /get_method

request url params: 

 ```
 name: str
 age: int
```

response: 
```
[
    “Str”,
    “Str”
]
```

Task:

To be created in Rewrite as well as in BreakPoint (can be disabled so that it doesn’t freeze on every request):
- Replace url in Charles so that the name filled in in Postman in the request is sent, but the name filled in in Charles is recieved.

==================
#### Ex_2:

Method: POST

EndPoint: /user_info_3

request form data: 

```
name: str
age: int
salary: int
```
response: 
```
{'name': name,
          'age': age,
          'salary': salary,
          'family': {'children': [['Alex', 24], ['Kate', 12]],
                     'u_salary_1_5_year': salary * 4}}
```

Task:

To be created in Rewrite as well as in BreakPoint (can be disabled so that it doesn’t freeze on every request):
- Replace body in Charles so that salary filled in in Postman in the request is sent, but the value of u_salary_1_5_year less that the original one in the request is recieved.

==================
#### Ex_3:

Method: GET

EndPoint: /object_info_1

request url params: 
```
 name: str
 age: int
 weight: int
```

response: 
```
{'name': name,
          'age': age,
          'daily_food': weight * 0.012,
          'daily_sleep': weight * 2.5}
```

Task:

To be created in Rewrite as well as in BreakPoint (can be disabled so that it doesn’t freeze on every request):
- Replace request params in Charles so that the response with another name, daily_food > weight of the request, as well as daily_sleep < weight of the request is recieved in Postman.

==================
#### Ex_4:

Method: GET

EndPoint: /object_info_3

request url params: 
```
 name: str
 age: int
 salary: int
```

response: 
```
{'name': name,
          'age': age,
          'salary': salary,
          'family': {'children': [['Alex', 24], ['Kate', 12]],
                     'pets': {'cat':{'name':'Sunny',
                                     'age': 3},
                              'dog':{'name':'Luky',
                                     'age': 4}},
                     'u_salary_1_5_year': salary * 4}
          }
```

Task:

To be created in Rewrite as well as in BreakPoint (can be disabled so that it doesn’t freeze on every request):
- Create in Charles so that Code 500 is returned by the server.
- Create in Charles so that Code 405 is returned by the server.

==================
#### Ex_5:

Method: GET

EndPoint: /object_info_4

request url params: 
```
 name: str
 age: int
 salary: int
```

response: 
```
{'name': name,
          'age': int(age),
          'salary': [salary, str(salary * 2), str(salary * 3)]}
```

Task:
To be created in Rewrite as well as in BreakPoint (can be disabled so that it doesn’t freeze on every request):
- Create in Charles so that Code 405 is returned by the server.
- Replace salary in the request.
- Replace (salary * 2) in the response.

==================
#### Ex_6:

Method: POST

EndPoint: /user_info_2

request form data: 
```
 name: str
 age: int
 salary: int
```

response: 
```
{'start_qa_salary': salary,
          'qa_salary_after_6_months': salary * 2,
          'qa_salary_after_12_months': salary * 2.7,
          'qa_salary_after_1.5_year': salary * 3.3,
          'qa_salary_after_3.5_years': salary * 3.8,
          'person': {'u_name': [user_name, salary, age],
                     'u_age': age,
                     'u_salary_5_years': salary * 4.2}
          }
```

Task:

To be created in Rewrite as well as in BreakPoint (can be disabled so that it doesn’t freeze on every request):
- Create in Charles so that response with qa_salary_after_1.5_year replaced to qa_salary_after_1.5_month is returned in Postman.
- Create so that qa_salary_after_3.5_years less than qa_salary_after_12_months to be in response.

#### All Charles settings to be uploaded in GitHub.
