# Report
All reports endpoint.

## Get All Reports
This endpoint retrieves all reports.

> Sample Request

```shell
curl "http://localhost:8080/api/reports"
  -H "Authorization: Bearer <token>"
```

> Success response 

```json
{
  "_links" : {
    "self" : {
      "href" : "http://localhost:8080/api/reports/{&page,size,sort}",
      "templated" : true
    }
  },
  "_embedded" : {
    "reports" : [ {
      "reportDate" : "2015-05-01",
      "reportedBy" : "Natalie",
      "reportNote" : "",
      "ownRisk" : 5000.00,
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
            "href" : "http://localhost:8080/api/reports/a752d2a4-03b7-42aa-9387-d1093a431380"
          },
          "reportChannel" : {
            "href" : "http://localhost:8080/api/reports/a752d2a4-03b7-42aa-9387-d1093a431380/reportChannel"
          },
          "driver" : {
            "href" : "http://localhost:8080/api/reports/a752d2a4-03b7-42aa-9387-d1093a431380/driver"
          },
          "survey" : {
            "href" : "http://localhost:8080/api/reports/a752d2a4-03b7-42aa-9387-d1093a431380/survey"
          },
          "surveyorEmployee" : {
            "href" : "http://localhost:8080/api/reports/a752d2a4-03b7-42aa-9387-d1093a431380/surveyorEmployee"
          },
          "reportStatus" : {
            "href" : "http://localhost:8080/api/reports/a752d2a4-03b7-42aa-9387-d1093a431380/reportStatus"
          },
          "csStatus" : {
            "href" : "http://localhost:8080/api/reports/a752d2a4-03b7-42aa-9387-d1093a431380/csStatus"
          },
          "surveyorStatus" : {
            "href" : "http://localhost:8080/api/reports/a752d2a4-03b7-42aa-9387-d1093a431380/surveyorStatus"
          },
          "premium" : {
            "href" : "http://localhost:8080/api/reports/a752d2a4-03b7-42aa-9387-d1093a431380/premium"
          },
          "workshopStatus" : {
            "href" : "http://localhost:8080/api/reports/a752d2a4-03b7-42aa-9387-d1093a431380/workshopStatus"
          },
          "lossCausal" : {
            "href" : "http://localhost:8080/api/reports/a752d2a4-03b7-42aa-9387-d1093a431380/lossCausal"
          },
          "csEmployee" : {
            "href" : "http://localhost:8080/api/reports/a752d2a4-03b7-42aa-9387-d1093a431380/csEmployee"
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

### HTTP Request

`GET http://localhost:8080/api/reports`

### URL Parameters
Parameter | Description
--------- | -----------
page | Page you want to retrieve (First page started with 0 (zero))
size | Size of the page you want to retrieve.
sort | Properties that should be sorted. Default sort direction is ascending (Use attributeName.dir to change direction)

<aside class="notice">
  Example : <br />
  <b>reports?size=10&page=3&sort=reportDate&reportDate.dir=desc</b>
</aside>
