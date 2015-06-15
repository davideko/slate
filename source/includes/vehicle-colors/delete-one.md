## Delete a Specific Vehicle Color
This endpoint delete vehicle color object by <code>vehicleColorId</code>

> Sample request 

```shell
curl "http://localhost:8080/api/vehicle-colors/1"
  -X DELETE
  -H "Authorization: Bearer <token>"
```

> Success response <code>HTTP 204 No Content</code>

### HTTP Request

`DELETE http://localhost:8080/api/vehicle-colors/{vehicleColorId}`

### URL Parameters

Parameter | Description
--------- | -----------
vehicleColorId | Selected vehicle color id