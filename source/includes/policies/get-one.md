## Get a Specific Policy

This endpoint get policy by <code>policyNumber</code>

> Sample request

```shell
curl "http://localhost:8080/api/policies/2b46fc11-8f45-43ac-a305-fbe1be4b7dae"
  -H "Authorization: Bearer <token>"
```

> Success response

```json
{
    "policyBeginningDate": "2015-06-03",
    "policyExpiryDate": "2017-06-03",
    "_links": {
        "self": {
            "href": "http://localhost:8080/api/policies/2b46fc11-8f45-43ac-a305-fbe1be4b7dae{?projection}",
            "templated": true
        },
        "insured": {
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

`GET http://localhost:8080/api/policies/<policyNumber>`

### URL Parameters

Parameter | Description
--------- | -----------
policyNumber | Selected policy number