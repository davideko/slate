## Add New Premiums Extended Coverages

This endpoint used to add new premiums extended coverages

> Sample request

```shell
curl "http://localhost:8080/api/premiums-extended-coverages"
  -X POST
  -H "Authorization: Bearer <token>"
  -H "Content-Type: application/json"
  -d '{
        "premiumExtendedCoveragePk":{
            "premium":"http://localhost:8080/api/premiums/1ffc0022-6e51-43b3-b4b5-649634fd086c",
            "extendedCoverage":"http://localhost:8080/api/extended-coverages/1"
        },
        "extendedCoverageBeginningDate":"2015-06-04",
        "extendedCoverageExpiryDate":"2015-12-04"
      }'
```

> Success response

```json
{
    "extendedCoverageBeginningDate": "2015-06-04T00:00:00.000+0000",
    "extendedCoverageExpiryDate": "2015-12-04T00:00:00.000+0000",
    "premium": {
        "extentionCausal": "New cause"
    },
    "extendedCoverage": {
        "extendedCoverageType": "Comprehensive"
    },
    "_links": {
        "self": {
            "href": "http://localhost:8080/api/premiums-extended-coverages/1ffc0022-6e51-43b3-b4b5-649634fd086c@1"
        },
        "extendedCoverage": {
            "href": "http://localhost:8080/api/premiums-extended-coverages/1ffc0022-6e51-43b3-b4b5-649634fd086c@1/extendedCoverage"
        },
        "premium": {
            "href": "http://localhost:8080/api/premiums-extended-coverages/1ffc0022-6e51-43b3-b4b5-649634fd086c@1/premium"
        }
    }
}
```

### HTTP Request

`POST http://localhost:8080/api/premiums-extended-coverages`

### Parameters

Parameter | Description | Format
--------- | ----------- | ------
premiumExtendedCoveragePk | Composite object key | String
premium | Fill with premium object url id | String
extendedCoverage | Fill with extended coverage object url id | String
extendedCoverageBeginningDate | Fill with extended coverage beginning date | String (date/datetime)
extendedCoverageExpiryDate | Fill with extended coverage expiry date | String (date/datetime)