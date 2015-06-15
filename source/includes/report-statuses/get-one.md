## Get a Specific Report Status

This endpoint get report status by <code>reportStatusId</code>

> Sample request

```shell
curl "http://localhost:8080/api/report-statuses/1"
  -H "Authorization: Bearer <token>"
```

> Success response

```json
{
    "reportStatusType": "Pending",
    "_links": {
        "self": {
            "href": "http://localhost:8080/api/report-statuses/1"
        }
    }
}
```

### HTTP Request

`GET http://localhost:8080/api/report-statuses/{reportStatusId}`

### URL Parameters

Parameter | Description
--------- | -----------
reportStatusId | Selected report status id
