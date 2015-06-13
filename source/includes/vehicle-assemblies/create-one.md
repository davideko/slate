## Add New Vehicle Assembly

This endpoint used to add new vehicle assembly

> Sample request

```shell
curl "http://localhost:8080/api/vehicle-assemblies"
  -X POST
  -H "Authorization: Bearer <token>"
  -H "Content-Type: application/json"
  -d '{
        "vehicleAssemblyType":"Domestic"
      }'
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

> Failed response

```json
{
  "error": "because"
}
```

### HTTP Request

`POST http://localhost:8080/api/vehicle-assemblies`

### Parameters

Parameter | Description | Format 
--------- | ----------- | ------ 
vehicleAssemblyType | Fill with vehicle assembly type | String 