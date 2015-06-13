## Get a Specific Coverages

This endpoint get coverages by <code>coverageId</code>

> Sample request

```shell
curl "href": "http://localhost:8080/api/coverages/1"
  -H "Authorization: Bearer <token>"
```

> Success response

```json
{
    "coverageType": "CASCO",
    "_links": {
        "self": {
            "href": "http://localhost:8080/api/coverages/1"
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

`GET http://localhost:8080/api/coverages/<coverageId>`

### URL Parameters

Parameter | Description
--------- | -----------
coverageId | Selected coverages id
