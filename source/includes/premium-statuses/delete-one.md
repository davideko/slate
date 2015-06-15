## Delete a Specific Premium Status
This endpoint delete premium status object by <code>premiumStatusId</code>

> Sample request 

```shell
curl "http://localhost:8080/api/premium-statuses/1"
  -X DELETE
  -H "Authorization: Bearer <token>"
```

> Success response <code>HTTP 204 No Content</code>

### HTTP Request

`DELETE http://localhost:8080/api/premium-statuses/{premiumStatusId}`

### URL Parameters

Parameter | Description
--------- | -----------
premiumStatusId | Selected premium status id