## Delete Bank
This endpoint will delete bank by ID.

> Sample request

```shell
  curl "http://localhost:8080/api/banks/1"
  -X DELETE
  -H "Authorization: Bearer <token>"
```

### HTTP Request

`DELETE http://localhost:8080/api/banks/{bankId}`

### URL Parameters

Parameter | Description | Data Type
--------- | ----------- | ---------
bankId | Bank ID to delete | integer