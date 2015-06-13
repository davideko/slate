## Delete a Specific Vehicle Category
This endpoint delete vehicle category object by <code>vehicleCategoryId</code>

> Sample request 

```shell
curl "http://localhost:8080/api/vehicle-categories/1"
  -X DELETE
  -H "Authorization: Bearer <token>"
```

> Success response

```json
{
  "message":"deleted"
}
```

> Failed response

```json
{
  "error": "because"
}
```

### HTTP Request

`DELETE http://localhost:8080/api/vehicle-categories/<vehicleCategoryId>`

### URL Parameters

Parameter | Description
--------- | -----------
vehicleCategoryId | Selected vehicle category id