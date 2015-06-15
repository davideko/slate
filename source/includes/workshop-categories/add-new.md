## Add New Workshop Category
This endpoint will create new workshop category.

> Sample request

```shell
  curl "http://localhost:8080/api/workshop-categories"
  -X POST
  -H "Authorization: Bearer <token>"
  -d '{
    "workshopCategoryType" : "Langganan"
  }'
```

> Sucessful response

```json
{
  "workshopCategoryType" : "Langganan",
  "_links" : {
    "self" : {
      "href" : "http://localhost:8080/api/workshop-categories/4"
    }
  }
}
```

### HTTP Request

`POST http://localhost:8080/api/workshop-categories/`

###  Parameters

Parameter | Description | Data Type
--------- | ----------- | ---------
workshopCategoryType | New workshop category type | string