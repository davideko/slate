## Get a Specific Employee Role
This endpoint retrieves specific employee role.

> Sample request

```shell
  curl "http://localhost:8080/api/employee-roles/4736464f-d073-4957-9fbf-4b38c7add85e@5"
  -H "Authorization: Bearer <token>"
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

`GET http://localhost:8080/api/employees-roles/{employeeRolePk}`

### URL Parameters

Parameter | Description | Format
--------- | ----------- | ---------
employeeRolePk | Employee role pk to retrieve | String