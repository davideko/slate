## Get a Specific Survey

This endpoint get survey by <code>surveyId</code>

> Sample request

```shell
curl "http://localhost:8080/api/surveys/2616d6a1-c267-4032-899d-83531665b846"
  -H "Authorization: Bearer <token>"
```

> Success response

```json
{
    "surveyAddress": "Slipi",
    "surveyDate": "2015-06-15",
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

`GET http://localhost:8080/api/surveys/<surveyId>`

### URL Parameters

Parameter | Description
--------- | -----------
surveyId | Selected survey id
