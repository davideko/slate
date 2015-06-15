## Delete a Specific Vehicle Category
This endpoint delete vehicle category object by <code>vehicleCategoryId</code>

> Sample request 

```shell
curl "http://localhost:8080/api/vehicle-categories/1"
  -X DELETE
  -H "Authorization: Bearer <token>"
```

> Success response <code>HTTP 204 No Content</code>

### HTTP Request

`DELETE http://localhost:8080/api/vehicle-categories/{vehicleCategoryId}`

### URL Parameters

Parameter | Description
--------- | -----------
vehicleCategoryId | Selected vehicle category id