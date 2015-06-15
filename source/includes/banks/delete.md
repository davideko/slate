## Delete Bank
This endpoint will delete bank by ID.

> Sample request

```shell
  curl "http://localhost:8080/api/banks/1"
  -X DELETE
  -H "Authorization: Bearer <token>"
```

> Success response <code>HTTP 204 No Content</code>

### HTTP Request

`DELETE http://localhost:8080/api/banks/{bankId}`

### URL Parameters

Parameter | Description | Format
--------- | ----------- | ---------
bankId | Bank ID to delete | integer