# Policies
## Get All Policies

This endpoint used to return all policies
> Sample request

```shell
curl "http://localhost:8080/api/policies"
  -H "Authorization: Bearer <token>"
```

> Success response

```json
    {
        "_embedded": {
            "policies": [
                {
                    "policyExpiryDate": "2017-06-03",
                    "policyBeginningDate": "2015-06-03",
                    "policyNumber": "2b46fc11-8f45-43ac-a305-fbe1be4b7dae",
                    "insured": {
                        "insuredName": "Star Lord",
                        "insuredAddress": "Galaxy",
                        "insuredPhone": "0218875645",
                        "insuredFax": "56789844",
                        "insuredHandphone": "0888888811",
                        "insuredEmail": "test@this.com"
                    },
                    "_links": {
                        "self": {
                            "href": "http://localhost:8080/api/policies/2b46fc11-8f45-43ac-a305-fbe1be4b7dae{?projection}",
                            "templated": true
                        },
                        "insured": {
                            "href": "http://localhost:8080/api/insureds/00e227f3-5469-4e3d-ad7a-4c79833358e4"
                        }
                    }
                },
                {
                    "policyExpiryDate": "2017-10-03",
                    "policyBeginningDate": "2015-06-03",
                    "policyNumber": "5a0d5fdb-88c8-473b-a210-41afbd6263e2",
                    "insured": {
                        "insuredName": "Joe West",
                        "insuredAddress": "Bekasi",
                        "insuredPhone": "0218861234",
                        "insuredFax": "12345678",
                        "insuredHandphone": "0855778899",
                        "insuredEmail": "this@test.com"
                    },
                    "_links": {
                        "self": {
                            "href": "http://localhost:8080/api/policies/5a0d5fdb-88c8-473b-a210-41afbd6263e2{?projection}",
                            "templated": true
                        },
                        "insured": {
                            "href": "http://localhost:8080/api/insureds/f1466d54-d6bd-4718-9893-3fdba5bce606"
                        }
                    }
                }
            ]
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

`GET http://localhost:8080/api/policies`