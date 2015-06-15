## Add New TIN
This endpoint will create new TIN.

> Sample request

```shell
  curl "http://localhost:8080/api/tins"
  -X POST
  -H "Authorization: Bearer <token>"
  -d '{
    "taxIdentificationNumber" : "01.342.006.2-046.000",
    "taxIdentificationName" : "ASURANSI UMUM BCA",
    "taxIdentificationAddress" : "GEDUNG WTC MANGGA 2 LT 3A BLOK CL003"
  }'
```

> Success response

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

`POST http://localhost:8080/api/tins`

###  Parameters

Parameter | Description | Format
--------- | ----------- | ---------
taxIdentificationNumber | New tax identification number | String
taxIdentificationName | New tax identification name | String
taxIdentificationAddress | New tax identification address | String
