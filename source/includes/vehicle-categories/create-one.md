## Add New Vehicle Category

This endpoint used to add new vehicle category

> Sample request

```shell
curl "http://localhost:8080/api/vehicle-categories"
  -X POST
  -H "Authorization: Bearer <token>"
  -H "Content-Type: application/json"
  -d '{
        "vehicleCategoryType":"Automatic"
      }'
```

> Success response

```json
{
    "vehicleCategoryType": "Automatic",
    "_links": {
        "self": {
            "href": "http://localhost:8080/api/vehicle-categories/1"
        }
    }
}
```

### HTTP Request

`POST http://localhost:8080/api/vehicle-categories`

### Parameters

Parameter | Description | Format 
--------- | ----------- | ------ 
vehicleCategoryType | Fill with vehicle category type | String 