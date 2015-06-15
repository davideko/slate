## Delete TPL
This endpoint will delete TPL by ID.

> Sample request

```shell
  curl "http://localhost:8080/api/tpls/1"
  -X DELETE
  -H "Authorization: Bearer <token>"
```

> Success response <code>HTTP 204 No Content</code>

### HTTP Request

`DELETE http://localhost:8080/api/tpls/{tplId}`

### URL Parameters

Parameter | Description | Format
--------- | ----------- | ---------
tplId | TPL ID to delete | String