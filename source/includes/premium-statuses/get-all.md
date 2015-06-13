# Premium Statuses
## Get All Premium Statuses

This endpoint used to return all premium statuses

> Sample request

```shell
curl "http://localhost:8080/api/premium-statuses"
  -H "Authorization: Bearer <token>"
```

> Success response

```json
{
    "_embedded": {
        "premiumStatuses": [
            {
                "premiumStatusType": "Active",
                "_links": {
                    "self": {
                        "href": "http://localhost:8080/api/premium-statuses/1"
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

`GET http://localhost:8080/api/premium-statuses`