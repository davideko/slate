# Insureds
## Get All Insureds

This endpoint used to return all insureds

> Sample request

```shell
curl "http://localhost:8080/api/insureds"
  -H "Authorization: Bearer <token>"
```

> Success response

```json
{
    "_embedded": {
        "insureds": [
            {
                "insuredName": "Star Lord",
                "insuredAddress": "Galaxy",
                "insuredPhone": "0218875645",
                "insuredFax": "56789844",
                "insuredHandphone": "0888888811",
                "insuredEmail": "test@this.com",
                "_links": {
                    "self": {
                        "href": "http://localhost:8080/api/insureds/00e227f3-5469-4e3d-ad7a-4c79833358e4"
                    }
                }
            },
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
        ]
    }
}
```

### HTTP Request 

`GET http://localhost:8080/api/insureds`