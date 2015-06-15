## Get a Specific Workshop Status

This endpoint get workshop status by <code>workshopStatusId</code>

> Sample request

```shell
curl "http://localhost:8080/api/workshop-statuses/1"
  -H "Authorization: Bearer <token>"
```

> Success response

```json
{
    "workshopStatusType": "Partner",
    "_links": {
        "self": {
            "href": "http://localhost:8080/api/workshop-statuses/1"
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

`GET http://localhost:8080/api/workshop-statuses/<workshopStatusId>`

### URL Parameters

Parameter | Description
--------- | -----------
workshopStatusId | Selected workshop status id
