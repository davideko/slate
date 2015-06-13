## Add New Premiums Own Risks

This endpoint used to add new premiums own risks

> Sample request

```shell
curl "http://localhost:8080/api/premiums-own-risks"
  -X POST
  -H "Authorization: Bearer <token>"
  -H "Content-Type: application/json"
  -d '{
        "premiumOwnRiskPk":{
            "premium":"http://localhost:8080/api/premiums/1ffc0022-6e51-43b3-b4b5-649634fd086c",
            "ownRisk":"http://localhost:8080/api/own-risks/1"
        },
        "ownRiskDescription":"10 % Claim Minimum"
      }'
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
            "href": "http://localhost:8080/api/premiums-own-risks/1ffc0022-6e51-43b3-b4b5-649634fd086c@1"
        },
        "premium": {
            "href": "http://localhost:8080/api/premiums-own-risks/1ffc0022-6e51-43b3-b4b5-649634fd086c@1/premium"
        },
        "ownRisk": {
            "href": "http://localhost:8080/api/premiums-own-risks/1ffc0022-6e51-43b3-b4b5-649634fd086c@1/ownRisk"
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

`POST http://localhost:8080/api/premiums-own-risks`

### Parameters

Parameter | Description
--------- | -----------
premiumOwnRiskPk | Composite object key
premium | Fill with premium object url id
ownRisk | Fill with own risk object url id
ownRiskDescription | Fill with own risk description