
## Get a Specific TPL Category
This endpoint retrieves specific TPL Category.

> Sample request

```shell
  curl "http://localhost:8080/api/tpl-categories/1"
  -H "Authorization: Bearer <token>"
```

> Sucessful response

```json
{
  "tplCategoryType" : "Car",
  "_links" : {
    "self" : {
      "href" : "http://localhost:8080/api/tpl-categories/1"
    }
  }
}
```

### HTTP Request

`GET http://localhost:8080/api/tpl-categories/{tplCategoryId}`

### URL Parameters

Parameter | Description | Data Type
--------- | ----------- | ---------
tplCategoryId | TPL category to retrieve | integer