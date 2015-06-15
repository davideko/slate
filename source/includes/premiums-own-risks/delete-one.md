## Delete a Specific Premiums Own risks

This endpoint delete premiums own risks object by composite id

> Sample request 

```shell
curl "http://localhost:8080/api/premiums-own-risks/1ffc0022-6e51-43b3-b4b5-649634fd086c@1"
  -X DELETE
  -H "Authorization: Bearer <token>"
```

> Success response <code>HTTP 204 No Content</code>

### HTTP Request

`DELETE http://localhost:8080/api/premiums-own-risks/<compositeId>`

### URL Parameters

Parameter | Description
--------- | -----------
compositeId | It was composed by premium id + "@" + own risk id