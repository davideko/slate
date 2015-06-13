## Add New Vehicle Color

This endpoint used to add new vehicle color

> Sample request

```shell
curl "http://localhost:8080/api/vehicle-colors"
  -X POST
  -H "Authorization: Bearer <token>"
  -H "Content-Type: application/json"
  -d '{
        "vehicleColorName":"Blue"
      }'
```

> Success response

```json
{
    "vehicleColorName": "Blue",
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

`POST http://localhost:8080/api/vehicle-colors`

### Parameters

Parameter | Description | Format 
--------- | ----------- | ------ 
vehicleColorName | Fill with vehicle color name | String 