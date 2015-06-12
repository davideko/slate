## Get a Specific Insured

This endpoint get insured by <code>insuredId</code>

> Sample request

```shell
curl "http://localhost:8080/api/insureds/00e227f3-5469-4e3d-ad7a-4c79833358e4"
  -H "Authorization: Bearer <token>"
```

> Success response

```json
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
}
```

> Failed response

```json
{
  "error": "because"
}
```

### HTTP Request

`GET http://localhost:8080/api/insureds/<insuredId>`

### URL Parameters

Parameter | Description
--------- | -----------
insuredId | Selected insured id
