## Delete Workshop Fee
This endpoint will delete workshop fee by ID.

> Sample request

```shell
  curl "http://localhost:8080/api/workshop-fees/EDFFF909-64AA-4A7B-807E-77A7875F805C"
  -X DELETE
  -H "Authorization: Bearer <token>"
```

> Success response <code>HTTP 204 No Content</code>

### HTTP Request

`DELETE http://localhost:8080/api/workshop-fees/{workshopFeeId}`

### URL Parameters

Parameter | Description | Format
--------- | ----------- | ---------
workshopFeeId | Workshop fee ID to delete | string