## Add New Vehicle Model

This endpoint used to add new vehicle model

> Sample request

```shell
curl "http://localhost:8080/api/vehicle-models"
  -X POST
  -H "Authorization: Bearer <token>"
  -H "Content-Type: application/json"
  -d '{
        "vehicleModelType":"Honda",
        "vehicleBrand":"http://localhost:8080/api/vehicle-brands/1",
        "vehicleCategory":"http://localhost:8080/api/vehicle-categories/1"
      }'
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

`POST http://localhost:8080/api/vehicle-models`

### Parameters

Parameter | Description | Format 
--------- | ----------- | ------ 
vehicleModelType | Fill with vehicle model type | String
vehicleBrand | Fill with vehicle brand object url id | String
vehicleCategory | Fill with vehicle category object url id | String