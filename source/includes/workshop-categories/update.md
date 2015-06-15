## Update Workshop Category
This endpoint will update workshop category by ID.

> Sample request PUT

```shell
  curl "http://localhost:8080/api/workshop-categories/4"
  -X PUT
  -H "Authorization: Bearer <token>"
  -d '{
    "workshopCategoryType" : "Rekanan"
  }'
```

> Sample request PATCH

```shell
  curl "http://localhost:8080/api/workshops-categories4"
  -X PATCH
  -H "Authorization: Bearer <token>"
  -d '{
    "workshopCategoryType" : "rekanan"
  }'
```

> Sucessful response

```json
{
  "workshopCategoryType" : "Rekanan",
  "_links" : {
    "self" : {
      "href" : "http://localhost:8080/api/workshop-categories/4"
    }
  }
}
```

### HTTP Request

`PUT http://localhost:8080/api/workshop-categories/{workshopCategoryId}`

`PATCH http://localhost:8080/api/workshop-categories/{workshopCategoryId}`

### URL Parameters

Parameter | Description | Data Type
--------- | ----------- | ---------
workshopCategoryId | Workshop category ID to update | string

### Parameters

Parameter | Description | Data Type
--------- | ----------- | ---------
workshopCategoryType | New workshop category type | string