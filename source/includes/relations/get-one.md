
## Get a Specific Relation
This endpoint retrieves specific relation.

> Sample request

```shell
  curl "http://localhost:8080/api/relations/1"
  -H "Authorization: Bearer <token>"
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

`GET http://localhost:8080/api/relations/{relationId}`

### URL Parameters

Parameter | Description | Format
--------- | ----------- | ---------
relationId | Relation ID to retrieve | string