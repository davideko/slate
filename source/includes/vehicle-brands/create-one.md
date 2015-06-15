## Add New Vehicle Brand

This endpoint used to add new vehicle brand

> Sample request

```shell
curl "http://localhost:8080/api/vehicle-brands"
  -X POST
  -H "Authorization: Bearer <token>"
  -H "Content-Type: application/json"
  -d '{
        "vehicleBrandType":"Honda"
      }'
```

> Success response

```json
{
    "vehicleBrandType": "Honda",
    "_links": {
        "self": {
            "href": "http://localhost:8080/api/vehicle-brands/1"
        }
    }
}
```

### HTTP Request

`POST http://localhost:8080/api/vehicle-brands`

### Parameters

Parameter | Description | Format 
--------- | ----------- | ------ 
vehicleBrandType | Fill with vehicle brand type | String 