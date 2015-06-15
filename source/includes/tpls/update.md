## Update TPL
This endpoint will update TPL by ID.

> Sample request PUT

```shell
  curl "http://localhost:8080/api/tpls"
  -X PUT
  -H "Authorization: Bearer <token>"
  -d '{
    "tplName" : "Rejaaa",
    "tplAddress" : "Gading",
    "tplPhone" : "12345",
    "tplPlateNumber" : "B 1234 BIT",
    "tplMake" : "Toyotaaa",
    "tplDamage" : "Baret coyyy",
    "tplValue" : 2000000,
    "tplCategory" : "http://localhost:8080/api/tpl-categories/1"
  }'
```

> Sample request PATCH

```shell
  curl "http://localhost:8080/api/tpls/59fdeded-fc94-45f4-b0bd-6a788d0fc375"
  -X PATCH
  -H "Authorization: Bearer <token>"
  -d '{
    "tplAddress" : "Gading",
  }'
```

> Success response

```json
{
  "tplName" : "Rejaaa",
  "tplAddress" : "Gading",
  "tplPhone" : "12345",
  "tplPlateNumber" : "B 1234 BIT",
  "tplMake" : "Toyotaaa",
  "tplDamage" : "Baret coyyy",
  "tplValue" : 2000000.00,
  "_links" : {
    "self" : {
      "href" : "http://localhost:8080/api/tpls/1acf6d4e-ef99-4561-9615-ad444105ff21{?projection}",
      "templated" : true
    },
    "tplCategory" : {
      "href" : "http://localhost:8080/api/tpl-categories/1"
    }
  }
}
```

### HTTP Request

`PUT http://localhost:8080/api/tpls/{tplId}`

`PATCH http://localhost:8080/api/tpls/{tplId}`

### URL Parameters

Parameter | Description | Format
--------- | ----------- | ---------
tplId | TPL id to update | string

### Parameters

Parameter | Description | Format
--------- | ----------- | ---------
tplName | New tpl name | string
tplAddress | New tpl address | string
tplPhone | New tpl phone | string
tplPlateNumber | New tpl plate number | string
tplMake | New tpl make | string
tplDamage | New tpl damage | string
tplValue | New tpl value | integer
tplCategory | Tpl Category object url | string