## Update Survey

This endpoint used to update a survey object. It can update using <code>PUT</code> for full update or <code>PATCH</code> for partial update

> Sample request PUT

```shell
curl "http://localhost:8080/api/surveys/2616d6a1-c267-4032-899d-83531665b846"
  -X PUT
  -H "Authorization: Bearer <token>"
  -H "Content-Type: application/json"
  -d '{
        "surveyAddress":"Kebon Jeruk",
        "surveyDate":"2015-06-15",
        "pendingCausal":"Laporan belum lengkap"
      }'
```

> Sample request PATCH

```shell
curl "http://localhost:8080/api/surveys/2616d6a1-c267-4032-899d-83531665b846"
  -X PATCH
  -H "Authorization: Bearer <token>"
  -H "Content-Type: application/json"
  -d '{
        "surveyAddress":"Kebon Jeruk"
      }'
```

> Success response

```json
{
    "surveyAddress": "Kebon Jeruk",
    "surveyDate": "2015-06-15",
    "pendingCausal": "Laporan belum lengkap",
    "_links": {
        "self": {
            "href": "http://localhost:8080/api/surveys/2616d6a1-c267-4032-899d-83531665b846"
        }
    }
}
```

### HTTP Request

`PUT http://localhost:8080/api/surveys/{surveyId}`

`PATCH http://localhost:8080/api/surveys/{surveyId}`

### URL Parameters

Parameter | Description
--------- | -----------
surveyId | Selected survey id

### Parameters

Parameter | Description | Format 
--------- | ----------- | ------ 
surveyAddress | Fill with survey address | String
surveyDate | Fill with survey date | String (date/datetime)
pendingCausal | Fill with pending causal | String 