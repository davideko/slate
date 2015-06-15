## Update Premiums Coverages

This endpoint used to update a premiums coverages object. It can update using <code>PUT</code> for full update or <code>PATCH</code> for partial update

> Sample request PUT

```shell
curl "http://localhost:8080/api/premiums-extended-coverages/1ffc0022-6e51-43b3-b4b5-649634fd086c@1"
  -X PUT
  -H "Authorization: Bearer <token>"
  -H "Content-Type: application/json"
  -d '{
        "extendedCoverageBeginningDate":"2015-04-04",
        "extendedCoverageExpiryDate":"2015-12-04"
      }'
```

> Sample request PATCH

```shell
curl "http://localhost:8080/api/premiums-extended-coverages/1ffc0022-6e51-43b3-b4b5-649634fd086c@1"
  -X PATCH
  -H "Authorization: Bearer <token>"
  -H "Content-Type: application/json"
  -d '{
        "extendedCoverageBeginningDate":"2015-04-04"
      }'
```

> Success response

```json
{
    "extendedCoverageBeginningDate": "2015-04-04T00:00:00.000+0000",
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

`PUT http://localhost:8080/api/premiums-extended-coverages/{compositeId}`

`PATCH http://localhost:8080/api/premiums-extended-coverages/{compositeId}`

### URL Parameters

Parameter | Description
--------- | -----------
compositeId | It was composed by premium id + "@" + extended coverage id

### Parameters

Parameter | Description | Format
--------- | ----------- | ------
extendedCoverageBeginningDate | Fill with extended coverage beginning date | String (date/datetime)
extendedCoverageExpiryDate | Fill with extended coverage expiry date | String (date/datetime)
