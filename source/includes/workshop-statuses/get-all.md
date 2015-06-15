# Workshop Statuses
## Get All Workshop Statuses

This endpoint used to return all workshop statuses

> Sample request

```shell
curl "http://localhost:8080/api/workshop-statuses"
  -H "Authorization: Bearer <token>"
```

> Success response

```json
{
    "_embedded": {
        "workshopStatuss": [
            {
                "workshopStatusType": "Partner",
                "_links": {
                    "self": {
                        "href": "http://localhost:8080/api/workshop-statuses/1"
                    }
                }
            },
            {
                "workshopStatusType": "Non Partner",
                "_links": {
                    "self": {
                        "href": "http://localhost:8080/api/workshop-statuses/2"
                    }
                }
            }
        ]
    }
}
```

### HTTP Request 

`GET http://localhost:8080/api/workshop-statuses`