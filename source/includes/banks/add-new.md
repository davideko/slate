## Add New Bank
This endpoint will create new bank.

> Sample request

```shell
  curl "http://localhost:8080/api/banks"
  -X POST
  -H "Authorization: Bearer <token>"
  -d '{
    "bankName" : "BANK DJARUM"
  }'
```

> Success response

```json
{
  "bankName" : "BANK DJARUM",
  "_links" : {
    "self" : {
      "href" : "http://localhost:8080/api/banks/1"
    }
  }
}
```

### HTTP Request

`POST http://localhost:8080/api/banks`

###  Parameters

Parameter | Description | Format
--------- | ----------- | ---------
bankName | New bank name | String
