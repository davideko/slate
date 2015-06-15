## Update Policy

This endpoint used to update a policy object. It can update using <code>PUT</code> for full update or <code>PATCH</code> for partial update

> Sample request PUT

```shell
curl "http://localhost:8080/api/policies/9e78484f-8f79-4124-867c-9f3c079a7522"
  -X PUT
  -H "Authorization: Bearer <token>"
  -H "Content-Type: application/json"
  -d '{
        "policyBeginningDate":"2015-06-03",
        "policyExpiryDate":"2020-06-03",
        "insured":"http://localhost:8080/api/insureds/f3f5cc63-3c83-48ac-b05d-73ea882a3208"
      }'
```

> Sample request PATCH

```shell
curl "http://localhost:8080/api/policies/9e78484f-8f79-4124-867c-9f3c079a7522"
  -X PATCH
  -H "Authorization: Bearer <token>"
  -H "Content-Type: application/json"
  -d '{
        "policyExpiryDate":"2020-06-03"
      }'
```

> Success response

```json
{
    "policyBeginningDate": "2015-06-03T00:00:00.000+0000",
    "policyExpiryDate": "2020-06-03T00:00:00.000+0000",
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

`PUT http://localhost:8080/api/policies/<policyNumber>`

`PATCH http://localhost:8080/api/policies/<policyNumber>`

### URL Parameters

Parameter | Description
--------- | -----------
policyNumber | Selected policy number

### Parameters

Parameter | Description | Format
--------- | ----------- | ------
policyBeginningDate | Fill with policy beginning date | String (date)
policyExpiryDate | Fill with policy expiry date | String (date)
insured | Fill with insured object url id | String