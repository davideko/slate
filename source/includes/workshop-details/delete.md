## Delete Workshop Detail
This endpoint will delete workshop detail by ID.

> Sample request

```shell
  curl "http://localhost:8080/api/workshop-details/4CFEADB9-EAF8-48A7-808A-0CF141A8B99D"
  -X DELETE
  -H "Authorization: Bearer <token>"
```

> Success response <code>HTTP 204 No Content</code>

### HTTP Request

`DELETE http://localhost:8080/api/workshop-details/{workshopDetailId}`

### URL Parameters

Parameter | Description | Format
--------- | ----------- | ---------
workshopDetailId | Workshop detail ID to delete | string