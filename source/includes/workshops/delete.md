## Delete Workshop
This endpoint will delete workshop by ID.

> Sample request

```shell
  curl "http://localhost:8080/api/workshops/12a90304-e455-44d5-ada0-a4aa657f8416"
  -X DELETE
  -H "Authorization: Bearer <token>"
```

> Success response <code>HTTP 204 No Content</code>

### HTTP Request

`DELETE http://localhost:8080/api/workshops/{workshopId}`

### URL Parameters

Parameter | Description | Format
--------- | ----------- | ---------
workshopId | Workshop ID to delete | String