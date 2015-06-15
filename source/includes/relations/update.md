## Update Relation
This endpoint will update Relation by ID.

> Sample request PUT

```shell
  curl "http://localhost:8080/api/relations"
  -X PUT
  -H "Authorization: Bearer <token>"
  -d '{
    "relationType" : "Owner"
  }'
```

> Sample request PATCH

```shell
  curl "http://localhost:8080/api/relations"
  -X PATCH
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

`PUT http://localhost:8080/api/relations/{relationId}`

`PATCH http://localhost:8080/api/relations/{relationId}`

### URL Parameters

Parameter | Description | Data Type
--------- | ----------- | ---------
relationId | Relation ID to update | string

### Parameters

Parameter | Description | Data Type
--------- | ----------- | ---------
relationType | New relation type | string