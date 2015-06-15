## Get a Specific Premium Extended Coverage

This endpoint get premium extended coverage by <code>premiumId</code>

> Sample request

```shell
curl "http://localhost:8080/api/premiums/1ffc0022-6e51-43b3-b4b5-649634fd086c/premiumExtendedCoverage"
  -H "Authorization: Bearer <token>"
```

> Success response

```json
{
    "_embedded": {
        "premiumsExtendedCoverages": [
            {
                "extendedCoverageBeginningDate": "2015-06-04",
                "extendedCoverageExpiryDate": "2015-12-04",
                "premium": {
                    "extentionCausal": "New cause"
                },
                "extendedCoverage": {
                    "extendedCoverageType": "Flood"
                },
                "_links": {
                    "self": {
                        "href": "http://localhost:8080/api/premiums-extended-coverages/1ffc0022-6e51-43b3-b4b5-649634fd086c@2"
                    },
                    "extendedCoverage": {
                        "href": "http://localhost:8080/api/premiums-extended-coverages/1ffc0022-6e51-43b3-b4b5-649634fd086c@2/extendedCoverage"
                    },
                    "premium": {
                        "href": "http://localhost:8080/api/premiums-extended-coverages/1ffc0022-6e51-43b3-b4b5-649634fd086c@2/premium"
                    }
                }
            },
            {
                "extendedCoverageBeginningDate": "2015-06-04",
                "extendedCoverageExpiryDate": "2015-12-04",
                "premium": {
                    "extentionCausal": "New cause"
                },
                "extendedCoverage": {
                    "extendedCoverageType": "Earthquake"
                },
                "_links": {
                    "self": {
                        "href": "http://localhost:8080/api/premiums-extended-coverages/1ffc0022-6e51-43b3-b4b5-649634fd086c@3"
                    },
                    "extendedCoverage": {
                        "href": "http://localhost:8080/api/premiums-extended-coverages/1ffc0022-6e51-43b3-b4b5-649634fd086c@3/extendedCoverage"
                    },
                    "premium": {
                        "href": "http://localhost:8080/api/premiums-extended-coverages/1ffc0022-6e51-43b3-b4b5-649634fd086c@3/premium"
                    }
                }
            },
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
        ]
    }
}
```

### HTTP Request

`GET http://localhost:8080/api/premiums/<premiumId>/premiumExtendedCoverage`

### URL Parameters

Parameter | Description
--------- | -----------
premiumId | Selected premium id