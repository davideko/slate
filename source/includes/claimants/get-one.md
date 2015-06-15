
## Get a Specific Claimant
This endpoint retrieves specific claimant.

> Sample request

```shell
  curl "http://localhost:8080/api/claimants/0bf56d35-1dc2-4826-a6e0-9e67397c6283"
  -H "Authorization: Bearer <token>"
```

> Success response

```json
{
  "claimantName" : "Nico Natalie",
  "claimantAddress" : "Tanjung Duren",
  "claimantPhone" : "123456",
  "claimantFax" : "123456",
  "claimantHandphone" : "123456",
  "claimantEmail" : "asd@asd.com",
    "_links" : {
      "self" : {
        "href" : "http://localhost:8080/api/claimants/0bf56d35-1dc2-4826-a6e0-9e67397c6283{?projection}",
        "templated" : true
      },
      "relation" : {
        "href" : "http://localhost:8080/api/relations/1"
      }
    }
}
```

### HTTP Request

`GET http://localhost:8080/api/claimants/{claimantId}`

### URL Parameters

Parameter | Description | Format
--------- | ----------- | ---------
claimantId | Claimant ID to retrieve | string