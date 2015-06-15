## Add New Loss Causal

This endpoint used to add new loss causal

> Sample request

```shell
curl "http://localhost:8080/api/loss-causals"
  -X POST
  -H "Authorization: Bearer <token>"
  -H "Content-Type: application/json"
  -d '{
        "lossCausalName":"Item"
      }'
```

> Success response

```json
{
    "lossCausalName": "Item",
    "_links": {
        "self": {
            "href": "http://localhost:8080/api/loss-causals/1"
        }
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

`POST http://localhost:8080/api/loss-causals`

### Parameters

Parameter | Description | Format 
--------- | ----------- | ------ 
lossCausalName | Fill with loss causal name | String 