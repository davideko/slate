## Delete a Specific coverage
This endpoint delete coverage object by <code>coverageId</code>

> Sample request 

```shell
curl "http://localhost:8080/api/coverages/1"
  -X DELETE
  -H "Authorization: Bearer <token>"
```

> Success response <code>HTTP 204 No Content</code>

### HTTP Request

`DELETE http://localhost:8080/api/coverages/{coverageId}`

### URL Parameters

Parameter | Description
--------- | -----------
coverageId | Selected coverage id