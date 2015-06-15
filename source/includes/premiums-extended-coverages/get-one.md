## Get a Premiums Extended Coverages

This endpoint get a premium extended coverages by composite id.

> Sample request

```shell
curl "http://localhost:8080/api/premiums-extended-coverages/1ffc0022-6e51-43b3-b4b5-649634fd086c@1"
  -H "Authorization: Bearer <token>"
```

> Success response

```json
{
    "extendedCoverageBeginningDate": "2015-06-04",
    "extendedCoverageExpiryDate": "2015-12-04",
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

`GET http://localhost:8080/api/premiums-extended-coverages/<compositeId>`

### URL Parameters

Parameter | Description
--------- | -----------
compositeId | It was composed by premium id + "@" + extended coverage id