## Add New Employee Role
This endpoint will create new employee role.

> Sample request

```shell
  curl "http://localhost:8080/api/employees-roles"
  -X POST
  -H "Authorization: Bearer <token>"
  -d '{
    "employeeRolePk" : {
      "employee" : "http://localhost:8080/api/employees/4736464f-d073-4957-9fbf-4b38c7add85e",
      "role" : "http://localhost:8080/api/roles/5"
    }
  }'
```

> Success response

```json
{
  "employee" : {
    "employeeName" : "Resha"
  },
  "role" : {
    "roleType" : "Gamers"
  },
  "_links" : {
    "self" : {
      "href" : "http://localhost:8080/api/employees-roles/4736464f-d073-4957-9fbf-4b38c7add85e@5"
    },
    "role" : {
      "href" : "http://localhost:8080/api/employees-roles/4736464f-d073-4957-9fbf-4b38c7add85e@5/role"
    },
    "employee" : {
      "href" : "http://localhost:8080/api/employees-roles/4736464f-d073-4957-9fbf-4b38c7add85e@5/employee"
    }
  }
}
```

### HTTP Request

`POST http://localhost:8080/api/employees-roles`

###  Parameters

Parameter | Description | Format
--------- | ----------- | ---------
employeeRolePk | Composite key object | Object
