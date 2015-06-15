## Delete a Specific Accident
This endpoint delete accident object by <code>accidentId</code>

> Sample request 

```shell
curl "http://localhost:8080/api/accidents/3f016e51-07db-42ea-b20b-822b0a6eecdb"
  -X DELETE
  -H "Authorization: Bearer <token>"
```

> Success response <code>HTTP 204 No Content</code>

### HTTP Request

`DELETE http://localhost:8080/api/accidents/{accidentId}`

### URL Parameters

Parameter | Description
--------- | -----------
accidentId | Selected accident id