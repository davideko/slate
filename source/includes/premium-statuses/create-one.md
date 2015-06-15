## Add New Premium Status

This endpoint used to add new premium status

> Sample request

```shell
curl "http://localhost:8080/api/premium-statuses"
  -X POST
  -H "Authorization: Bearer <token>"
  -H "Content-Type: application/json"
  -d '{
        "premiumStatusType":"Active"
      }'
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

`POST http://localhost:8080/api/premium-statuses`

### Parameters

Parameter | Description | Format 
--------- | ----------- | ------ 
premiumStatusType | Fill with premium status type | String 