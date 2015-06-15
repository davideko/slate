
## Get a Specific Employee
This endpoint retrieves specific employee.

> Sample request

```shell
  curl "http://localhost:8080/api/employees/045d9baa-2c68-4390-a385-a4bfef33e9dd"
  -H "Authorization: Bearer <token>"
```

> Success response

```json
{
  "employeeName" : "DAPIDSSS",
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

`GET http://localhost:8080/api/employees/{employeeId}`

### URL Parameters

Parameter | Description | Format
--------- | ----------- | ---------
employeeId | Employee ID to retrieve | String