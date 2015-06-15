## Delete Relation
This endpoint will delete relation by ID.

> Sample request

```shell
  curl "http://localhost:8080/api/relations/1"
  -X DELETE
  -H "Authorization: Bearer <token>"
```

> Success response <code>HTTP 204 No Content</code>

### HTTP Request

`DELETE http://localhost:8080/api/relation/{relationId}`

### URL Parameters

Parameter | Description | Format
--------- | ----------- | ---------
relationId | Relation ID to delete | String