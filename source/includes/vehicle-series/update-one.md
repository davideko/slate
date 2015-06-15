## Update Vehicle Serie

This endpoint used to update a vehicle serie object. It can update using <code>PUT</code> for full update or <code>PATCH</code> for partial update

> Sample request PUT

```shell
curl "http://localhost:8080/api/vehicle-series/1"
  -X PUT
  -H "Authorization: Bearer <token>"
  -H "Content-Type: application/json"
  -d '{
        "vehicleSerieType":"Brilio",
        "vehicleModel":"http://localhost:8080/api/vehicle-models/1"
      }'
```

> Sample request PATCH

```shell
curl "http://localhost:8080/api/vehicle-series/1"
  -X PATCH
  -H "Authorization: Bearer <token>"
  -H "Content-Type: application/json"
  -d '{
        "vehicleSerieType":"Brilio"
      }'
```

> Success response

```json
{
    "vehicleSerieType": "Brilio",
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

> Failed response

```json
{
  "error": "because"
}
```

### HTTP Request

`PUT http://localhost:8080/api/vehicle-series/<vehicleSerieId>`

`PATCH http://localhost:8080/api/vehicle-series/<vehicleSerieId>`

### URL Parameters

Parameter | Description
--------- | -----------
vehicleSerieId | Selected vehicle serie id

### Parameters

Parameter | Description | Format 
--------- | ----------- | ------ 
vehicleSerieType | Fill with vehicle serie type | String
vehicleModel | Fill with vehicle model object url id | String