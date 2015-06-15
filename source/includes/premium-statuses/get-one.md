## Get a Specific Premium Status

This endpoint get premium status by <code>premiumStatusId</code>

> Sample request

```shell
curl "http://localhost:8080/api/premium-statuses/1"
  -H "Authorization: Bearer <token>"
```

> Success response

```json
{
    "premiumStatusType": "Active",
    "_links": {
        "self": {
            "href": "http://localhost:8080/api/premium-statuses/1"
        }
    }
}
```

### HTTP Request

`GET http://localhost:8080/api/premium-statuses/{premiumStatusId}`

### URL Parameters

Parameter | Description
--------- | -----------
premiumStatusId | Selected premium status id
