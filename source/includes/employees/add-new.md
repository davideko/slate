## Add New Employee
This endpoint will create new employee.

> Sample request

```shell
  curl "http://localhost:8080/api/employees"
  -X POST
  -H "Authorization: Bearer <token>"
  -d '{
    "employeeName" : "David Eko"
  }'
```

> Success response

```json
{
  "employeeName" : "David Eko",
  "_links" : {
    "self" : {
      "href" : "http://localhost:8080/api/employees/045d9baa-2c68-4390-a385-a4bfef33e9dd"
    },
    "employeeRoles" : {
      "href" : "http://localhost:8080/api/employees/045d9baa-2c68-4390-a385-a4bfef33e9dd/employeeRoles"
    }
  }
}
```

### HTTP Request

`POST http://localhost:8080/api/employees`

###  Parameters

Parameter | Description | Format
--------- | ----------- | ---------
employeeName | New employee name | string
