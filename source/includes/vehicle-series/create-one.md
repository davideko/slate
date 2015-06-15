## Add New Vehicle Serie

This endpoint used to add new vehicle serie

> Sample request

```shell
curl "http://localhost:8080/api/vehicle-series"
  -X POST
  -H "Authorization: Bearer <token>"
  -H "Content-Type: application/json"
  -d '{
        "vehicleSerieType":"Honda",
        "vehicleModel":"http://localhost:8080/api/vehicle-models/1"
      }'
```

> Success response

```json
{
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
}
```

### HTTP Request

`POST http://localhost:8080/api/vehicle-series`

### Parameters

Parameter | Description | Format 
--------- | ----------- | ------ 
vehicleSerieType | Fill with vehicle serie type | String 
vehicleModel | Fill with vehicle model object url id | String