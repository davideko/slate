## Update Role
This endpoint will update role by ID.

> Sample request PUT

```shell
  curl "http://localhost:8080/api/roles/1"
  -X PUT
  -H "Authorization: Bearer <token>"
  -d '{
    "roleType" : "CTO"
  }'
```

> Sample request PATCH

```shell
  curl "http://localhost:8080/api/roles/1"
  -X PATCH
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

`PUT http://localhost:8080/api/roles/{roleId}`

`PATCH http://localhost:8080/api/roles/{roleId}`

### URL Parameters

Parameter | Description | Format
--------- | ----------- | ---------
roleId | Role ID to update | integer

### Parameters

Parameter | Description | Format
--------- | ----------- | ---------
roleType | New role type | String