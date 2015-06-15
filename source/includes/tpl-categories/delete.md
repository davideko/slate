## Delete TPL Category
This endpoint will delete TPL category by ID.

> Sample request

```shell
  curl "http://localhost:8080/api/tpl-categories/1"
  -X DELETE
  -H "Authorization: Bearer <token>"
```

### HTTP Request

`DELETE http://localhost:8080/api/tpl-categories/{tplCategoryId}`

### URL Parameters

Parameter | Description | Data Type
--------- | ----------- | ---------
tplCategoryId | TPL category ID to delete | integer