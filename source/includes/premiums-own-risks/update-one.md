## Update Premiums Own Risks
This endpoint used to update a premiums own risks object. It can update using <code>PUT</code> for full update or <code>PATCH</code> for partial update

> Sample request PUT

```shell
curl "http://localhost:8080/api/premiums-own-risks/1ffc0022-6e51-43b3-b4b5-649634fd086c@1"
  -X PUT
  -H "Authorization: Bearer <token>"
  -H "Content-Type: application/json"
  -d '{
        "ownRiskDescription":"20 % Claim Minimum"
      }'
```

> Sample request PATCH

```shell
curl "http://localhost:8080/api/premiums-own-risks/1ffc0022-6e51-43b3-b4b5-649634fd086c@1"
  -X PATCH
  -H "Authorization: Bearer <token>"
  -H "Content-Type: application/json"
  -d '{
        "ownRiskDescription":"20 % Claim Minimum"
      }'
```

> Success response

```json
{
    "ownRiskDescription": "20 % Claim Minimum",
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

`PUT http://localhost:8080/api/premiums-own-risks/<compositeId>`

`PATCH http://localhost:8080/api/premiums-own-risks/<compositeId>`

### URL Parameters

Parameter | Description
--------- | -----------
compositeId | It was composed by premium id + "@" + own risk id

### Parameters

Parameter | Description
--------- | -----------
ownRiskDescription | Fill with own risk description
