# Vehicle Brands
## Get All Vehicle Brands

This endpoint used to return all vehicle brands

> Sample request

```shell
curl "http://localhost:8080/api/vehicle-brands"
  -H "Authorization: Bearer <token>"
```

> Success response

```json
{
    "_embedded": {
        "vehicleBrands": [
            {
                "vehicleBrandType": "Honda",
                "_links": {
                    "self": {
                        "href": "http://localhost:8080/api/vehicle-brands/1"
                    }
                }
            },
            {
                "vehicleBrandType": "Daihatsu",
                "_links": {
                    "self": {
                        "href": "http://localhost:8080/api/vehicle-brands/2"
                    }
                }
            }
        ]
    }
}
```

### HTTP Request 

`GET http://localhost:8080/api/vehicle-brands`