## Get a Specific Vehicle Serie

This endpoint get vehicle serie by <code>vehicleSerieId</code>

> Sample request

```shell
curl "http://localhost:8080/api/vehicle-series/1"
  -H "Authorization: Bearer <token>"
```

> Success response

```json
{
    "vehicleSerieType": "CRV",
    "_links": {
        "self": {
            "href": "http://localhost:8080/api/vehicle-series/1{?projection}",
            "templated": true
        },
        "vehicleModel": {
            "href": "http://localhost:8080/api/vehicle-models/1{?projection}",
            "templated": true
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

`GET http://localhost:8080/api/vehicle-series/<vehicleSerieId>`

### URL Parameters

Parameter | Description
--------- | -----------
vehicleSerieId | Selected vehicle serie id
