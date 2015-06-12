## Get a Specific Premium Own Risk

This endpoint get premium own risk by <code>premiumId</code>

> Sample request

```shell
curl "http://localhost:8080/api/premiums/1ffc0022-6e51-43b3-b4b5-649634fd086c/premiumOwnRisk"
  -H "Authorization: Bearer <token>"
```

> Success response

```json
{
    "_embedded": {
        "premiumsOwnRisks": [
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
                        "href": "http://localhost:8080/api/premiums-own-risks/1ffc0022-6e51-43b3-b4b5-649634fd086c@ae566760-93b2-4267-a75f-f1743a11af80"
                    },
                    "premium": {
                        "href": "http://localhost:8080/api/premiums-own-risks/1ffc0022-6e51-43b3-b4b5-649634fd086c@ae566760-93b2-4267-a75f-f1743a11af80/premium"
                    },
                    "ownRisk": {
                        "href": "http://localhost:8080/api/premiums-own-risks/1ffc0022-6e51-43b3-b4b5-649634fd086c@ae566760-93b2-4267-a75f-f1743a11af80/ownRisk"
                    }
                }
            },
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
                        "href": "http://localhost:8080/api/premiums-own-risks/1ffc0022-6e51-43b3-b4b5-649634fd086c@f3409adb-3354-4a31-a742-4cb4a9de2099"
                    },
                    "premium": {
                        "href": "http://localhost:8080/api/premiums-own-risks/1ffc0022-6e51-43b3-b4b5-649634fd086c@f3409adb-3354-4a31-a742-4cb4a9de2099/premium"
                    },
                    "ownRisk": {
                        "href": "http://localhost:8080/api/premiums-own-risks/1ffc0022-6e51-43b3-b4b5-649634fd086c@f3409adb-3354-4a31-a742-4cb4a9de2099/ownRisk"
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

`GET http://localhost:8080/api/premiums/<premiumId>/premiumOwnRisk`

### URL Parameters

Parameter | Description
--------- | -----------
premiumId | Selected premium id