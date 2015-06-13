## Delete a Specific Vehicle Assembly
This endpoint delete vehicle assembly object by <code>vehicleAssemblyId</code>

> Sample request 

```shell
curl "http://localhost:8080/api/vehicle-assemblies/1"
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

`DELETE http://localhost:8080/api/vehicle-assemblies/<vehicleAssemblyId>`

### URL Parameters

Parameter | Description
--------- | -----------
vehicleAssemblyId | Selected vehicle assembly id