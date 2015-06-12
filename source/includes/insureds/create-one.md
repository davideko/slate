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

> Failed response

```json
{
  "error": "because"
}
```

### HTTP Request

`POST http://localhost:8080/api/insureds`

### Parameters

Parameter | Description
--------- | -----------
insuredName | Fill with insured name
insuredAddress | Fill with insured address
insuredPhone | Fill with insured phone
insuredFax | Fill with insured fax
insuredHandphone | Fill with insured handphone
insuredEmail | Fill with insured email