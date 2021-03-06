## Update employee
This endpoint will update employee by ID.

> Sample request PUT

```shell
  curl "http://localhost:8080/api/employees/045d9baa-2c68-4390-a385-a4bfef33e9dd"
  -X PUT
  -H "Authorization: Bearer <token>"
  -d '{
    "employeeName" : "David Eko Wibowo"
  }'
```

> Sample request PATCH

```shell
  curl "http://localhost:8080/api/employees/045d9baa-2c68-4390-a385-a4bfef33e9dd"
  -X PATCH
  -H "Authorization: Bearer <token>"
  -d '{
    "employeeName" : "David Eko Wibowo"
  }'
```

> Success response

```json
{
  "employeeName" : "David",
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

`PUT http://localhost:8080/api/employees/{employeeId}`

`PATCH http://localhost:8080/api/employees/{employeeId}`

### URL Parameters

Parameter | Description | Format
--------- | ----------- | ---------
employeeId | Employee ID to update | String

### Parameters

Parameter | Description | Format
--------- | ----------- | ---------
employeeName | New employee name | String