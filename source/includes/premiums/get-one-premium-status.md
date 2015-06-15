## Get a Specific Premium Status

This endpoint get premium status by <code>premiumId</code>

> Sample request

```shell
curl "http://localhost:8080/api/premiums/1ffc0022-6e51-43b3-b4b5-649634fd086c/premiumStatus"
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

`GET http://localhost:8080/api/premiums/<premiumId>/premiumStatus`

### URL Parameters

Parameter | Description
--------- | -----------
premiumId | Selected premium id