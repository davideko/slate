## Delete Report
This enpdpoint will delete report by report number.

> Sample request

```shell
curl "http://localhost:8080/api/reports/2d451f4e-9547-4691-8193-1eb32dc16e4a"
  -X DELETE
  -H "Authorization: Bearer <token>"
```

### HTTP Request

`DELETE http://localhost:8080/api/reports/{reportNumber}`

### URL Parameters
Parameter | Description | Data Type
--------- | ----------- | ---------
reportNumber| Report number to delete | string