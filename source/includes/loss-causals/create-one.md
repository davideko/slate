## Add New Loss Causal

This endpoint used to add new loss causal

> Sample request

```shell
curl "http://localhost:8080/api/loss-causals"
  -X POST
  -H "Authorization: Bearer <token>"
  -H "Content-Type: application/json"
  -d '{
        "lossCausalType":"Item"
      }'
```

> Success response

```json
{
    "lossCausalType": "Item",
    "_links": {
        "self": {
            "href": "http://localhost:8080/api/loss-causals/1"
        }
    }
}
```

### HTTP Request

`POST http://localhost:8080/api/loss-causals`

### Parameters

Parameter | Description | Format 
--------- | ----------- | ------ 
lossCausalType | Fill with loss causal type | String 