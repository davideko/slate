## Get a Specific Premium Coverage

This endpoint get premium coverage by <code>premiumId</code>

> Sample request

```shell
curl "http://localhost:8080/api/premiums/1ffc0022-6e51-43b3-b4b5-649634fd086c/premiumCoverage"
  -H "Authorization: Bearer <token>"
```

> Success response

```json
{
    "_embedded": {
        "premiumsCoverages": [
            {
                "coverageBeginningDate": "2015-06-04",
                "coverageExpiryDate": "2015-10-04",
                "totalSumInsured": 100000,
                "thirdPartyLiability": 100000,
                "coverage": {
                    "coverageType": "TPL"
                },
                "premium": {
                    "extentionCausal": "New cause"
                },
                "_links": {
                    "self": {
                        "href": "http://localhost:8080/api/premiums-coverages/1ffc0022-6e51-43b3-b4b5-649634fd086c@3"
                    },
                    "premium": {
                        "href": "http://localhost:8080/api/premiums-coverages/1ffc0022-6e51-43b3-b4b5-649634fd086c@3/premium"
                    },
                    "coverage": {
                        "href": "http://localhost:8080/api/premiums-coverages/1ffc0022-6e51-43b3-b4b5-649634fd086c@3/coverage"
                    }
                }
            },
            {
                "coverageBeginningDate": "2015-03-04",
                "coverageExpiryDate": "2017-12-04",
                "totalSumInsured": 100000,
                "thirdPartyLiability": 100000,
                "coverage": {
                    "coverageType": "TPL"
                },
                "premium": {
                    "extentionCausal": "New cause"
                },
                "_links": {
                    "self": {
                        "href": "http://localhost:8080/api/premiums-coverages/1ffc0022-6e51-43b3-b4b5-649634fd086c@4"
                    },
                    "premium": {
                        "href": "http://localhost:8080/api/premiums-coverages/1ffc0022-6e51-43b3-b4b5-649634fd086c@4/premium"
                    },
                    "coverage": {
                        "href": "http://localhost:8080/api/premiums-coverages/1ffc0022-6e51-43b3-b4b5-649634fd086c@4/coverage"
                    }
                }
            },
            {
                "coverageBeginningDate": "2015-06-04",
                "coverageExpiryDate": "2015-10-04",
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
            },
            {
                "coverageBeginningDate": "2015-06-04",
                "coverageExpiryDate": "2017-10-04",
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
        ]
    }
}
```

### HTTP Request

`GET http://localhost:8080/api/premiums/<premiumId>/premiumCoverage`

### URL Parameters

Parameter | Description
--------- | -----------
premiumId | Selected premium id
