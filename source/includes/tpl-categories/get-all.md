# TPL Categories

## Get All TPL Category
This endpoint retrieves all TPL Categories.

> Sample request

```shell
  curl "http://localhost:8080/api/tpl-categories"
  -H "Authorization: Bearer <token>"
```

> Sucessful response

```json
{
  "_embedded" : {
    "tplCategories" : [ {
      "tplCategoryType" : "Car",
      "_links" : {
        "self" : {
          "href" : "http://localhost:8080/api/tpl-categories/1"
        }
      }
    }, {
      "tplCategoryType" : "Others",
      "_links" : {
        "self" : {
          "href" : "http://localhost:8080/api/tpl-categories/2"
        }
      }
    } ]
  }
}
```

### HTTP Request

`GET http://localhost:8080/api/tpl-categories`

