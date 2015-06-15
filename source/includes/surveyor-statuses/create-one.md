## Add New Surveyor Status

This endpoint used to add new surveyor status

> Sample request

```shell
curl "http://localhost:8080/api/surveyor-statuses"
  -X POST
  -H "Authorization: Bearer <token>"
  -H "Content-Type: application/json"
  -d '{
        "surveyorStatusType":"Junior"
      }'
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

> Failed response

```json
{
  "error": "because"
}
```

### HTTP Request

`POST http://localhost:8080/api/surveyor-statuses`

### Parameters

Parameter | Description | Format 
--------- | ----------- | ------ 
surveyorStatusType | Fill with surveyor status type | String 