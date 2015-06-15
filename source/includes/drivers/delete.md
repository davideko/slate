## Delete Driver
This endpoint will delete driver by ID.

> Sample request

```shell
  curl "http://localhost:8080/api/drivers/5fc53083-4d3e-4546-97b8-b2cfd23612cc"
  -X DELETE
  -H "Authorization: Bearer <token>"
```

> Success response <code>HTTP 204 No Content</code>

### HTTP Request

`DELETE http://localhost:8080/api/drivers/{driverId}`

### URL Parameters

Parameter | Description | Format
--------- | ----------- | ---------
driverId | Driver ID to delete | String