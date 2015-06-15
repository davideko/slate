## Delete a Specific Survey
This endpoint delete survey object by <code>surveyId</code>

> Sample request 

```shell
curl "http://localhost:8080/api/surveys/1"
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

`DELETE http://localhost:8080/api/surveys/<surveyId>`

### URL Parameters

Parameter | Description
--------- | -----------
surveyId | Selected survey id