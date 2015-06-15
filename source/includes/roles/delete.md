## Delete Role
This endpoint will delete role by ID.

> Sample request

```shell
  curl "http://localhost:8080/api/roles/1"
  -X DELETE
  -H "Authorization: Bearer <token>"
```

### HTTP Request

`DELETE http://localhost:8080/api/roles/{roleId}`

### URL Parameters

Parameter | Description | Data Type
--------- | ----------- | ---------
roleId | Role ID to delete | string