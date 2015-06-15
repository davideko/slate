## Add New Survey

This endpoint used to add new survey

> Sample request

```shell
curl "http://localhost:8080/api/surveys"
  -X POST
  -H "Authorization: Bearer <token>"
  -H "Content-Type: application/json"
  -d '{
        "surveyAddress":"Slipi",
        "surveyDate":"2015-06-15",
        "pendingCausal":"Laporan belum lengkap"
      }'
```

> Success response

```json
{
    "surveyAddress": "Slipi",
    "surveyDate": "2015-06-15T00:00:00.000+0000",
    "pendingCausal": "Laporan belum lengkap",
    "_links": {
        "self": {
            "href": "http://localhost:8080/api/surveys/2616d6a1-c267-4032-899d-83531665b846"
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

`POST http://localhost:8080/api/surveys`

### Parameters

Parameter | Description | Format 
--------- | ----------- | ------ 
surveyAddress | Fill with survey address | String
surveyDate | Fill with survey date | String (date)
pendingCausal | Fill with pending causal | String 