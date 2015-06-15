# Loss Categories
## Get All Loss Categories

This endpoint used to return all loss categories

> Sample request

```shell
curl "http://localhost:8080/api/loss-categories"
  -H "Authorization: Bearer <token>"
```

> Success response

```json
{
    "_embedded": {
        "lossCategories": [
            {
                "lossCategoryName": "Item",
                "_links": {
                    "self": {
                        "href": "http://localhost:8080/api/loss-categories/1"
                    }
                }
            }
        ]
    }
}
```

> Failed response

```json
{
  "error": "because"
}
```

### HTTP Request 

`GET http://localhost:8080/api/loss-categories`