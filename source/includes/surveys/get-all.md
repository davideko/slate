# Surveys
## Get All Surveys

This endpoint used to return all surveys

> Sample request

```shell
curl "http://localhost:8080/api/surveys"
  -H "Authorization: Bearer <token>"
```

> Success response

```json
{
    "_embedded": {
        "surveys": [
            {
                "surveyAddress": "Slipi",
                "surveyDate": "2015-06-15",
                "pendingCausal": "Laporan belum lengkap",
                "_links": {
                    "self": {
                        "href": "http://localhost:8080/api/surveys/2616d6a1-c267-4032-899d-83531665b846"
                    }
                }
            },
            {
                "surveyAddress": "Kemanggisan",
                "surveyDate": "2015-06-09",
                "pendingCausal": "None",
                "_links": {
                    "self": {
                        "href": "http://localhost:8080/api/surveys/d5c1e5ae-9bf8-4b13-93d3-947fd74ba24d"
                    }
                }
            }
        ]
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

`GET http://localhost:8080/api/surveys`