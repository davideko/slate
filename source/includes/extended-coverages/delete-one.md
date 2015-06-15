## Delete a Specific Extended Coverage
This endpoint delete extended coverage object by <code>extendedCoverageId</code>

> Sample request 

```shell
curl "http://localhost:8080/api/extended-coverages/1"
  -X DELETE
  -H "Authorization: Bearer <token>"
```

> Success response <code>HTTP 204 No Content</code>

### HTTP Request

`DELETE http://localhost:8080/api/extended-coverages/{extendedCoverageId}`

### URL Parameters

Parameter | Description
--------- | -----------
extendedCoverageId | Selected extended coverage id