## Delete a Specific Insured

This endpoint delete insured object by <code>insuredId</code>

> Sample request 

```shell
curl "http://localhost:8080/api/insureds/f1466d54-d6bd-4718-9893-3fdba5bce606"
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

`DELETE http://localhost:8080/api/insureds/<insuredId>`

### URL Parameters

Parameter | Description
--------- | -----------
insuredId | Selected insured id