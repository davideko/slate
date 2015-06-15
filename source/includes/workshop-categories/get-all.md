# Workshop Categories

## Get All Worskhop Categories
This endpoint retrieves all workshop categories.

> Sample request

```shell
  curl "http://localhost:8080/api/workshop-categories"
  -H "Authorization: Bearer <token>"
```

> Sucessful response

```json
{
  "_embedded" : {
    "workshopCategories" : [ {
      "workshopCategoryType" : "AFFILIATED",
      "_links" : {
        "self" : {
          "href" : "http://localhost:8080/api/workshop-categories/1"
        }
      }
    }, {
      "workshopCategoryType" : "NON AFFILIATED",
      "_links" : {
        "self" : {
          "href" : "http://localhost:8080/api/workshop-categories/2"
        }
      }
    } ]
  }
}
```

### HTTP Request

`GET http://localhost:8080/api/workshop-categories`

