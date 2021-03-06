# Workshop Fees

## Get All Wokrshop Fee
This endpoint retrieves all workshop fees.

> Sample request

```shell
  curl "http://localhost:8080/api/workshop-fees"
  -H "Authorization: Bearer <token>"
```

> Success response

```json
{
  "_embedded" : {
    "workshopFees" : [ {
      "pph23" : 2,
      "sparePartServicePercentage" : 80,
      "sparePartPpn" : 15,
      "sparePartPercentage" : 10,
      "sparePartDiscount" : 10,
      "servicePpn" : 70,
      "servicePercentage" : 20,
      "serviceDiscount" : 10,
      "salvageDiscount" : 5,
      "isTaxIncluded" : true,
      "_links" : {
        "self" : {
          "href" : "http://localhost:8080/api/workshop-fees/EDFFF909-64AA-4A7B-807E-77A7875F805C"
        }
      }
    } ]
  }
}
```

### HTTP Request

`GET http://localhost:8080/api/workshop-fees`

