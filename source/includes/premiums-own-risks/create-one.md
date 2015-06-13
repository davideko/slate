## Add New Premiums Own Risks

This endpoint used to add new premiums own risks

> Sample request

```shell
curl "http://localhost:8080/api/premiums-coverages"
  -X POST
  -H "Authorization: Bearer <token>"
  -H "Content-Type: application/json"
  -d '{
        "premiumCoveragePk":{
            "premium":"http://localhost:8080/api/premiums/1ffc0022-6e51-43b3-b4b5-649634fd086c",
            "coverage":"http://localhost:8080/api/coverages/2"
        },
        "coverageBeginningDate":"2015-06-04",
        "coverageExpiryDate":"2015-10-04",
        "totalSumInsured":100000,
        "thirdPartyLiability":100000
      }'
```

> Success response

```json
{
    "coverageBeginningDate": "2015-06-04T00:00:00.000+0000",
    "coverageExpiryDate": "2015-10-04T00:00:00.000+0000",
    "totalSumInsured": 100000,
    "thirdPartyLiability": 100000,
    "coverage": {
        "coverageType": "CASCO"
    },
    "premium": {
        "extentionCausal": "New cause"
    },
    "_links": {
        "self": {
            "href": "http://localhost:8080/api/premiums-coverages/1ffc0022-6e51-43b3-b4b5-649634fd086c@2"
        },
        "premium": {
            "href": "http://localhost:8080/api/premiums-coverages/1ffc0022-6e51-43b3-b4b5-649634fd086c@2/premium"
        },
        "coverage": {
            "href": "http://localhost:8080/api/premiums-coverages/1ffc0022-6e51-43b3-b4b5-649634fd086c@2/coverage"
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

`POST http://localhost:8080/api/premiums-coverages`

### Parameters

Parameter | Description
--------- | -----------
premiumCoveragePk | Composite object key
premium | Fill with premium object url id
coverage | Fill with coverage object url id
coverageBeginningDate | Fill with coverage beginning date
coverageExpiryDate | Fill with coverage expiry date
totalSumInsured | Fill with total sum insured value
thirdPartyLiability | Fill with third party liability value