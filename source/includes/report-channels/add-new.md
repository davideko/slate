## Add New Report Channel
This endpoint will create new report channel.

> Sample request

```shell
  curl "http://localhost:8080/api/report-channels"
  -X POST
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
        "href" : "http://localhost:8080/api/report-channels/4"
      }
    }
}
```

### HTTP Request

`POST http://localhost:8080/api/report-channels`

###  Parameters

Parameter | Description | Format
--------- | ----------- | ---------
reportChannelType | New report channel type | String
