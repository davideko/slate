## Update Loss Category

This endpoint used to update a loss category object. It can update using <code>PUT</code> for full update or <code>PATCH</code> for partial update

> Sample request PUT

```shell
curl "http://localhost:8080/api/loss-categories/1"
  -X PUT
  -H "Authorization: Bearer <token>"
  -H "Content-Type: application/json"
  -d '{
        "lossCategoryName":"New Item"
      }'
```

> Sample request PATCH

```shell
curl "http://localhost:8080/api/loss-categories/1"
  -X PATCH
  -H "Authorization: Bearer <token>"
  -H "Content-Type: application/json"
  -d '{
        "lossCategoryName":"New Item"
      }'
```

> Success response

```json
{
    "lossCategoryName": "New Item",
    "_links": {
        "self": {
            "href": "http://localhost:8080/api/loss-categories/1"
        }
    }
}
```

### HTTP Request

`PUT http://localhost:8080/api/loss-categories/{lossCategoryId}`

`PATCH http://localhost:8080/api/loss-categories/{lossCategoryId}`

### URL Parameters

Parameter | Description
--------- | -----------
lossCategoryId | Selected loss category id

### Parameters

Parameter | Description | Format 
--------- | ----------- | ------ 
lossCategoryName | Fill with loss category name | String