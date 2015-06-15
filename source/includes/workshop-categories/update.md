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

> Success response

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

Parameter | Description | Format
--------- | ----------- | ---------
workshopCategoryId | Workshop category ID to update | String

### Parameters

Parameter | Description | Format
--------- | ----------- | ---------
workshopCategoryType | New workshop category type | String