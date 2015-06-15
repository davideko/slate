## Delete a Specific Loss Category
This endpoint delete loss category object by <code>lossCategoryId</code>

> Sample request 

```shell
curl "http://localhost:8080/api/loss-categories/1"
  -X DELETE
  -H "Authorization: Bearer <token>"
```

> Success response <code> HTTP 204 No Content</code>

### HTTP Request

`DELETE http://localhost:8080/api/loss-categories/<lossCategoryId>`

### URL Parameters

Parameter | Description
--------- | -----------
lossCategoryId | Selected loss category id