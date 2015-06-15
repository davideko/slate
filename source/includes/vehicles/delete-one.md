## Delete a Specific Vehicle

This endpoint delete vehicle object by <code>vehicleId</code>

> Sample request 

```shell
curl "http://localhost:8080/api/vehicles/fa6a0d05-b700-47d8-abf9-1e19b250fd71"
  -X DELETE
  -H "Authorization: Bearer <token>"
```

> Success response <code>HTTP 204 No Content</code>

### HTTP Request

`DELETE http://localhost:8080/api/vehicles/<vehicleId>`

### URL Parameters

Parameter | Description
--------- | -----------
vehicleId | Selected vehicle id