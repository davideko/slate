## Add New TPL Category
This endpoint will create new TPL category.

> Sample request

```shell
  curl "http://localhost:8080/api/tpl-categories"
  -X POST
  -H "Authorization: Bearer <token>"
  -d '{
    "tplCategoryType" : "Bike"
  }'
```

> Sucessful response

```json
{
  "tplCategoryType" : "Bike",
  "_links" : {
    "self" : {
      "href" : "http://localhost:8080/api/tpl-categories/5"
    }
  }
}
```

### HTTP Request

`POST http://localhost:8080/api/tpl-categories`

###  Parameters

Parameter | Description | Data Type
--------- | ----------- | ---------
tplCategoryType | New TPL category type | string
