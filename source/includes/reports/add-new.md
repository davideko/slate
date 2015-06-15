## Add New Report
This endpoint will create new report.

> Sample request

```shell
curl "http://localhost:8080/api/reports"
  -X POST
  -H "Authorization: Bearer <token>"
  -d '{
    "reportDate" : "2015-05-05",
    "reportedBy" : "Nico Natalie",
    "reportNote" : "",
    "ownRisk" : 5000,
    "reportChannel" : "http://localhost:8080/api/report-channels/1",
    "lossCausal" : "http://localhost:8080/api/loss-causals/1",
    "premium" : "http://localhost:8080/api/premiums/81546689-a608-40be-815a-f42db7791231",
    "survey" : "http://localhost:8080/api/surveys/5858a7b2-c7ac-464d-8cea-393c291965ae",
    "claimant" : "http://localhost:8080/api/claimants/0bf56d35-1dc2-4826-a6e0-9e67397c6283",
    "driver" : "http://localhost:8080/api/drivers/5fc53083-4d3e-4546-97b8-b2cfd23612cc",
    "csEmployee" : "http://localhost:8080/api/employees/045d9baa-2c68-4390-a385-a4bfef33e9dd",
    "csStatus" : "http://localhost:8080/api/cs-statuses/1",
    "surveyorEmployee" : "http://localhost:8080/api/employees/0f9f0bfa-3e67-498c-bb5d-84a94b56d804",
    "surveyorStatus" : "http://localhost:8080/api/surveyorStatuses/1",
    "workshop" : "http://localhost:8080/api/workshops/42686B50-DB64-4884-85F5-075C19AB92A0",
    "workshopStatus" : "http://localhost:8080/api/workshop-statuses/1",
    "reportStatus" : "http://localhost:8080/api/report-statuses/1"
  }'
```

> Sucessful response

```json
{
  "reportDate": "2015-05-08",
  "reportedBy": "Nico Natalie",
  "reportNote": "",
  "ownRisk": 6000,
  "_embedded": {
      "workshop": {
        "workshopId": "42686B50-DB64-4884-85F5-075C19AB92A0",
        "onlineDate": "2015-06-02",
        "workshopEmail": "oto@oto.com",
        "accountNumber": "1234567880",
        "isSupplier": true,
        "isFeeSystem": true,
        "workshopName": "OTO 1234",
        "workshopFax": "021-6661234",
        "workshopPic": "Ridwan",
        "isActive": true,
        "isOnline": true,
        "workshopPhone": "021-5554422",
        "workshopPicTitle": "Manager",
        "feeSystemValue": 100,
        "workshopAddress": "TANJUNG DUREN SELATAN",
        "workshopPicHandphone": "08123412334",
        "workshopCategory": {
          "workshopCategoryType": "AFFILIATED"
        },
        "workshopDetail": {
          "workshopManager": "Nico Natalie",
          "workshopManagerHandphone": "082120500834",
          "serviceAdvisor": "David Eko",
          "financeManager": "Immanuel Resha",
          "financeManagerHandphone": "1234564455",
          "serviceAdvisorPhone": "123456789001"
        },
        "bank": {
          "bankName": "BANK CENTRAL ASIA"
        },
        "city": {
          "cityName": "JAKARTA"
        },
        "workshopFee": {
          "pph23": 2,
          "sparePartServicePercentage": 80,
          "sparePartPpn": 15,
          "sparePartPercentage": 10,
          "sparePartDiscount": 10,
          "servicePpn": 70,
          "servicePercentage": 20,
          "serviceDiscount": 10,
          "salvageDiscount": 5,
          "isTaxIncluded": true
        },
        "tin": {
          "taxIdentificationName": "ASURANSI UMUM BCA",
          "taxIdentificationAddress": "GEDUNG WTC MANGGA 2 LT 3A BLOK CL003"
        }
      },
    "claimant": {
      "claimantId": "0bf56d35-1dc2-4826-a6e0-9e67397c6283",
      "claimantFax": "123456",
      "claimantName": "Nico Natalie",
      "claimantPhone": "123456",
      "claimantEmail": "asd@asd.com",
      "claimantHandphone": "123456",
      "claimantAddress": "Tanjung Duren",
      "relation": {
        "relationType": "Owner"
      }
    }
  },
  "_links": {
    "self": {
      "href": "http://localhost:8080/api/reports/2d451f4e-9547-4691-8193-1eb32dc16e4a"
    },
    "reportChannel": {
      "href": "http://localhost:8080/api/reports/2d451f4e-9547-4691-8193-1eb32dc16e4a/reportChannel"
    },
    "driver": {
      "href": "http://localhost:8080/api/reports/2d451f4e-9547-4691-8193-1eb32dc16e4a/driver"
    },
    "survey": {
      "href": "http://localhost:8080/api/reports/2d451f4e-9547-4691-8193-1eb32dc16e4a/survey"
    },
    "claimant": {
      "href": "http://localhost:8080/api/reports/2d451f4e-9547-4691-8193-1eb32dc16e4a/claimant"
    },
    "surveyorEmployee": {
      "href": "http://localhost:8080/api/reports/2d451f4e-9547-4691-8193-1eb32dc16e4a/surveyorEmployee"
    },
    "reportStatus": {
      "href": "http://localhost:8080/api/reports/2d451f4e-9547-4691-8193-1eb32dc16e4a/reportStatus"
    },
    "csStatus": {
      "href": "http://localhost:8080/api/reports/2d451f4e-9547-4691-8193-1eb32dc16e4a/csStatus"
    },
    "surveyorStatus": {
      "href": "http://localhost:8080/api/reports/2d451f4e-9547-4691-8193-1eb32dc16e4a/surveyorStatus"
    },
    "premium": {
      "href": "http://localhost:8080/api/reports/2d451f4e-9547-4691-8193-1eb32dc16e4a/premium"
    },
    "workshopStatus": {
      "href": "http://localhost:8080/api/reports/2d451f4e-9547-4691-8193-1eb32dc16e4a/workshopStatus"
    },
    "lossCausal": {
      "href": "http://localhost:8080/api/reports/2d451f4e-9547-4691-8193-1eb32dc16e4a/lossCausal"
    },
    "csEmployee": {
      "href": "http://localhost:8080/api/reports/2d451f4e-9547-4691-8193-1eb32dc16e4a/csEmployee"
    },
    "workshop": {
      "href": "http://localhost:8080/api/reports/2d451f4e-9547-4691-8193-1eb32dc16e4a/workshop"
    }
  }
}
```

### HTTP Request

`POST http://localhost:8080/api/reports`

###  Parameters

Parameter | Description | Data Type
--------- | ----------- | ---------
reportDate | Date of report | string
reportedBy | Name of reporter | string
reportNote | Report notes (optional) | string
ownRisk | Total own risk (calculated) | integer
reportChannel | Report channel object url | string
lossCausal | Loss causal object url | string
premium | Premium object url | string
survey | Survey object url | string
claimant | Claimant object url | string
driver | Driver object url | string
csEmployee | Employee object url | string
csStatus | Cs status object url | string
surveyorEmployee | Employee object url | string
surveyorStatus | Surveyor object url | string
workshop | Workshop object url | string
workshopStatus | Workshop status object url | string