# Vehicle Assemblies
## Get All Vehicle Assemblies

This endpoint used to return all vehicle assemblies

> Sample request

```shell
curl "http://localhost:8080/api/vehicle-assemblies"
  -H "Authorization: Bearer <token>"
```

> Success response

```json
{
    "_embedded": {
        "vehicleAssemblies": [
            {
                "vehicleAssemblyType": "Domestic",
                "_links": {
                    "self": {
                        "href": "http://localhost:8080/api/vehicle-assemblies/1"
                    }
                }
            }
        ]
    }
}
```

> Failed response

```json
{
  "error": "because"
}
```

### HTTP Request 

`GET http://localhost:8080/api/vehicle-assemblies`