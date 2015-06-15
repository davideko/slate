# Own Risks
## Get All Own Risks

This endpoint used to return all own risks

> Sample request

```shell
curl "http://localhost:8080/api/own-risks"
  -H "Authorization: Bearer <token>"
```

> Success response

```json
{
    "_embedded": {
        "ownRisks": [
            {
                "ownRiskType": "Flood",
                "_links": {
                    "self": {
                        "href": "http://localhost:8080/api/own-risks/1"
                    }
                }
            },
            {
                "ownRiskType": "Earthquake",
                "_links": {
                    "self": {
                        "href": "http://localhost:8080/api/own-risks/1"
                    }
                }
            }
        ]
    }
}
```

### HTTP Request 

`GET http://localhost:8080/api/own-risks`