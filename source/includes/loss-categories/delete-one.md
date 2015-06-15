## Delete a Specific Loss Category
This endpoint delete loss category object by <code>lossCategoryId</code>

> Sample request 

```shell
curl "http://localhost:8080/api/loss-categories/1"
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

`DELETE http://localhost:8080/api/loss-categories/<lossCategoryId>`

### URL Parameters

Parameter | Description
--------- | -----------
lossCategoryId | Selected loss category id