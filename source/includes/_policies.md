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
    "_links": {
        "search": {
            "href": "http://localhost:8080/api/policies/search"
        }
    },
      "_embedded": {
          "policies": [
              {
                  "insured": {
                      "insuredName": "Ddddd",
                      "insuredAddress": "Galaxy",
                      "insuredPhone": "1111111",
                      "insuredFax": "12345678",
                      "insuredHandphone": "08888888",
                      "insuredEmail": "test@coba.com"
                  },
                  "policyNumber": "2b46fc11-8f45-43ac-a305-fbe1be4b7dae",
                  "policyExpiryDate": "2017-06-03",
                  "policyBeginningDate": "2015-06-03",
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

## Get a Specific Policy

This endpoint get policy by <code>policyNumber</code>

> Sample request

```shell
curl "http://localhost:8080/api/policies/<policyNumber>"
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

> Failed response

```json
{
  "error": "because"
}
```

### HTTP Request

`POST http://localhost:8080/api/policies`

### Parameters

Parameter | Description
--------- | -----------
policyBeginningDate | Fill with policy beginning date
policyExpiryDate | Fill with policy expiry date
insured | Fill with insured object url id

## Update Policy

This endpoint used to update a policy object. It can update using <code>PUT</code> for full update or <code>PATCH</code> for partial update

> Sample request PUT

```shell
curl "http://localhost:8080/api/policies/<policyNumber>"
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
curl "http://localhost:8080/api/policies/<policyNumber>"
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
      "href": "http://localhost:8080/api/policies/9e78484f-8f79-4124-867c-9f3c079a7522{?projection}",
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

Parameter | Description
--------- | -----------
policyBeginningDate | Fill with policy beginning date
policyExpiryDate | Fill with policy expiry date
insured | Fill with insured object url id

## Delete a Specific Policy

This endpoint delete insured object by <code>policyNumber</code>

> Sample request 

```shell
curl "http://localhost:8080/api/policies/<policyNumber>"
  -X DELETE
  -H "Authorization: Bearer <token>"
```

> Success response

```json
  {
    "message":"deleted"
  }
```

> Failed response

```json
  {
    "error": "because"
  }
```

### HTTP Request

`DELETE http://localhost:8080/api/policies/<policyNumber>`

### URL Parameters

Parameter | Description
--------- | -----------
policyNumber | Selected policy number