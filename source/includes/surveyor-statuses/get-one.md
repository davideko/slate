## Get a Specific Surveyor Status

This endpoint get surveyor status by <code>surveyorStatusId</code>

> Sample request

```shell
curl "http://localhost:8080/api/surveyor-statuses/1"
  -H "Authorization: Bearer <token>"
```

> Success response

```json
{
    "surveyorStatusType": "Junior",
    "_links": {
        "self": {
            "href": "http://localhost:8080/api/surveyor-statuses/1"
        }
    }
}
```

### HTTP Request

`GET http://localhost:8080/api/surveyor-statuses/<surveyorStatusId>`

### URL Parameters

Parameter | Description
--------- | -----------
surveyorStatusId | Selected surveyor status id
