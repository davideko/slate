## Delete City
This endpoint will delete city by ID.

> Sample request

```shell
  curl "http://localhost:8080/api/cities/1"
  -X DELETE
  -H "Authorization: Bearer <token>"
```

> Success response <code>HTTP 204 No Content</code>

### HTTP Request

`DELETE http://localhost:8080/api/cities/{cityId}`

### URL Parameters

Parameter | Description | Format
--------- | ----------- | ---------
cityId | City ID to delete | integer