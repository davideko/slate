## Get a Premiums Coverages

This endpoint get a premium coverages by composite id.

> Sample request

```shell
curl "http://localhost:8080/api/premiums-coverages/1ffc0022-6e51-43b3-b4b5-649634fd086c@1"
  -H "Authorization: Bearer <token>"
```

> Success response

```json
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
```

> Failed response

```json
{
  "error": "because"
}
```

### HTTP Request

`GET http://localhost:8080/api/premiums-coverages/<compositeId>`

### URL Parameters

Parameter | Description
--------- | -----------
compositeId | It was composed by premium id + "@" + coverage id