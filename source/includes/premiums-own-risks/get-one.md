## Get a Premiums Own Risks

This endpoint get a premium own risks by composite id.

> Sample request

```shell
curl "http://localhost:8080/api/premiums-own-risks/1ffc0022-6e51-43b3-b4b5-649634fd086c@f3409adb-3354-4a31-a742-4cb4a9de2099"
  -H "Authorization: Bearer <token>"
```

> Success response

```json
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
```

> Failed response

```json
{
  "error": "because"
}
```

### HTTP Request

`GET http://localhost:8080/api/premiums-own-risks/<compositeId>`

### URL Parameters

Parameter | Description
--------- | -----------
compositeId | It was composed by premium id + "@" + own risk id