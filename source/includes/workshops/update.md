## Update Workshop
This endpoint will update workshop by ID.

> Sample request PUT

```shell
  curl "http://localhost:8080/api/workshops/12a90304-e455-44d5-ada0-a4aa657f8416"
  -X PUT
  -H "Authorization: Bearer <token>"
  -d '{
    "workshopName" : "OTO 3000",
    "workshopAddress" : "TANJUNG DUREN BARAT",
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
    "bank" :"http://localhost:8080/api/banks/1",
    "city" : "http://localhost:8080/api/cities/1",
    "tin" : "http://localhost:8080/api/tins/01.342.006.2-046.000",
    "workshopCategory" : "http://localhost:8080/api/workshop-categories/1",
    "workshopDetail" : "http://localhost:8080/api/workshop-details/4CFEADB9-EAF8-48A7-808A-0CF141A8B99D",
    "workshopFee" : "http://localhost:8080/api/workshop-fees/EDFFF909-64AA-4A7B-807E-77A7875F805C"
  }'
```

> Sample request PATCH

```shell
  curl "http://localhost:8080/api/workshops/12a90304-e455-44d5-ada0-a4aa657f8416"
  -X PATCH
  -H "Authorization: Bearer <token>"
  -d '{
    "workshopAddress" : "TANJUNG DUREN BARAT",
  }'
```

> Success response

```json
{
  "workshopName" : "OTO 3000",
  "workshopAddress" : "TANJUNG DUREN BARAT",
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
  "onlineDate" : "2015-06-02T00:00:00.000+0000",
  "accountNumber" : "1234567880",
  "_links" : {
    "self" : {
      "href" : "http://localhost:8080/api/workshops/12a90304-e455-44d5-ada0-a4aa657f8416{?projection}",
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

`PUT http://localhost:8080/api/workshops/{workshopId}`

`PATCH http://localhost:8080/api/workshops/{workshopId}`

### URL Parameters

Parameter | Description | Format
--------- | ----------- | ---------
workshopId | Workshop ID to update | String

### Parameters

Parameter | Description | Format
--------- | ----------- | ---------
workshopName | New workshop name | String
workshopAddress | New workshop address | String
workshopPhone | New workshop phone | String
workshopFax | New workshop fax | String
workshopEmail | New workshop email | String
workshopPic | New workshop pic | String
workshopPicTitle | New workshop pic title | String
workshopPicHandphone | New workshop pic handphone | String
isActive | true / false | boolean
isSupplier | true / false | boolean
feeSystemValue | New fee system value | integer
isOnline | true / false | boolean
onlineDate | New online date | datetime
accountNumber | New account number | String
bank | Bank object url | String
city | City object url | String
tin | Tin object url | String
workshopCategory | Workshop category object url | String
workshopDetail | Workshop detail object url | String
workshopFee | Workshop fee object url | String