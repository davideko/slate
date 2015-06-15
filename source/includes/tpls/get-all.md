# TPL

## Get All TPL
This endpoint retrieves all TPLs.

> Sample request

```shell
  curl "http://localhost:8080/api/tpls"
  -H "Authorization: Bearer <token>"
```

> Sucessful response

```json
{
  "_embedded" : {
    "tpls" : [ {
      "tplPhone" : "12345",
      "tplDamage" : "Baret coyyy",
      "tplMake" : "Toyotaaa",
      "tplName" : "Rejaaa",
      "tplValue" : 2000000.00,
      "tplAddress" : "Gadingssss",
      "tplPlateNumber" : "B 1234 BIT",
      "tplCategory" : {
        "tplCategoryType" : "Car"
      },
      "tplId" : "1acf6d4e-ef99-4561-9615-ad444105ff21",
        "_links" : {
            "self" : {
              "href" : "http://localhost:8080/api/tpls/1acf6d4e-ef99-4561-9615-ad444105ff21{?projection}",
              "templated" : true
            },
            "tplCategory" : {
              "href" : "http://localhost:8080/api/tpl-categories/1"
            }
        }
    } ]
  }
}
```

### HTTP Request

`GET http://localhost:8080/api/tpls`

