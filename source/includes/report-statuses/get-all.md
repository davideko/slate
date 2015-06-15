# Report Statuses
## Get All Report Statuses

This endpoint used to return all report statuses

> Sample request

```shell
curl "http://localhost:8080/api/report-statuses"
  -H "Authorization: Bearer <token>"
```

> Success response

```json
{
    "_embedded": {
        "reportStatuss": [
            {
                "reportStatusType": "Pending",
                "_links": {
                    "self": {
                        "href": "http://localhost:8080/api/report-statuses/1"
                    }
                }
            },
            {
                "reportStatusType": "Approved",
                "_links": {
                    "self": {
                        "href": "http://localhost:8080/api/report-statuses/2"
                    }
                }
            }
        ]
    }
}
```

### HTTP Request 

`GET http://localhost:8080/api/report-statuses`