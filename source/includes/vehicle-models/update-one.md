## Update Vehicle Model

This endpoint used to update a vehicle model object. It can update using <code>PUT</code> for full update or <code>PATCH</code> for partial update

> Sample request PUT

```shell
curl "http://localhost:8080/api/vehicle-models/1"
  -X PUT
  -H "Authorization: Bearer <token>"
  -H "Content-Type: application/json"
  -d '{
        "vehicleModelType":"New Capsule"
      }'
```

> Sample request PATCH

```shell
curl "http://localhost:8080/api/vehicle-models/1"
  -X PATCH
  -H "Authorization: Bearer <token>"
  -H "Content-Type: application/json"
  -d '{
        "vehicleModelType":"New Capsule"
      }'
```

> Success response

```json
{
    "vehicleModelType": "New Capsule",
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

> Failed response

```json
{
  "error": "because"
}
```

### HTTP Request

`PUT http://localhost:8080/api/vehicle-models/<vehicleModelId>`

`PATCH http://localhost:8080/api/vehicle-models/<vehicleModelId>`

### URL Parameters

Parameter | Description
--------- | -----------
vehicleModelId | Selected vehicle model id

### Parameters

Parameter | Description | Format 
--------- | ----------- | ------ 
vehicleModelType | Fill with vehicle model type | String
vehicleBrand | Fill with vehicle brand object url id | String
vehicleCategory | Fill with vehicle category object url id | String