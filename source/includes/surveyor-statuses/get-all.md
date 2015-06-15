# Surveyor Statuses
## Get All Surveyor Statuses

This endpoint used to return all surveyor statuses

> Sample request

```shell
curl "http://localhost:8080/api/surveyor-statuses"
  -H "Authorization: Bearer <token>"
```

> Success response

```json
{
    "_embedded": {
        "surveyorStatuss": [
            {
                "surveyorStatusType": "Junior",
                "_links": {
                    "self": {
                        "href": "http://localhost:8080/api/surveyor-statuses/1"
                    }
                }
            },
            {
                "surveyorStatusType": "Senior",
                "_links": {
                    "self": {
                        "href": "http://localhost:8080/api/surveyor-statuses/2"
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

`GET http://localhost:8080/api/surveyor-statuses`