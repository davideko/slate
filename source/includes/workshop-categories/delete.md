## Delete Workshop Category
This endpoint will delete workshop category by ID.

> Sample request

```shell
  curl "http://localhost:8080/api/workshop-categories/4"
  -X DELETE
  -H "Authorization: Bearer <token>"
```

### HTTP Request

`DELETE http://localhost:8080/api/workshop-categories/{workshopCategoryId}`

### URL Parameters

Parameter | Description | Data Type
--------- | ----------- | ---------
workshopCategoryId | Workshop category ID to delete | string