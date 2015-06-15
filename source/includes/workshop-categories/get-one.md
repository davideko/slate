## Get a Specific Workshop Category
This endpoint retrieves specific workshop category.

> Sample request

```shell
  curl "http://localhost:8080/api/workshop-categories/1"
  -H "Authorization: Bearer <token>"
```

> Success response

```json
{
  "workshopCategoryType" : "AFFILIATED",
  "_links" : {
    "self" : {
      "href" : "http://localhost:8080/api/workshop-categories/1"
    }
  }
}
```

### HTTP Request

`GET http://localhost:8080/api/workshop-categories/{workshopCategoryId}`

### URL Parameters

Parameter | Description | Format
--------- | ----------- | ---------
workshopCategoryId | Workshop category ID to retrieve | string