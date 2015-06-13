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
            "href": "http://localhost:8080/api/premiums-own-risks/1ffc0022-6e51-43b3-b4b5-649634fd086c@f3409adb-3354-4a31-a742-4cb4a9de2099"
          },
          "premium": {
            "href": "http://localhost:8080/api/premiums-own-risks/1ffc0022-6e51-43b3-b4b5-649634fd086c@f3409adb-3354-4a31-a742-4cb4a9de2099/premium"
          },
          "ownRisk": {
            "href": "http://localhost:8080/api/premiums-own-risks/1ffc0022-6e51-43b3-b4b5-649634fd086c@f3409adb-3354-4a31-a742-4cb4a9de2099/ownRisk"
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
            "href": "http://localhost:8080/api/premiums-own-risks/1ffc0022-6e51-43b3-b4b5-649634fd086c@ae566760-93b2-4267-a75f-f1743a11af80"
          },
          "premium": {
            "href": "http://localhost:8080/api/premiums-own-risks/1ffc0022-6e51-43b3-b4b5-649634fd086c@ae566760-93b2-4267-a75f-f1743a11af80/premium"
          },
          "ownRisk": {
            "href": "http://localhost:8080/api/premiums-own-risks/1ffc0022-6e51-43b3-b4b5-649634fd086c@ae566760-93b2-4267-a75f-f1743a11af80/ownRisk"
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