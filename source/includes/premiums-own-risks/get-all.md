# Premiums Own Risks
## Get Premiums Own Risks

This endpoint used to return all premiums own risks

> Sample request

```shell
curl "http://localhost:8080/api/premiums-own-risks"
  -H "Authorization: Bearer <token>"
```

> Success response

```json
{
    "_embedded": {
        "premiumsOwnRisks": [
            {
                "ownRiskDescription": "10 % Claim Minimum",
                "premium": {
                    "extentionCausal": "New cause"
                },
                "ownRisk": {
                    "ownRiskType": "Earthquake"
                },
                "_links": {
                    "self": {
                        "href": "http://localhost:8080/api/premiums-own-risks/1ffc0022-6e51-43b3-b4b5-649634fd086c@1"
                    },
                    "premium": {
                        "href": "http://localhost:8080/api/premiums-own-risks/1ffc0022-6e51-43b3-b4b5-649634fd086c@1/premium"
                    },
                    "ownRisk": {
                        "href": "http://localhost:8080/api/premiums-own-risks/1ffc0022-6e51-43b3-b4b5-649634fd086c@1/ownRisk"
                    }
                }
            },
            {
                "ownRiskDescription": "20 % Claim Minimum",
                "premium": {
                    "extentionCausal": "New cause"
                },
                "ownRisk": {
                    "ownRiskType": "Flood"
                },
                "_links": {
                    "self": {
                        "href": "http://localhost:8080/api/premiums-own-risks/1ffc0022-6e51-43b3-b4b5-649634fd086c@2"
                    },
                    "premium": {
                        "href": "http://localhost:8080/api/premiums-own-risks/1ffc0022-6e51-43b3-b4b5-649634fd086c@2/premium"
                    },
                    "ownRisk": {
                        "href": "http://localhost:8080/api/premiums-own-risks/1ffc0022-6e51-43b3-b4b5-649634fd086c@2/ownRisk"
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

`GET http://localhost:8080/api/premiums-own-risks`