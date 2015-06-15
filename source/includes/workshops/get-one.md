## Get a Specific Workshop
This endpoint retrieves specific workshop.

> Sample request

```shell
  curl "http://localhost:8080/api/workshops/42686B50-DB64-4884-85F5-075C19AB92A0"
  -H "Authorization: Bearer <token>"
```

> Success response

```json
{
  "workshopName" : "OTO 1234",
  "workshopAddress" : "TANJUNG DUREN SELATAN",
  "workshopPhone" : "021-5554422",
  "workshopFax" : "021-6661234",
  "workshopEmail" : "oto@oto.com",
  "workshopPic" : "Ridwan",
  "workshopPicTitle" : "Manager",
  "workshopPicHandphone" : "08123412334",
  "isActive" : true,
  "isSupplier" : true,
  "isFeeSystem" : true,
  "feeSystemValue" : 100,
  "isOnline" : true,
  "onlineDate" : "2015-06-02",
  "accountNumber" : "1234567880",
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
}
```

### HTTP Request

`GET http://localhost:8080/api/workshops/{workshopId}`

### URL Parameters

Parameter | Description | Format
--------- | ----------- | ---------
workshopId | Workshop ID to retrieve | String