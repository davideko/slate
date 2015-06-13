## Update Insured

This endpoint used to update a insured object. It can update using <code>PUT</code> for full update or <code>PATCH</code> for partial update

> Sample request PUT

```shell
curl "http://localhost:8080/api/insureds/f1466d54-d6bd-4718-9893-3fdba5bce606"
  -X PUT
  -H "Authorization: Bearer <token>"
  -H "Content-Type: application/json"
  -d '{
        "insuredName":"Joe West",
        "insuredAddress":"Bandung",
        "insuredPhone":"0218861234",
        "insuredFax":"12345678",
        "insuredHandphone":"0855778899",
        "insuredEmail":"this@test.com"
      }'
```

> Sample request PATCH

```shell
curl "http://localhost:8080/api/insureds/f1466d54-d6bd-4718-9893-3fdba5bce606"
  -X PATCH
  -H "Authorization: Bearer <token>"
  -H "Content-Type: application/json"
  -d '{
        "insuredAddress":"Bandung"
      }'
```

> Success response

```json
{
    "insuredName": "Joe West",
    "insuredAddress": "Bandung",
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

`PUT http://localhost:8080/api/insureds/<insuredId>`

`PATCH http://localhost:8080/api/insureds/<insuredId>`

### URL Parameters

Parameter | Description
--------- | -----------
insuredId | Selected insured id

### Parameters

Parameter | Description
--------- | -----------
insuredName | Fill with insured name
insuredAddress | Fill with insured address
insuredPhone | Fill with insured phone
insuredFax | Fill with insured fax
insuredHandphone | Fill with insured handphone
insuredEmail | Fill with insured email