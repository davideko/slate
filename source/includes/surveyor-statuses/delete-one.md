## Delete a Specific Surveyor Status
This endpoint delete surveyor status object by <code>surveyorStatusId</code>

> Sample request 

```shell
curl "http://localhost:8080/api/surveyor-statuses/1"
  -X DELETE
  -H "Authorization: Bearer <token>"
```

> Success response

```json
{
  "message":"deleted"
}
```

> Failed response

```json
{
  "error": "because"
}
```

### HTTP Request

`DELETE http://localhost:8080/api/surveyor-statuses/<surveyorStatusId>`

### URL Parameters

Parameter | Description
--------- | -----------
surveyorStatusId | Selected surveyor status id