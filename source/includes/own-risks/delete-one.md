## Delete a Specific Own Risk
This endpoint delete own risk object by <code>ownRiskId</code>

> Sample request 

```shell
curl "http://localhost:8080/api/own-risks/1"
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

`DELETE http://localhost:8080/api/own-risks/<ownRiskId>`

### URL Parameters

Parameter | Description
--------- | -----------
ownRiskId | Selected own risk id