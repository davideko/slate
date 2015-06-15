# Vehicle Models
## Get All Vehicle Models

This endpoint used to return all vehicle models

> Sample request

```shell
curl "http://localhost:8080/api/vehicle-models"
  -H "Authorization: Bearer <token>"
```

> Success response

```json
{
    "_embedded": {
        "vehicleModels": [
            {
                "vehicleModelId": 1,
                "vehicleBrand": {
                    "vehicleBrandType": "Honda"
                },
                "vehicleCategory": {
                    "vehicleCategoryType": "Automatic"
                },
                "vehicleModelType": "Capsule",
                "_links": {
                    "self": {
                        "href": "http://localhost:8080/api/vehicle-models/1{?projection}",
                        "templated": true
                    },
                    "vehicleBrand": {
                        "href": "http://localhost:8080/api/vehicle-brands/1"
                    },
                    "vehicleCategory": {
                        "href": "http://localhost:8080/api/vehicle-categories/1"
                    }
                }
            },
            {
                "vehicleModelId": 2,
                "vehicleBrand": {
                    "vehicleBrandType": "Honda"
                },
                "vehicleCategory": {
                    "vehicleCategoryType": "Automatic"
                },
                "vehicleModelType": "Sedan",
                "_links": {
                    "self": {
                        "href": "http://localhost:8080/api/vehicle-models/2{?projection}",
                        "templated": true
                    },
                    "vehicleBrand": {
                        "href": "http://localhost:8080/api/vehicle-brands/1"
                    },
                    "vehicleCategory": {
                        "href": "http://localhost:8080/api/vehicle-categories/1"
                    }
                }
            }
        ]
    }
}
```

### HTTP Request 

`GET http://localhost:8080/api/vehicle-models`