## Delete a Specific Premiums Coverages

This endpoint delete premiums coverages object by composite id

> Sample request 

```shell
curl "http://localhost:8080/api/premiums-coverages/1ffc0022-6e51-43b3-b4b5-649634fd086c@1"
  -X DELETE
  -H "Authorization: Bearer <token>"
```

> Success response

```json
{
  "message":"deleted"
}
```

> Failed response

```json
{
  "error": "because"
}
```

### HTTP Request

`DELETE http://localhost:8080/api/premiums-coverages/<compositeId>`

### URL Parameters

Parameter | Description
--------- | -----------
compositeId | It was composed by premium id + "@" + coverage id