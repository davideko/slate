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

> Success response

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

Parameter | Description | Format
--------- | ----------- | ---------
roleType | New role type | String
