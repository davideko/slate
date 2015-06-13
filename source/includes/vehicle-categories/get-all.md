# Vehicle Categories
## Get All Vehicle Categories

This endpoint used to return all vehicle categories

> Sample request

```shell
curl "http://localhost:8080/api/vehicle-categories"
  -H "Authorization: Bearer <token>"
```

> Success response

```json
{
    "_embedded": {
        "vehicleCategories": [
            {
                "vehicleCategoryType": "Automatic",
                "_links": {
                    "self": {
                        "href": "http://localhost:8080/api/vehicle-categories/1"
                    }
                }
            },
            {
                "vehicleCategoryType": "Manual",
                "_links": {
                    "self": {
                        "href": "http://localhost:8080/api/vehicle-categories/2"
                    }
                }
            }
        ]
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

`GET http://localhost:8080/api/vehicle-categories`