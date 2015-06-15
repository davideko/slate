## Add New Loss Category

This endpoint used to add new loss category

> Sample request

```shell
curl "http://localhost:8080/api/loss-categories"
  -X POST
  -H "Authorization: Bearer <token>"
  -H "Content-Type: application/json"
  -d '{
        "lossCategoryName":"Item"
      }'
```

> Success response

```json
{
    "lossCategoryName": "Item",
    "_links": {
        "self": {
            "href": "http://localhost:8080/api/loss-categories/1"
        }
    }
}
```

### HTTP Request

`POST http://localhost:8080/api/loss-categories`

### Parameters

Parameter | Description | Format 
--------- | ----------- | ------ 
lossCategoryName | Fill with loss category name | String 