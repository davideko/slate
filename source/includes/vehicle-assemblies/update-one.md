## Update Vehicle Assembly

This endpoint used to update a vehicle assembly object. It can update using <code>PUT</code> for full update or <code>PATCH</code> for partial update

> Sample request PUT

```shell
curl "http://localhost:8080/api/vehicle-assemblies/1"
  -X PUT
  -H "Authorization: Bearer <token>"
  -H "Content-Type: application/json"
  -d '{
        "vehicleAssemblyType":"Import"
      }'
```

> Sample request PATCH

```shell
curl "http://localhost:8080/api/vehicle-assemblies/1"
  -X PATCH
  -H "Authorization: Bearer <token>"
  -H "Content-Type: application/json"
  -d '{
        "vehicleAssemblyType":"Import"
      }'
```

> Success response

```json
{
    "vehicleAssemblyType": "Import",
    "_links": {
        "self": {
            "href": "http://localhost:8080/api/vehicle-assemblies/1"
        }
    }
}
```

### HTTP Request

`PUT http://localhost:8080/api/vehicle-assemblies/{vehicleAssemblyId}`

`PATCH http://localhost:8080/api/vehicle-assemblies/{vehicleAssemblyId}`

### URL Parameters

Parameter | Description
--------- | -----------
vehicleAssemblyId | Selected vehicle assembly id

### Parameters

Parameter | Description | Format 
--------- | ----------- | ------ 
vehicleAssemblyType | Fill with vehicle assembly type | String