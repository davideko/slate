# Workshop

## Get All Worskhop
This endpoint retrieves all workshops.

> Sample request

```shell
  curl "http://localhost:8080/api/workshops"
  -H "Authorization: Bearer <token>"
```

> Success response

```json
{
  "_embedded" : {
    "workshops" : [ {
      "workshopFax" : "021-6661234",
      "isSupplier" : true,
      "onlineDate" : "2015-06-02",
      "accountNumber" : "1234567880",
      "workshopPic" : "Ridwan",
      "isFeeSystem" : true,
      "workshopPhone" : "021-5554422",
      "isOnline" : true,
      "workshopEmail" : "oto@oto.com",
      "workshopName" : "OTO 1234",
      "isActive" : true,
      "workshopId" : "42686B50-DB64-4884-85F5-075C19AB92A0",
      "bank" : {
        "bankName" : "BANK CENTRAL ASIA"
      },
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
      "city" : {
        "cityName" : "JAKARTA"
      },
      "feeSystemValue" : 100,
      "workshopPicHandphone" : "08123412334",
      "workshopPicTitle" : "Manager",
      "workshopAddress" : "TANJUNG DUREN SELATAN",
      "tin" : {
        "taxIdentificationName" : "ASURANSI UMUM BCA",
        "taxIdentificationAddress" : "GEDUNG WTC MANGGA 2 LT 3A BLOK CL003"
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
      "_links" : {
        "self" : {
          "href" : "http://localhost:8080/api/workshops/42686B50-DB64-4884-85F5-075C19AB92A0{?projection}",
          "templated" : true
        },
        "bank" : {
          "href" : "http://localhost:8080/api/banks/1"
        },
        "city" : {
          "href" : "http://localhost:8080/api/cities/1"
        },
        "tin" : {
          "href" : "http://localhost:8080/api/tins/01.342.006.2-046.000"
        },
        "workshopCategory" : {
          "href" : "http://localhost:8080/api/workshop-categories/1"
        },
        "workshopDetail" : {
          "href" : "http://localhost:8080/api/workshop-details/4CFEADB9-EAF8-48A7-808A-0CF141A8B99D"
        },
        "workshopFee" : {
          "href" : "http://localhost:8080/api/workshop-fees/EDFFF909-64AA-4A7B-807E-77A7875F805C"
        }
      }
    } ]
  }
}
```

### HTTP Request

`GET http://localhost:8080/api/workshops`

