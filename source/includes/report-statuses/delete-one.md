## Delete a Specific Report Status
This endpoint delete report status object by <code>reportStatusId</code>

> Sample request 

```shell
curl "http://localhost:8080/api/report-statuses/1"
  -X DELETE
  -H "Authorization: Bearer <token>"
```

> Success response <code>HTTP 204 No Content</code>

### HTTP Request

`DELETE http://localhost:8080/api/report-statuses/{reportStatusId}`

### URL Parameters

Parameter | Description
--------- | -----------
reportStatusId | Selected report status id