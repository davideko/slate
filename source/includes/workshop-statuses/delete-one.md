## Delete a Specific Workshop Status
This endpoint delete workshop status object by <code>workshopStatusId</code>

> Sample request 

```shell
curl "http://localhost:8080/api/workshop-statuses/1"
  -X DELETE
  -H "Authorization: Bearer <token>"
```

> Success response <code>HTTP 204 No Content</code>

### HTTP Request

`DELETE http://localhost:8080/api/workshop-statuses/{workshopStatusId}`

### URL Parameters

Parameter | Description
--------- | -----------
workshopStatusId | Selected workshop status id