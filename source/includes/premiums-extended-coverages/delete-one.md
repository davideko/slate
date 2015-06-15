## Delete a Specific Premiums Extended Coverages

This endpoint delete premiums extended coverages object by composite id

> Sample request 

```shell
curl "http://localhost:8080/api/premiums-extended-coverages/1ffc0022-6e51-43b3-b4b5-649634fd086c@1"
  -X DELETE
  -H "Authorization: Bearer <token>"
```

> Success response <code>HTTP 204 No Content</code>

### HTTP Request

`DELETE http://localhost:8080/api/premiums-extended-coverages/{compositeId}`

### URL Parameters

Parameter | Description
--------- | -----------
compositeId | It was composed by premium id + "@" + extended coverage id