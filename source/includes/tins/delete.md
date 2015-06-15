## Delete TIN
This endpoint will delete TIN by ID.

> Sample request

```shell
  curl "http://localhost:8080/api/tins/01.342.006.2-046.000"
  -X DELETE
  -H "Authorization: Bearer <token>"
```

> Success response <code>HTTP 204 No Content</code>

### HTTP Request

`DELETE http://localhost:8080/api/tins/{taxIdentificationNumber}`

### URL Parameters

Parameter | Description | Format
--------- | ----------- | ---------
taxIdentificationNumber | Tax identification number to delete | string