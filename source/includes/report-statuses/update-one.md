## Update Report Status

This endpoint used to update a report status object. It can update using <code>PUT</code> for full update or <code>PATCH</code> for partial update

> Sample request PUT

```shell
curl "http://localhost:8080/api/report-statuses/1"
  -X PUT
  -H "Authorization: Bearer <token>"
  -H "Content-Type: application/json"
  -d '{
        "reportStatusType":"Temporary"
      }'
```

> Sample request PATCH

```shell
curl "http://localhost:8080/api/report-statuses/1"
  -X PATCH
  -H "Authorization: Bearer <token>"
  -H "Content-Type: application/json"
  -d '{
        "reportStatusType":"Temporary"
      }'
```

> Success response

```json
{
    "reportStatusType": "Temporary",
    "_links": {
        "self": {
            "href": "http://localhost:8080/api/report-statuses/1"
        }
    }
}
```

### HTTP Request

`PUT http://localhost:8080/api/report-statuses/{reportStatusId}`

`PATCH http://localhost:8080/api/report-statuses/{reportStatusId}`

### URL Parameters

Parameter | Description
--------- | -----------
reportStatusId | Selected report status id

### Parameters

Parameter | Description | Format 
--------- | ----------- | ------ 
reportStatusType | Fill with report status type | String