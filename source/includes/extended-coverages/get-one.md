## Get a Specific Extended Coverage

This endpoint get extended coverage by <code>extendedCoverageId</code>

> Sample request

```shell
curl http://localhost:8080/api/extended-coverages/1"
  -H "Authorization: Bearer <token>"
```

> Success response

```json
{
    "extendedCoverageType": "Comprehensive",
    "_links": {
        "self": {
            "href": "http://localhost:8080/api/extended-coverages/1"
        }
    }
}
```

### HTTP Request

`GET http://localhost:8080/api/extended-coverages/{extendedCoverageId}`

### URL Parameters

Parameter | Description
--------- | -----------
extendedCoverageId | Selected extended coverage id
