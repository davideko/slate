## Delete a Specific Cs Status
This endpoint delete cs status object by <code>csStatusId</code>

> Sample request 

```shell
curl "http://localhost:8080/api/cs-statuses/1"
  -X DELETE
  -H "Authorization: Bearer <token>"
```

> Success response <code>HTTP 204 No Content</code>

### HTTP Request

`DELETE http://localhost:8080/api/cs-statuses/{csStatusId}`

### URL Parameters

Parameter | Description
--------- | -----------
csStatusId | Selected cs status id