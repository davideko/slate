## Get a Specific Vehicle Category

This endpoint get vehicle category by <code>vehicleCategoryId</code>

> Sample request

```shell
curl "http://localhost:8080/api/vehicle-categories/1"
  -H "Authorization: Bearer <token>"
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

`GET http://localhost:8080/api/vehicle-categories/{vehicleCategoryId}`

### URL Parameters

Parameter | Description
--------- | -----------
vehicleCategoryId | Selected vehicle category id
