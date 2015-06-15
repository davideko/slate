## Search Report
This endpoint retrieves reports by Query String.

> Sample request

```shell
curl "http://localhost:8080/api/reports/search?query=reportDate:2015-05-08"
  -H "Authorization: Bearer <token>"
```

> Sucessful response

```json
{
  "_links" : {
    "self" : {
      "href" : "http://localhost:8080/api/reports/search?query=reportDate:2015-05-08{&page,size,sort}",
      "templated" : true
    }
  },
    "_embedded" : {
      "reports" : [ {
        "reportDate" : "2015-05-08",
        "reportedBy" : "Nico Natalie",
        "reportNote" : "Added Report Note",
        "ownRisk" : 6000.00,
          "_embedded" : {
            "workshop" : {
              "workshopCategory" : {
                "workshopCategoryType" : "AFFILIATED"
              },
              "workshopDetail" : {
                "workshopManager" : "Nico Natalie",
                "workshopManagerHandphone" : "082120500834",
                "serviceAdvisor" : "David Eko",
                "financeManager" : "Immanuel Resha",
                "financeManagerHandphone" : "1234564455",
                "serviceAdvisorPhone" : "123456789001"
              },
              "onlineDate" : "2015-06-02",
              "workshopEmail" : "oto@oto.com",
              "accountNumber" : "1234567880",
              "isSupplier" : true,
              "isFeeSystem" : true,
              "workshopName" : "OTO 1234",
              "workshopFax" : "021-6661234",
              "workshopPic" : "Ridwan",
              "isActive" : true,
              "isOnline" : true,
              "workshopPhone" : "021-5554422",
              "workshopPicTitle" : "Manager",
              "feeSystemValue" : 100,
              "workshopAddress" : "TANJUNG DUREN SELATAN",
              "workshopPicHandphone" : "08123412334",
              "bank" : {
                "bankName" : "BANK CENTRAL ASIA"
              },
              "city" : {
                "cityName" : "JAKARTA"
              },
              "workshopFee" : {
                "pph23" : 2,
                "sparePartServicePercentage" : 80,
                "sparePartPpn" : 15,
                "sparePartPercentage" : 10,
                "sparePartDiscount" : 10,
                "servicePpn" : 70,
                "servicePercentage" : 20,
                "serviceDiscount" : 10,
                "salvageDiscount" : 5,
                "isTaxIncluded" : true
              },
              "workshopId" : "42686B50-DB64-4884-85F5-075C19AB92A0",
              "tin" : {
                "taxIdentificationName" : "ASURANSI UMUM BCA",
                "taxIdentificationAddress" : "GEDUNG WTC MANGGA 2 LT 3A BLOK CL003"
              }
            },
            "claimant" : {
              "claimantId" : "0bf56d35-1dc2-4826-a6e0-9e67397c6283",
              "relation" : {
                "relationType" : "Owner"
              },
              "claimantFax" : "123456",
              "claimantName" : "Nico Natalie",
              "claimantPhone" : "123456",
              "claimantEmail" : "asd@asd.com",
              "claimantHandphone" : "123456",
              "claimantAddress" : "Tanjung Duren"
            }
          },
          "_links" : {
            "self" : {
              "href" : "http://localhost:8080/api/reports/2d451f4e-9547-4691-8193-1eb32dc16e4a"
            },
            "reportChannel" : {
              "href" : "http://localhost:8080/api/reports/2d451f4e-9547-4691-8193-1eb32dc16e4a/reportChannel"
            },
            "driver" : {
              "href" : "http://localhost:8080/api/reports/2d451f4e-9547-4691-8193-1eb32dc16e4a/driver"
            },
            "survey" : {
              "href" : "http://localhost:8080/api/reports/2d451f4e-9547-4691-8193-1eb32dc16e4a/survey"
            },
            "surveyorEmployee" : {
              "href" : "http://localhost:8080/api/reports/2d451f4e-9547-4691-8193-1eb32dc16e4a/surveyorEmployee"
            },
            "reportStatus" : {
              "href" : "http://localhost:8080/api/reports/2d451f4e-9547-4691-8193-1eb32dc16e4a/reportStatus"
            },
            "csStatus" : {
              "href" : "http://localhost:8080/api/reports/2d451f4e-9547-4691-8193-1eb32dc16e4a/csStatus"
            },
            "surveyorStatus" : {
              "href" : "http://localhost:8080/api/reports/2d451f4e-9547-4691-8193-1eb32dc16e4a/surveyorStatus"
            },
            "premium" : {
              "href" : "http://localhost:8080/api/reports/2d451f4e-9547-4691-8193-1eb32dc16e4a/premium"
            },
            "workshopStatus" : {
              "href" : "http://localhost:8080/api/reports/2d451f4e-9547-4691-8193-1eb32dc16e4a/workshopStatus"
            },
            "lossCausal" : {
              "href" : "http://localhost:8080/api/reports/2d451f4e-9547-4691-8193-1eb32dc16e4a/lossCausal"
            },
            "csEmployee" : {
              "href" : "http://localhost:8080/api/reports/2d451f4e-9547-4691-8193-1eb32dc16e4a/csEmployee"
            }
          }
      } ]
    },
  "page" : {
    "size" : 20,
    "totalElements" : 1,
    "totalPages" : 1,
    "number" : 0
  }
}
```

### HTTP request 

`GET http://localhost:8080/api/reports/search?{query}`

### URL Parameters
Parameter | Description | Data Type
--------- | ----------- | ---------
query | Query String | string

<aside class="notice">
  Format Query String: <br /><br />

  <b>[attributeName] [operations] [value] , [attributeName] [operations] [value], ...</b>

  <br /><br />
  Available operations: <br />
    <code><b>:</b></code> means equal or like <br />
    <code><b>></b></code> means greater than or equal <br />
    <code><b><</b></code> means less than or equal <br /><br />

  Example:<br />
  <b>query=reportDate>2015-06-06,reportDate<2015-06-20,policyNumber:AA23</b>
</aside>