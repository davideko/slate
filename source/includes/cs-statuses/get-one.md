## Get a Specific Cs Status

This endpoint get cs status by <code>csStatusId</code>

> Sample request

```shell
curl "http://localhost:8080/api/cs-statuses/1"
  -H "Authorization: Bearer <token>"
```

> Success response

```json
{
    "csStatusType": "Junior",
    "_links": {
        "self": {
            "href": "http://localhost:8080/api/cs-statuses/1"
        }
    }
}
```

### HTTP Request

`GET http://localhost:8080/api/cs-statuses/{csStatusId}`

### URL Parameters

Parameter | Description
--------- | -----------
csStatusId | Selected cs status id
