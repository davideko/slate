## Update Loss Causal

This endpoint used to update a loss causal object. It can update using <code>PUT</code> for full update or <code>PATCH</code> for partial update

> Sample request PUT

```shell
curl "http://localhost:8080/api/loss-causals/1"
  -X PUT
  -H "Authorization: Bearer <token>"
  -H "Content-Type: application/json"
  -d '{
        "lossCausalName":"New Item"
      }'
```

> Sample request PATCH

```shell
curl "http://localhost:8080/api/loss-causals/1"
  -X PATCH
  -H "Authorization: Bearer <token>"
  -H "Content-Type: application/json"
  -d '{
        "lossCausalType":"New Item"
      }'
```

> Success response

```json
{
    "lossCausalType": "New Item",
    "_links": {
        "self": {
            "href": "http://localhost:8080/api/loss-causals/1"
        }
    }
}
```

### HTTP Request

`PUT http://localhost:8080/api/loss-causals/{lossCausalId}`

`PATCH http://localhost:8080/api/loss-causals/{lossCausalId}`

### URL Parameters

Parameter | Description
--------- | -----------
lossCausalId | Selected loss causal id

### Parameters

Parameter | Description | Format 
--------- | ----------- | ------ 
lossCausalType | Fill with loss causal type | String