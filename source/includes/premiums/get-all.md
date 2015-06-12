# Premiums
## Get All Premiums

This endpoint used to return all premiums

> Sample request

```shell
curl "http://localhost:8080/api/premiums"
  -H "Authorization: Bearer <token>"
```

> Success response

```json
{
    "_links": {
        "self": {
            "href": "http://localhost:8080/api/premiums{?page,size,sort}",
            "templated": true
        }
    },
    "_embedded": {
        "premiums": [
            {
                "extentionCausal": "New cause",
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
                        "yearModel": "2007",
                        "vehicleId": "937d15ef-2c04-40de-a5e6-3a34d5031345",
                        "chassisNumber": "MHRGD38207J700989",
                        "engineNumber": "L15A24001878",
                        "plateNumber": "B 1234 ABC",
                        "certificateNumber": "A113344556677"
                    },
                    "policy": {
                        "policyNumber": "2b46fc11-8f45-43ac-a305-fbe1be4b7dae",
                        "insured": {
                            "insuredName": "Star Lord",
                            "insuredAddress": "Galaxy",
                            "insuredPhone": "0218875645",
                            "insuredFax": "56789844",
                            "insuredHandphone": "0888888811",
                            "insuredEmail": "test@this.com"
                        },
                        "policyExpiryDate": "2017-06-03",
                        "policyBeginningDate": "2015-06-03"
                    }
                },
                "_links": {
                    "self": {
                        "href": "http://localhost:8080/api/premiums/1ffc0022-6e51-43b3-b4b5-649634fd086c"
                    },
                    "premiumCoverage": {
                        "href": "http://localhost:8080/api/premiums/1ffc0022-6e51-43b3-b4b5-649634fd086c/premiumCoverage"
                    },
                    "premiumStatus": {
                        "href": "http://localhost:8080/api/premiums/1ffc0022-6e51-43b3-b4b5-649634fd086c/premiumStatus"
                    },
                    "premiumOwnRisk": {
                        "href": "http://localhost:8080/api/premiums/1ffc0022-6e51-43b3-b4b5-649634fd086c/premiumOwnRisk"
                    },
                    "premiumExtendedCoverage": {
                        "href": "http://localhost:8080/api/premiums/1ffc0022-6e51-43b3-b4b5-649634fd086c/premiumExtendedCoverage"
                    }
                }
            },
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
        "totalElements": 2,
        "totalPages": 1,
        "number": 0
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

`GET http://localhost:8080/api/premiums`