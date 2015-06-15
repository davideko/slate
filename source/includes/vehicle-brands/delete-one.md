## Delete a Specific Vehicle Brand
This endpoint delete vehicle brand object by <code>vehicleBrandId</code>

> Sample request 

```shell
curl "http://localhost:8080/api/vehicle-brands/1"
  -X DELETE
  -H "Authorization: Bearer <token>"
```

> Success response <code>HTTP 204 No Content</code>

### HTTP Request

`DELETE http://localhost:8080/api/vehicle-brands/<vehicleBrandId>`

### URL Parameters

Parameter | Description
--------- | -----------
vehicleBrandId | Selected vehicle brand id