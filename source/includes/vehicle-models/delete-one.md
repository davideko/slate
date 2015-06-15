## Delete a Specific Vehicle Model
This endpoint delete vehicle model object by <code>vehicleModelId</code>

> Sample request 

```shell
curl "http://localhost:8080/api/vehicle-models/1"
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

`DELETE http://localhost:8080/api/vehicle-models/<vehicleModelId>`

### URL Parameters

Parameter | Description
--------- | -----------
vehicleModelId | Selected vehicle model id