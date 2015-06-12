## Delete a Specific Policy

This endpoint delete insured object by <code>policyNumber</code>

> Sample request 

```shell
curl "http://localhost:8080/api/policies/9e78484f-8f79-4124-867c-9f3c079a7522"
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

`DELETE http://localhost:8080/api/policies/<policyNumber>`

### URL Parameters

Parameter | Description
--------- | -----------
policyNumber | Selected policy number