## Get a Specific Loss Causal

This endpoint get loss causal by <code>lossCausalId</code>

> Sample request

```shell
curl "http://localhost:8080/api/loss-causals/1"
  -H "Authorization: Bearer <token>"
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

`GET http://localhost:8080/api/loss-causals/<lossCausalId>`

### URL Parameters

Parameter | Description
--------- | -----------
lossCausalId | Selected loss causal id
