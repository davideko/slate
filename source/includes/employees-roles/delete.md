## Delete Employee Role
This endpoint will delete employee role by ID.

> Sample request

```shell
  curl "http://localhost:8080/api/employees-roles/4736464f-d073-4957-9fbf-4b38c7add85e@5"
  -X DELETE
  -H "Authorization: Bearer <token>"
```

### HTTP Request

`DELETE http://localhost:8080/api/employees-roles/{employeeRolePk}`

### URL Parameters

Parameter | Description | Data Type
--------- | ----------- | ---------
employeeRolePk | Composite key object | object