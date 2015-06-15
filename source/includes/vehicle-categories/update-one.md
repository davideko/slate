## Update Vehicle Category

This endpoint used to update a vehicle category object. It can update using <code>PUT</code> for full update or <code>PATCH</code> for partial update

> Sample request PUT

```shell
curl "http://localhost:8080/api/vehicle-categories/1"
  -X PUT
  -H "Authorization: Bearer <token>"
  -H "Content-Type: application/json"
  -d '{
        "vehicleCategoryType":"Semi Automatic"
      }'
```

> Sample request PATCH

```shell
curl "http://localhost:8080/api/vehicle-categories/1"
  -X PATCH
  -H "Authorization: Bearer <token>"
  -H "Content-Type: application/json"
  -d '{
        "vehicleCategoryType":"Semi Automatic"
      }'
```

> Success response

```json
{
    "vehicleCategoryType": "Semi Automatic",
    "_links": {
        "self": {
            "href": "http://localhost:8080/api/vehicle-categories/1"
        }
    }
}
```

### HTTP Request

`PUT http://localhost:8080/api/vehicle-categories/{vehicleCategoryId}`

`PATCH http://localhost:8080/api/vehicle-categories/{vehicleCategoryId}`

### URL Parameters

Parameter | Description
--------- | -----------
vehicleCategoryId | Selected vehicle category id

### Parameters

Parameter | Description | Format 
--------- | ----------- | ------ 
vehicleCategoryType | Fill with vehicle category type | String