# Cs Statuses
## Get All Cs Statuses

This endpoint used to return all cs statuses

> Sample request

```shell
curl "http://localhost:8080/api/cs-statuses"
  -H "Authorization: Bearer <token>"
```

> Success response

```json
{
    "_embedded": {
        "csStatuss": [
            {
                "csStatusType": "Junior",
                "_links": {
                    "self": {
                        "href": "http://localhost:8080/api/cs-statuses/1"
                    }
                }
            },
            {
                "csStatusType": "Senior",
                "_links": {
                    "self": {
                        "href": "http://localhost:8080/api/cs-statuses/2"
                    }
                }
            }
        ]
    }
}
```

### HTTP Request 

`GET http://localhost:8080/api/cs-statuses`