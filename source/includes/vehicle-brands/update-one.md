## Update Vehicle Brand

This endpoint used to update a vehicle brand object. It can update using <code>PUT</code> for full update or <code>PATCH</code> for partial update

> Sample request PUT

```shell
curl "http://localhost:8080/api/vehicle-brands/1"
  -X PUT
  -H "Authorization: Bearer <token>"
  -H "Content-Type: application/json"
  -d '{
        "vehicleBrandType":"New Honda"
      }'
```

> Sample request PATCH

```shell
curl "http://localhost:8080/api/vehicle-brands/1"
  -X PATCH
  -H "Authorization: Bearer <token>"
  -H "Content-Type: application/json"
  -d '{
        "vehicleBrandType":"New Honda"
      }'
```

> Success response

```json
{
    "vehicleBrandType": "New Honda",
    "_links": {
        "self": {
            "href": "http://localhost:8080/api/vehicle-brands/1"
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

`PUT http://localhost:8080/api/vehicle-brands/<vehicleBrandId>`

`PATCH http://localhost:8080/api/vehicle-brands/<vehicleBrandId>`

### URL Parameters

Parameter | Description
--------- | -----------
vehicleBrandId | Selected vehicle brand id

### Parameters

Parameter | Description | Format 
--------- | ----------- | ------ 
vehicleBrandType | Fill with vehicle brand type | String