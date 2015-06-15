# Loss Causals
## Get All Loss Causals

This endpoint used to return all loss causals

> Sample request

```shell
curl "http://localhost:8080/api/loss-causals"
  -H "Authorization: Bearer <token>"
```

> Success response

```json
{
    "_embedded": {
        "lossCausals": [
            {
                "lossCausalName": "Item",
                "_links": {
                    "self": {
                        "href": "http://localhost:8080/api/loss-causals/1"
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

`GET http://localhost:8080/api/loss-causals`