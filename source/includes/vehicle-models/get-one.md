## Get a Specific Vehicle Model

This endpoint get vehicle model by <code>vehicleModelId</code>

> Sample request

```shell
curl "http://localhost:8080/api/vehicle-models/1"
  -H "Authorization: Bearer <token>"
```

> Success response

```json
{
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
}
```

### HTTP Request

`GET http://localhost:8080/api/vehicle-models/<vehicleModelId>`

### URL Parameters

Parameter | Description
--------- | -----------
vehicleModelId | Selected vehicle model id
