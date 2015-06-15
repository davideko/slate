## Delete TIN
This endpoint will delete TIN by ID.

> Sample request

```shell
  curl "http://localhost:8080/api/tins/01.342.006.2-046.000"
  -X DELETE
  -H "Authorization: Bearer <token>"
```

### HTTP Request

`DELETE http://localhost:8080/api/tins/{taxIdentificationNumber}`

### URL Parameters

Parameter | Description | Data Type
--------- | ----------- | ---------
taxIdentificationNumber | Tax identification number to delete | string