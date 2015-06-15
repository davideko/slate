## Update Claimant
This endpoint will update claimant by ID.

> Sample request PUT

```shell
  curl "http://localhost:8080/api/claimants//0bf56d35-1dc2-4826-a6e0-9e67397c6283"
  -X PUT
  -H "Authorization: Bearer <token>"
  -d '{
    "claimantName" : "Nico Natalie",
    "claimantAddress" : "Tanjung Duren Selatan",
    "claimantPhone" : "123456",
    "claimantFax" : "123456",
    "claimantHandphone" : "123456",
    "claimantEmail" : "asd@asd.com",
    "relation" : "http://localhost:8080/api/relations/1"
  }'
```

> Sample request PATCH

```shell
  curl "http://localhost:8080/api/claimants//0bf56d35-1dc2-4826-a6e0-9e67397c6283"
  -X PATCH
  -H "Authorization: Bearer <token>"
  -d '{
    "claimantAddress" : "Tanjung Duren Selatan"
  }'
```

> Success response

```json
{
  "claimantName" : "Nico Natalie",
  "claimantAddress" : "Tanjung Duren Selatan",
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

`PUT http://localhost:8080/api/claimants/{claimantId}`

`PATCH http://localhost:8080/api/claimants/{claimantId}`

### URL Parameters

Parameter | Description | Format
--------- | ----------- | ---------
claimantId | Claimant ID to update | String

### Parameters

Parameter | Description | Format
--------- | ----------- | ---------
claimantName | New claimant name | String
claimantAddress | New claimant address | String
claimantPhone | New claimant phone | String
claimantFax | New claimant fax | String
claimantHandphone | New claimant handphone | String
claimantEmail | New claimant email | String
relation | Relation object url | String