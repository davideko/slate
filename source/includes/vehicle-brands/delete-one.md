## Delete a Specific Vehicle Brand
This endpoint delete vehicle brand object by <code>vehicleBrandId</code>

> Sample request 

```shell
curl "http://localhost:8080/api/vehicle-brands/1"
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

`DELETE http://localhost:8080/api/vehicle-brands/<vehicleBrandId>`

### URL Parameters

Parameter | Description
--------- | -----------
vehicleBrandId | Selected vehicle brand id