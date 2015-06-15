# Employee Role

## Get all Employee Role
This endpoint retrieves all employee role.

> Sample request

```shell
  curl "http://localhost:8080/api/employees-roles"
  -H "Authorization: Bearer <token>"
```

> Sucessful response

```json
{
  "_embedded" : {
    "employeesRoles" : [ {
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
    } ]
  }
}
```

### HTTP Request

`GET http://localhost:8080/api/employees-roles`

