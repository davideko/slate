## Update Vehicle Color

This endpoint used to update a vehicle color object. It can update using <code>PUT</code> for full update or <code>PATCH</code> for partial update

> Sample request PUT

```shell
curl "http://localhost:8080/api/vehicle-colors/1"
  -X PUT
  -H "Authorization: Bearer <token>"
  -H "Content-Type: application/json"
  -d '{
        "vehicleColorName":"Red"
      }'
```

> Sample request PATCH

```shell
curl "http://localhost:8080/api/vehicle-colors/1"
  -X PATCH
  -H "Authorization: Bearer <token>"
  -H "Content-Type: application/json"
  -d '{
        "vehicleColorName":"Red"
      }'
```

> Success response

```json
{
    "vehicleColorName": "Red",
    "_links": {
        "self": {
            "href": "http://localhost:8080/api/vehicle-colors/1"
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

`PUT http://localhost:8080/api/vehicle-colors/<vehicleColorId>`

`PATCH http://localhost:8080/api/vehicle-colors/<vehicleColorId>`

### URL Parameters

Parameter | Description
--------- | -----------
vehicleColorId | Selected vehicle color id

### Parameters

Parameter | Description | Format 
--------- | ----------- | ------ 
vehicleColorName | Fill with vehicle color name | String