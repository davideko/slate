## Update Premium Status

This endpoint used to update a premium status object. It can update using <code>PUT</code> for full update or <code>PATCH</code> for partial update

> Sample request PUT

```shell
curl "http://localhost:8080/api/premium-statuses/1"
  -X PUT
  -H "Authorization: Bearer <token>"
  -H "Content-Type: application/json"
  -d '{
        "premiumStatusType":"New"
      }'
```

> Sample request PATCH

```shell
curl "http://localhost:8080/api/premium-statuses/1"
  -X PATCH
  -H "Authorization: Bearer <token>"
  -H "Content-Type: application/json"
  -d '{
        "premiumStatusType":"New"
      }'
```

> Success response

```json
{
    "premiumStatusType": "New",
    "_links": {
        "self": {
            "href": "http://localhost:8080/api/premium-statuses/1"
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

`PUT http://localhost:8080/api/premium-statuses/<premiumStatusId>`

`PATCH http://localhost:8080/api/premium-statuses/<premiumStatusId>`

### URL Parameters

Parameter | Description
--------- | -----------
premiumStatusId | Selected premium status id

### Parameters

Parameter | Description | Format 
--------- | ----------- | ------ 
premiumStatusType | Fill with premium status type | String