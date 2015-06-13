## Get a Specific Vehicle Color

This endpoint get vehicle color by <code>vehicleColorId</code>

> Sample request

```shell
curl "href": "http://localhost:8080/api/vehicle-colors/1"
  -H "Authorization: Bearer <token>"
```

> Success response

```json
{
    "vehicleColorName": "Blue",
    "_links": {
        "self": {
            "href": "http://localhost:8080/api/vehicle-colors/1"
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

`GET http://localhost:8080/api/vehicle-colors/<vehicleColorId>`

### URL Parameters

Parameter | Description
--------- | -----------
vehicleColorId | Selected vehicle color id