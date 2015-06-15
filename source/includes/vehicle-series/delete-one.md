## Delete a Specific Vehicle Serie
This endpoint delete vehicle serie object by <code>vehicleSerieId</code>

> Sample request 

```shell
curl "http://localhost:8080/api/vehicle-series/1"
  -X DELETE
  -H "Authorization: Bearer <token>"
```

> Success response <code>HTTP 204 No Content</code>

### HTTP Request

`DELETE http://localhost:8080/api/vehicle-series/<vehicleSerieId>`

### URL Parameters

Parameter | Description
--------- | -----------
vehicleSerieId | Selected vehicle serie id