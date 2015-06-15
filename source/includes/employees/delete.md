## Delete Employee
This endpoint will delete employee by ID.

> Sample request

```shell
  curl "http://localhost:8080/api/employees/045d9baa-2c68-4390-a385-a4bfef33e9dd"
  -X DELETE
  -H "Authorization: Bearer <token>"
```

### HTTP Request

`DELETE http://localhost:8080/api/employees/{employeeId}`

### URL Parameters

Parameter | Description | Data Type
--------- | ----------- | ---------
employeeId | Employee ID to delete | string