## Update TIN
This endpoint will update TIN by tax identification number.

> Sample request PUT

```shell
  curl "http://localhost:8080/api/tins/01.342.006.2-046.000"
  -X PUT
  -H "Authorization: Bearer <token>"
  -d '{
    "taxIdentificationName" : "ASURANSI KHUSUS BCA",
    "taxIdentificationAddress" : "GEDUNG WTC MANGGA 2 LT 3A BLOK CL003"
  }'
```

> Sample request PATCH

```shell
  curl "http://localhost:8080/api/tins/01.342.006.2-046.000"
  -X PATCH
  -H "Authorization: Bearer <token>"
  -d '{
    "taxIdentificationName" : "ASURANSI KHUSUS BCA"
  }'
```

> Success response

```json
{
  "taxIdentificationName" : "ASURANSI KHUSUS BCA",
  "taxIdentificationAddress" : "GEDUNG WTC MANGGA 2 LT 3A BLOK CL003",
  "_links" : {
    "self" : {
      "href" : "http://localhost:8080/api/tins/01.342.006.2-046.000"
    }
  }
}
```

### HTTP Request

`PUT http://localhost:8080/api/tins/{taxIdentificatinNumber}`

`PATCH http://localhost:8080/api/tins/{taxIdentificatinNumber}`

### URL Parameters

Parameter | Description | Format
--------- | ----------- | ---------
taxIdentificatinNumber | Tax identification number to update | String

### Parameters

Parameter | Description | Format
--------- | ----------- | ---------
taxIdentificationName | New tax identification name | String
taxIdentificationAddress | New tax identification address | String