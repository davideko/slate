## Add New TPL
This endpoint will create new TPL.

> Sample request

```shell
  curl "http://localhost:8080/api/tpls"
  -X POST
  -H "Authorization: Bearer <token>"
  -d '{
    "tplName" : "Rejaaa",
    "tplAddress" : "Gadingssss",
    "tplPhone" : "12345",
    "tplPlateNumber" : "B 1234 BIT",
    "tplMake" : "Toyotaaa",
    "tplDamage" : "Baret coyyy",
    "tplValue" : 2000000,
    "tplCategory" : "http://localhost:8080/api/tpl-categories/1"
  }'
```

> Success response

```json
{
  "tplName" : "Rejaaa",
  "tplAddress" : "Gadingssss",
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

`POST http://localhost:8080/api/tpls`

###  Parameters

Parameter | Description | Format
--------- | ----------- | ---------
tplName | New tpl name | String
tplAddress | New tpl address | String
tplPhone | New tpl phone | String
tplPlateNumber | New tpl plate number | String
tplMake | New tpl make | String
tplDamage | New tpl damage | String
tplValue | New tpl value | integer
tplCategory | Tpl Category object url | String