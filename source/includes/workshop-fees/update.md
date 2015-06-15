## Update Workshop Fee
This endpoint will update workshop fee by ID.

> Sample request PUT

```shell
  curl "http://localhost:8080/api/workshop-fees/EDFFF909-64AA-4A7B-807E-77A7875F805C"
  -X PUT
  -H "Authorization: Bearer <token>"
  -d '{
    "pph23" : 5,
    "sparePartServicePercentage" : 80,
    "sparePartPpn" : 15,
    "sparePartPercentage" : 10,
    "sparePartDiscount" : 10,
    "servicePpn" : 70,
    "servicePercentage" : 20,
    "serviceDiscount" : 10,
    "salvageDiscount" : 5,
    "isTaxIncluded" : true
  }'
```

> Sample request PATCH

```shell
  curl "http://localhost:8080/api/workshop-fees/EDFFF909-64AA-4A7B-807E-77A7875F805C"
  -X PATCH
  -H "Authorization: Bearer <token>"
  -d '{
    "pph23" : 5
  }'
```

> Success response

```json
{
  "pph23" : 5,
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
}
```

### HTTP Request

`PUT http://localhost:8080/api/workshop-fees/{workshopFeeId}`

`PATCH http://localhost:8080/api/workshop-fees/{workshopFeeId}`

### URL Parameters

Parameter | Description | Format
--------- | ----------- | ---------
workshopFeeId | Workshop fee ID to update | String

### Parameters

Parameter | Description | Format
--------- | ----------- | ---------
pph23 | New pph23 | integer,
sparePartServicePercentage | New sparepart service percentage | integer
sparePartPpn | New sparepart ppn | integer
sparePartPercentage | New sparepart percentage | integer
sparePartDiscount | New sparepart discount | integer
servicePpn | New service ppn | integer
servicePercentage | New service percentage | integer
serviceDiscount | New service discount | integer
salvageDiscount | New salvage discount | integer
isTaxIncluded | Is tax included? | boolean