## Get a Specific Own Risk

This endpoint get own risk by <code>ownRiskId</code>

> Sample request

```shell
curl "href": "http://localhost:8080/api/own-risks/1"
  -H "Authorization: Bearer <token>"
```

> Success response

```json
{
    "ownRiskType": "Flood",
    "_links": {
        "self": {
            "href": "http://localhost:8080/api/own-risks/1"
        }
    }
}
```

### HTTP Request

`GET http://localhost:8080/api/own-risks/{ownRiskId}`

### URL Parameters

Parameter | Description
--------- | -----------
ownRiskId | Selected own risk id
