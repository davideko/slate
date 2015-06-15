# Role

## Get All Role
This endpoint retrieves all role.

> Sample request

```shell
  curl "http://localhost:8080/api/roles"
  -H "Authorization: Bearer <token>"
```

> Success response

```json
{
  "_embedded" : {
    "roles" : [ {
      "roleType" : "Manager",
      "_links" : {
        "self" : {
          "href" : "http://localhost:8080/api/roles/1"
        }
      }
    }, {
      "roleType" : "Customer Service",
      "_links" : {
        "self" : {
          "href" : "http://localhost:8080/api/roles/3"
        }
      }
    } ]
  }
}
```

### HTTP Request

`GET http://localhost:8080/api/roles`

