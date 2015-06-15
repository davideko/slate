## Add New Insured

This endpoint used to add new insured

> Sample request

```shell
curl "http://localhost:8080/api/insureds"
  -X POST
  -H "Authorization: Bearer <token>"
  -H "Content-Type: application/json"
  -d '{
        "insuredName":"Joe West",
        "insuredAddress":"Bekasi",
        "insuredPhone":"0218861234",
        "insuredFax":"12345678",
        "insuredHandphone":"0855778899",
        "insuredEmail":"this@test.com"
      }'
```

> Success response

```json
{
    "insuredName": "Joe West",
    "insuredAddress": "Bekasi",
    "insuredPhone": "0218861234",
    "insuredFax": "12345678",
    "insuredHandphone": "0855778899",
    "insuredEmail": "this@test.com",
    "_links": {
        "self": {
            "href": "http://localhost:8080/api/insureds/f1466d54-d6bd-4718-9893-3fdba5bce606"
        }
    }
}
```

### HTTP Request

`POST http://localhost:8080/api/insureds`

### Parameters

Parameter | Description | Format
--------- | ----------- | ------
insuredName | Fill with insured name | String
insuredAddress | Fill with insured address | String
insuredPhone | Fill with insured phone | String
insuredFax | Fill with insured fax | String
insuredHandphone | Fill with insured handphone | String
insuredEmail | Fill with insured email | String