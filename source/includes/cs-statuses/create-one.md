## Add New Cs Status

This endpoint used to add new cs status

> Sample request

```shell
curl "http://localhost:8080/api/cs-statuses"
  -X POST
  -H "Authorization: Bearer <token>"
  -H "Content-Type: application/json"
  -d '{
        "csStatusType":"Junior"
      }'
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

> Failed response

```json
{
  "error": "because"
}
```

### HTTP Request

`POST http://localhost:8080/api/cs-statuses`

### Parameters

Parameter | Description | Format 
--------- | ----------- | ------ 
csStatusType | Fill with cs status type | String 