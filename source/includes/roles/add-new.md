## Add New Role
This endpoint will create new role.

> Sample request

```shell
  curl "http://localhost:8080/api/roles"
  -X POST
  -H "Authorization: Bearer <token>"
  -d '{
    "roleType" : "CTO"
  }'
```

> Sucessful response

```json
{
  "roleType" : "CTO",
  "_links" : {
    "self" : {
      "href" : "http://localhost:8080/api/roles/1"
    }
  }
}
```

### HTTP Request

`POST http://localhost:8080/api/roles/`

###  Parameters

Parameter | Description | Data Type
--------- | ----------- | ---------
roleType | New role type | string
