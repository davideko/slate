## Update TPL Category
This endpoint will update TPL category by ID.

> Sample request PUT

```shell
  curl "http://localhost:8080/api/tpl-categories/1"
  -X PUT
  -H "Authorization: Bearer <token>"
  -d '{
    'tplCategoryType' : "Bike"
  }'
```

> Sample request PATCH

```shell
  curl "http://localhost:8080/api/tpl-categories/1"
  -X PATCH
  -H "Authorization: Bearer <token>"
  -d '{
    'tplCategoryType' : "Bike"
  }'
```

> Success response

```json
{
  "tplCategoryType" : "Bike",
  "_links" : {
    "self" : {
      "href" : "http://localhost:8080/api/tpl-categories/1"
    }
  }
}
```

### HTTP Request

`PUT http://localhost:8080/api/tpl-categories/{tplCategoryId}`

`PATCH http://localhost:8080/api/tpl-categories/{tplCategoryId}`

### URL Parameters

Parameter | Description | Format
--------- | ----------- | ---------
tplCategoryId | TPL category ID to update | integer

### Parameters

Parameter | Description | Format
--------- | ----------- | ---------
tplCategoryType | New TPL category type | String