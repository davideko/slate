## Update Premiums Coverages

This endpoint used to update a premiums coverages object. It can update using <code>PUT</code> for full update or <code>PATCH</code> for partial update

> Sample request PUT

```shell
curl "http://localhost:8080/api/premiums-coverages/1ffc0022-6e51-43b3-b4b5-649634fd086c@1"
  -X PUT
  -H "Authorization: Bearer <token>"
  -H "Content-Type: application/json"
  -d '{
        "coverageBeginningDate":"2015-06-04",
        "coverageExpiryDate":"2017-10-04",
        "totalSumInsured":400000,
        "thirdPartyLiability":500000
      }'
```

> Sample request PATCH

```shell
curl "http://localhost:8080/api/premiums-coverages/1ffc0022-6e51-43b3-b4b5-649634fd086c@1"
  -X PATCH
  -H "Authorization: Bearer <token>"
  -H "Content-Type: application/json"
  -d '{
        "thirdPartyLiability":500000
      }'
```

> Success response

```json
{
    "coverageBeginningDate": "2015-06-04T00:00:00.000+0000",
    "coverageExpiryDate": "2017-10-04T00:00:00.000+0000",
    "totalSumInsured": 400000,
    "thirdPartyLiability": 500000,
    "coverage": {
        "coverageType": "CASCO"
    },
    "premium": {
        "extentionCausal": "New cause"
    },
    "_links": {
        "self": {
            "href": "http://localhost:8080/api/premiums-coverages/1ffc0022-6e51-43b3-b4b5-649634fd086c@1"
        },
        "premium": {
            "href": "http://localhost:8080/api/premiums-coverages/1ffc0022-6e51-43b3-b4b5-649634fd086c@1/premium"
        },
        "coverage": {
            "href": "http://localhost:8080/api/premiums-coverages/1ffc0022-6e51-43b3-b4b5-649634fd086c@1/coverage"
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

`PUT http://localhost:8080/api/premiums-coverages/<compositeId>`

`PATCH http://localhost:8080/api/premiums-coverages/<compositeId>`

### URL Parameters

Parameter | Description
--------- | -----------
compositeId | It was composed by premium id + "@" + coverage id

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
