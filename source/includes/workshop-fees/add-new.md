## Add New Workshop Fee
This endpoint will create new workshop fee.

> Sample request

```shell
  curl "http://localhost:8080/api/workshop-categories"
  -X POST
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

> Sucessful response

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

`POST http://localhost:8080/api/`

###  Parameters

Parameter | Description | Data Type
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
