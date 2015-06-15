## Get a Specific Premium

This endpoint get premium by <code>premiumId</code>

> Sample request

```shell
curl "http://localhost:8080/api/premiums/1ffc0022-6e51-43b3-b4b5-649634fd086c"
  -H "Authorization: Bearer <token>"
```

> Success response

```json
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
        "vehicle": {
            "href": "http://localhost:8080/api/premiums/1ffc0022-6e51-43b3-b4b5-649634fd086c/vehicle"
        },
        "policy": {
            "href": "http://localhost:8080/api/premiums/1ffc0022-6e51-43b3-b4b5-649634fd086c/policy"
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
}
```

### HTTP Request

`GET http://localhost:8080/api/premiums/<premiumId>`

### URL Parameters

Parameter | Description
--------- | -----------
premiumId | Selected premium id