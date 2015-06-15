## Search Premium

This endpoint can filter by <code>policyNumber</code>,<code>engineNumber</code>,<code>plateNumber</code>,<code>chassisNumber</code>,<code>certificateNumber</code>, and <code>insuredName</code>.

> Sample request

```shell
curl "http://localhost:8080/api/premiums/search?query=policyNumber:5a0d5fdb-88c8-473b-a210-41afbd6263e2"
  -H "Authorization: Bearer <token>"
```

> Success response

```json
{
    "_links": {
        "self": {
            "href": "http://localhost:8080/api/premiums/search?query=policyNumber:5a0d5fdb-88c8-473b-a210-41afbd6263e2{&page,size,sort}",
            "templated": true
        }
    },
    "_embedded": {
        "premiums": [
            {
                "extentionCausal": "-",
                "_embedded": {
                    "vehicle": {
                        "vehicleSerie": {
                            "vehicleSerieType": "CRV"
                        },
                        "vehicleAssembly": {
                            "vehicleAssemblyType": "Domestic"
                        },
                        "vehicleColor": {
                            "vehicleColorName": "Blue"
                        },
                        "yearModel": "2010",
                        "vehicleId": "fa6a0d05-b700-47d8-abf9-1e19b250fd71",
                        "chassisNumber": "QWERTY45098D477543",
                        "engineNumber": "H89D11547634",
                        "plateNumber": "D 5678 DEF",
                        "certificateNumber": "B778899445566"
                    },
                    "policy": {
                        "policyNumber": "5a0d5fdb-88c8-473b-a210-41afbd6263e2",
                        "insured": {
                            "insuredName": "Joe West",
                            "insuredAddress": "Bekasi",
                            "insuredPhone": "0218861234",
                            "insuredFax": "12345678",
                            "insuredHandphone": "0855778899",
                            "insuredEmail": "this@test.com"
                        },
                        "policyExpiryDate": "2017-10-03",
                        "policyBeginningDate": "2015-06-03"
                    }
                },
                "_links": {
                    "self": {
                        "href": "http://localhost:8080/api/premiums/4c5977df-3cdd-49c1-a0d4-e0c147e8df80"
                    },
                    "premiumCoverage": {
                        "href": "http://localhost:8080/api/premiums/4c5977df-3cdd-49c1-a0d4-e0c147e8df80/premiumCoverage"
                    },
                    "premiumStatus": {
                        "href": "http://localhost:8080/api/premiums/4c5977df-3cdd-49c1-a0d4-e0c147e8df80/premiumStatus"
                    },
                    "premiumOwnRisk": {
                        "href": "http://localhost:8080/api/premiums/4c5977df-3cdd-49c1-a0d4-e0c147e8df80/premiumOwnRisk"
                    },
                    "premiumExtendedCoverage": {
                        "href": "http://localhost:8080/api/premiums/4c5977df-3cdd-49c1-a0d4-e0c147e8df80/premiumExtendedCoverage"
                    }
                }
            }
        ]
    },
    "page": {
        "size": 20,
        "totalElements": 1,
        "totalPages": 1,
        "number": 0
    }
}
```

This endpoint using <code>:</code> as a separator between <code>key</code> and <code>value</code>.

In case that need more than one <code>key</code> you can use <code>,</code> as a separator between <code>key</code>.

For example:

`?query=policyNumber:5a0d5fdb-88c8-473b-a210-41afbd6263e2,engineNumber:L15A24001878`

### HTTP Request

`GET http://localhost:8080/api/premiums/search?query=<selected-filter-key>:<selected-filter-value>`

### URL Parameters

Parameter | Description | Format
--------- | ----------- | ------
policyNumber | Inserted policy number | String
engineNumber | Inserted engine number | String
plateNumber | Inserted plate number | String
chassisNumber | Inserted chassis number | String
certificateNumber | Inserted certificate number | String
insuredName | Inserted insured name | String