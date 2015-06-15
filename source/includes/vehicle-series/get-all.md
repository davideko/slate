# Vehicle Series
## Get All Vehicle Series

This endpoint used to return all vehicle series

> Sample request

```shell
curl "http://localhost:8080/api/vehicle-series"
  -H "Authorization: Bearer <token>"
```

> Success response

```json
{
    "_embedded": {
        "vehicleSeries": [
            {
                "vehicleModel": {
                    "vehicleModelType": "Capsule"
                },
                "vehicleSerieId": 1,
                "vehicleSerieType": "CRV",
                "_links": {
                    "self": {
                        "href": "http://localhost:8080/api/vehicle-series/1{?projection}",
                        "templated": true
                    },
                    "vehicleModel": {
                        "href": "http://localhost:8080/api/vehicle-models/1{?projection}",
                        "templated": true
                    }
                }
            },
            {
                "vehicleModel": {
                    "vehicleModelType": "Sedan"
                },
                "vehicleSerieId": 2,
                "vehicleSerieType": "Jazz",
                "_links": {
                    "self": {
                        "href": "http://localhost:8080/api/vehicle-series/2{?projection}",
                        "templated": true
                    },
                    "vehicleModel": {
                        "href": "http://localhost:8080/api/vehicle-models/1{?projection}",
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

`GET http://localhost:8080/api/vehicle-series`