## Add New Report Status

This endpoint used to add new report status

> Sample request

```shell
curl "http://localhost:8080/api/report-statuses"
  -X POST
  -H "Authorization: Bearer <token>"
  -H "Content-Type: application/json"
  -d '{
        "reportStatusType":"Pending"
      }'
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

`POST http://localhost:8080/api/report-statuses`

### Parameters

Parameter | Description | Format 
--------- | ----------- | ------ 
reportStatusType | Fill with report status type | String 