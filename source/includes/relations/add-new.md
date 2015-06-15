## Add New Relation
This endpoint will create new relation.

> Sample request

```shell
  curl "http://localhost:8080/api/relations"
  -X POST
  -H "Authorization: Bearer <token>"
  -d '{
    "relationType" : "Owner"
  }'
```

> Sucessful response

```json
{
  "relationType" : "Owner",
  "_links" : {
    "self" : {
      "href" : "http://localhost:8080/api/relations/1"
    }
  }
}
```

### HTTP Request

`POST http://localhost:8080/api/relations`

###  Parameters

Parameter | Description | Data Type
--------- | ----------- | ---------
relationType | New relation type | string
