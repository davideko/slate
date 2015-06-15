## Get a Specific Vehicle Brand

This endpoint get vehicle brand by <code>vehicleBrandId</code>

> Sample request

```shell
curl "http://localhost:8080/api/vehicle-brands/1"
  -H "Authorization: Bearer <token>"
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

> Failed response

```json
{
  "error": "because"
}
```

### HTTP Request

`GET http://localhost:8080/api/vehicle-brands/<vehicleBrandId>`

### URL Parameters

Parameter | Description
--------- | -----------
vehicleBrandId | Selected vehicle brand id
