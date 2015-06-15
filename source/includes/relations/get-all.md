# Relation

## Get All Relation 
This endpoint retrieves all relations.

> Sample request

```shell
  curl "http://localhost:8080/api/relations"
  -H "Authorization: Bearer <token>"
```

> Success response

```json
{
  "_embedded" : {
    "relations" : [ {
      "relationType" : "Owner",
      "_links" : {
        "self" : {
          "href" : "http://localhost:8080/api/relations/1"
        }
      }
    }, {
      "relationType" : "Family",
      "_links" : {
        "self" : {
          "href" : "http://localhost:8080/api/relations/3"
        }
      }
    } ]
  }
}
```

### HTTP Request

`GET http://localhost:8080/api/relations`

