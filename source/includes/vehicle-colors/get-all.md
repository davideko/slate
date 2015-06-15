# Vehicle Colors
## Get All Vehicle Colors

This endpoint used to return all vehicle colors

> Sample request

```shell
curl "http://localhost:8080/api/vehicle-colors"
  -H "Authorization: Bearer <token>"
```

> Success response

```json
{
    "_embedded": {
        "vehicleColors": [
            {
                "vehicleColorName": "Blue",
                "_links": {
                    "self": {
                        "href": "http://localhost:8080/api/vehicle-colors/1"
                    }
                }
            }
        ]
    }
}
```

### HTTP Request 

`GET http://localhost:8080/api/vehicle-colors`