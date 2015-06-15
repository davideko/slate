## Get a Specific Vehicle

This endpoint get vehicle by <code>vehicleId</code>

> Sample request

```shell
curl "http://localhost:8080/api/vehicles/937d15ef-2c04-40de-a5e6-3a34d5031345"
  -H "Authorization: Bearer <token>"
```

> Success response

```json
{
    "engineNumber": "L15A24001878",
    "chassisNumber": "MHRGD38207J700989",
    "certificateNumber": "A113344556677",
    "plateNumber": "B 1234 ABC",
    "yearModel": "2007",
    "_links": {
        "self": {
            "href": "http://localhost:8080/api/vehicles/937d15ef-2c04-40de-a5e6-3a34d5031345{?projection}",
            "templated": true
        },
        "vehicleAssembly": {
            "href": "http://localhost:8080/api/vehicle-assemblies/1"
        },
        "vehicleColor": {
            "href": "http://localhost:8080/api/vehicle-colors/1"
        },
        "vehicleSerie": {
            "href": "http://localhost:8080/api/vehicle-series/1{?projection}",
            "templated": true
        }
    }
}
```

### HTTP Request

`GET http://localhost:8080/api/vehicles/<vehicleId>`

### URL Parameters

Parameter | Description
--------- | -----------
vehicleId | Selected vehicle id