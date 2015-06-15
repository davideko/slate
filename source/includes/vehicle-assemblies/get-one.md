## Get a Specific Vehicle Assembly

This endpoint get vehicle assembly by <code>vehicleAssemblyId</code>

> Sample request

```shell
curl "href": "http://localhost:8080/api/vehicle-assemblies/1"
  -H "Authorization: Bearer <token>"
```

> Success response

```json
{
    "vehicleAssemblyType": "Domestic",
    "_links": {
        "self": {
            "href": "http://localhost:8080/api/vehicle-assemblies/1"
        }
    }
}
```

### HTTP Request

`GET http://localhost:8080/api/vehicle-assemblies/{vehicleAssemblyId}`

### URL Parameters

Parameter | Description
--------- | -----------
vehicleAssemblyId | Selected vehicle assembly id
