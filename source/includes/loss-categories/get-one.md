## Get a Specific Loss Category

This endpoint get loss category by <code>lossCategoryId</code>

> Sample request

```shell
curl "http://localhost:8080/api/loss-categories/1"
  -H "Authorization: Bearer <token>"
```

> Success response

```json
{
    "lossCategoryName": "Item",
    "_links": {
        "self": {
            "href": "http://localhost:8080/api/loss-categories/1"
        }
    }
}
```

### HTTP Request

`GET http://localhost:8080/api/loss-categories/{lossCategoryId}`

### URL Parameters

Parameter | Description
--------- | -----------
lossCategoryId | Selected loss category id
