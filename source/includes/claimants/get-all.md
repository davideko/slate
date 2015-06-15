# Claimant

## Get All Claimant
This endpoint retrieves all claimants.

> Sample request

```shell
  curl "http://localhost:8080/api/claimants"
  -H "Authorization: Bearer <token>"
```

> Success response

```json
{
  "_embedded" : {
    "claimants" : [ {
      "claimantEmail" : "asd@asd.com",
      "claimantName" : "Nico Natalie",
      "claimantPhone" : "123456",
      "claimantFax" : "123456",
      "relation" : {
        "relationType" : "Owner"
      },
      "claimantId" : "0bf56d35-1dc2-4826-a6e0-9e67397c6283",
      "claimantAddress" : "Tanjung Duren",
      "claimantHandphone" : "123456",
      "_links" : {
        "self" : {
          "href" : "http://localhost:8080/api/claimants/0bf56d35-1dc2-4826-a6e0-9e67397c6283{?projection}",
          "templated" : true
        },
        "relation" : {
          "href" : "http://localhost:8080/api/relations/1"
        }
      }
    } ]
  }
}
```

### HTTP Request

`GET http://localhost:8080/api/claimants`

