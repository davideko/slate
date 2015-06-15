
## Get a Specific TPL
This endpoint retrieves specific TPL.

> Sample request

```shell
  curl "http://localhost:8080/api/tpls/1acf6d4e-ef99-4561-9615-ad444105ff21"
  -H "Authorization: Bearer <token>"
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

`GET http://localhost:8080/api/tpls/{tplId}`

### URL Parameters

Parameter | Description | Format
--------- | ----------- | ---------
tplId | TPL ID to retrieve | string