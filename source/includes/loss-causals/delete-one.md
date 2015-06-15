## Delete a Specific Loss Causal
This endpoint delete loss causal object by <code>lossCausalId</code>

> Sample request 

```shell
curl "http://localhost:8080/api/loss-causals/1"
  -X DELETE
  -H "Authorization: Bearer <token>"
```

> Success response <code>HTTP 204 No Content</code>

### HTTP Request

`DELETE http://localhost:8080/api/loss-causals/<lossCausalId>`

### URL Parameters

Parameter | Description
--------- | -----------
lossCausalId | Selected loss causal id