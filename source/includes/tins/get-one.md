
## Get a Specific TIN
This endpoint retrieves specific TIN.

> Sample request

```shell
  curl "http://localhost:8080/api/tins/01.342.006.2-046.000"
  -H "Authorization: Bearer <token>"
```

> Sucessful response

```json
{
  "taxIdentificationName" : "ASURANSI UMUM BCA",
  "taxIdentificationAddress" : "GEDUNG WTC MANGGA 2 LT 3A BLOK CL003",
  "_links" : {
    "self" : {
      "href" : "http://localhost:8080/api/tins/01.342.006.2-046.000"
    }
  }
}
```

### HTTP Request

`GET http://localhost:8080/api/tins/{taxIdentificationNumber}`

### URL Parameters

Parameter | Description | Data Type
--------- | ----------- | ---------
taxIdentificationNumber | Tax identification number to retrieve | string