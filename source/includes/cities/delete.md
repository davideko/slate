## Delete City
This endpoint will delete city by ID.

> Sample request

```shell
  curl "http://localhost:8080/api/cities/1"
  -X DELETE
  -H "Authorization: Bearer <token>"
```

### HTTP Request

`DELETE http://localhost:8080/api/cities/{cityId}`

### URL Parameters

Parameter | Description | Data Type
--------- | ----------- | ---------
cityId | City ID to delete | integer