## Add New Premium

This endpoint used to add new premium

> Sample request

```shell
curl "http://localhost:8080/api/premiums"
  -X POST
  -H "Authorization: Bearer <token>"
  -H "Content-Type: application/json"
  -d '{
        "extentionCausal":"cause",
        "policy":"http://localhost:8080/api/policies/2b46fc11-8f45-43ac-a305-fbe1be4b7dae",
        "vehicle":"http://localhost:8080/api/insureds/937d15ef-2c04-40de-a5e6-3a34d5031345",
        "premiumStatus":"http://localhost:8080/api/premium-statuses/1"
     }'
```

> Success response

```json
{
    "extentionCausal": "cause",
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
                "href": "http://localhost:8080/api/premiums/40e4e490-a0e8-4983-b3bb-adc7e0192d00"
            },
            "vehicle": {
                "href": "http://localhost:8080/api/premiums/40e4e490-a0e8-4983-b3bb-adc7e0192d00/vehicle"
            },
            "policy": {
                "href": "http://localhost:8080/api/premiums/40e4e490-a0e8-4983-b3bb-adc7e0192d00/policy"
            },
            "premiumCoverage": {
                "href": "http://localhost:8080/api/premiums/40e4e490-a0e8-4983-b3bb-adc7e0192d00/premiumCoverage"
            },
            "premiumStatus": {
                "href": "http://localhost:8080/api/premiums/40e4e490-a0e8-4983-b3bb-adc7e0192d00/premiumStatus"
            },
            "premiumOwnRisk": {
                "href": "http://localhost:8080/api/premiums/40e4e490-a0e8-4983-b3bb-adc7e0192d00/premiumOwnRisk"
            },
            "premiumExtendedCoverage": {
                "href": "http://localhost:8080/api/premiums/40e4e490-a0e8-4983-b3bb-adc7e0192d00/premiumExtendedCoverage"
            }
      }
}
```

### HTTP Request

`POST http://localhost:8080/api/premiums`

### Parameters

Parameter | Description | Format
--------- | ----------- | ------
extentionCausal | Fill with extention causal | String
policy | Fill with policyobject url  | String
vehicle | Fill with vehicle object url id | String
premiumStatus | Fill with premiumStatus object url id | String
