## Delete a Specific Premium

This endpoint delete premium object by <code>premiumId</code>

> Sample request 

```shell
curl "http://localhost:8080/api/premiums/1ffc0022-6e51-43b3-b4b5-649634fd086c"
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

`DELETE http://localhost:8080/api/premiums/<premiumId>`

### URL Parameters

Parameter | Description
--------- | -----------
premiumId | Selected premium id