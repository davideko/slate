## Update Report Channel
This endpoint update report channel by ID.

> Sample request PUT

```shell
  curl "http://localhost:8080/api/report-channels/1"
  -X PUT
  -H "Authorization: Bearer <token>"
  -d '{
    "reportChannelType": "HOTLINE GSM"
  }'
```

> Sample request PATCH

```shell
  curl "http://localhost:8080/api/report-channels/1"
  -X PATCH
  -H "Authorization: Bearer <token>"
  -d '{
    "reportChannelType": "HOTLINE GSM"
  }'
```

> Success response

```json
{
  "reportChannelType" : "HOTLINE GSM",
  "_links" : {
    "self" : {
      "href" : "http://localhost:8080/api/report-channels/1"
    }
  }
}
```

### HTTP Request

`PUT http://localhost:8080/api/report-channels/{reportChannelId}`

`PATCH http://localhost:8080/api/report-channels/{reportChannelId}`

### URL Parameters

Parameter | Description | Format
--------- | ----------- | ---------
reportChannelId | Report channel ID to update | string

### Parameters

Parameter | Description | Format
--------- | ----------- | ---------
reportChannelType | New report channel type | string
