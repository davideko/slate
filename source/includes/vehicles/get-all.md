# Vehicles
## Get All Vehicles

This endpoint used to return all vehicles

> Sample request

```shell
curl "http://localhost:8080/api/vehicles"
  -H "Authorization: Bearer <token>"
```

> Success response

```json
{
    "_embedded": {
        "vehicles": [
            {
                "plateNumber": "B 1234 ABC",
                "certificateNumber": "A113344556677",
                "engineNumber": "L15A24001878",
                "chassisNumber": "MHRGD38207J700989",
                "yearModel": "2007",
                "vehicleAssembly": {
                    "vehicleAssemblyType": "Domestic"
                },
                "vehicleSerie": {
                    "vehicleSerieType": "CRV"
                },
                "vehicleColor": {
                    "vehicleColorName": "Blue"
                },
                "vehicleId": "937d15ef-2c04-40de-a5e6-3a34d5031345",
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
            },
            {
                "plateNumber": "D 5678 DEF",
                "certificateNumber": "B778899445566",
                "engineNumber": "H89D11547634",
                "chassisNumber": "QWERTY45098D477543",
                "yearModel": "2010",
                "vehicleAssembly": {
                    "vehicleAssemblyType": "Domestic"
                },
                "vehicleSerie": {
                    "vehicleSerieType": "CRV"
                },
                "vehicleColor": {
                    "vehicleColorName": "Blue"
                },
                "vehicleId": "fa6a0d05-b700-47d8-abf9-1e19b250fd71",
                "_links": {
                    "self": {
                        "href": "http://localhost:8080/api/vehicles/fa6a0d05-b700-47d8-abf9-1e19b250fd71{?projection}",
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

`GET http://localhost:8080/api/vehicles`