## Add New Policy

This endpoint used to add new policy

> Sample request

```shell
curl "http://localhost:8080/api/policies"
  -X POST
  -H "Authorization: Bearer <token>"
  -H "Content-Type: application/json"
  -d '{
        "policyBeginningDate":"2015-06-03",
        "policyExpiryDate":"2017-06-03",
        "insured":"http://localhost:8080/api/insureds/f3f5cc63-3c83-48ac-b05d-73ea882a3208"
      }'
```

> Success response

```json
{
    "policyBeginningDate": "2015-06-03T00:00:00.000+0000",
    "policyExpiryDate": "2017-06-03T00:00:00.000+0000",
    "_links": {
        "self": {
          "href": "http://localhost:8080/api/policies/9e78484f-8f79-4124-867c-9f3c079a7522{?projection}",
          "templated": true
        },
        "insured": {
          "href": "http://localhost:8080/api/insureds/00e227f3-5469-4e3d-ad7a-4c79833358e4"
        }
    }
}
```

### HTTP Request

`POST http://localhost:8080/api/policies`

### Parameters

Parameter | Description | Format
--------- | ----------- | ------
policyBeginningDate | Fill with policy beginning date | String (date)
policyExpiryDate | Fill with policy expiry date | String (date)
insured | Fill with insured object url id | String
