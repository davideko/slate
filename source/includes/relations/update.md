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

> Success response

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

Parameter | Description | Format
--------- | ----------- | ---------
relationId | Relation ID to update | string

### Parameters

Parameter | Description | Format
--------- | ----------- | ---------
relationType | New relation type | string