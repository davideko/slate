## Update Surveyor Status

This endpoint used to update a surveyor status object. It can update using <code>PUT</code> for full update or <code>PATCH</code> for partial update

> Sample request PUT

```shell
curl "http://localhost:8080/api/surveyor-statuses/1"
  -X PUT
  -H "Authorization: Bearer <token>"
  -H "Content-Type: application/json"
  -d '{
        "surveyorStatusType":"New Junior"
      }'
```

> Sample request PATCH

```shell
curl "http://localhost:8080/api/surveyor-statuses/1"
  -X PATCH
  -H "Authorization: Bearer <token>"
  -H "Content-Type: application/json"
  -d '{
        "surveyorStatusType":"New Junior"
      }'
```

> Success response

```json
{
    "surveyorStatusType": "New Junior",
    "_links": {
        "self": {
            "href": "http://localhost:8080/api/surveyor-statuses/1"
        }
    }
}
```

### HTTP Request

`PUT http://localhost:8080/api/surveyor-statuses/<surveyorStatusId>`

`PATCH http://localhost:8080/api/surveyor-statuses/<surveyorStatusId>`

### URL Parameters

Parameter | Description
--------- | -----------
surveyorStatusId | Selected surveyor status id

### Parameters

Parameter | Description | Format 
--------- | ----------- | ------ 
surveyorStatusType | Fill with surveyor status type | String