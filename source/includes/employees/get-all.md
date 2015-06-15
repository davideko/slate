# Employee

## Get All employee
This endpoint retrieves all employees.

> Sample request

```shell
  curl "http://localhost:8080/api/employees"
  -H "Authorization: Bearer <token>"
```

> Sucessful response

```json
{
  "_embedded" : {
    "employees" : [ {
      "employeeName" : "DAPIDSSS",
      "_links" : {
        "self" : {
          "href" : "http://localhost:8080/api/employees/045d9baa-2c68-4390-a385-a4bfef33e9dd"
        },
        "employeeRoles" : {
          "href" : "http://localhost:8080/api/employees/045d9baa-2c68-4390-a385-a4bfef33e9dd/employeeRoles"
        }
      }
    }, {
      "employeeName" : "Nico Natalie",
      "_links" : {
        "self" : {
          "href" : "http://localhost:8080/api/employees/0f9f0bfa-3e67-498c-bb5d-84a94b56d804"
        },
        "employeeRoles" : {
          "href" : "http://localhost:8080/api/employees/0f9f0bfa-3e67-498c-bb5d-84a94b56d804/employeeRoles"
        }
      }
    } ]
  }
}
```

### HTTP Request

`GET http://localhost:8080/api/employees`

