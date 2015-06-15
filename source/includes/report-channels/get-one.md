
## Get a Specific Report Channel
This endpoint retrieves specific report channel.

> Sample request

```shell
  curl "http://localhost:8080/api/report-channels/1"
  -H "Authorization: Bearer <token>"
```

> Sucessful response

```json
{
  "reportChannelType" : "HOTLINE CDMA",
  "_links" : {
    "self" : {
      "href" : "http://localhost:8080/api/report-channels/1"
    }
  }
}
```

### HTTP Request

`GET http://localhost:8080/api/report-channels/{reportChannelId}`

### URL Parameters

Parameter | Description | Data Type
--------- | ----------- | ---------
reportChannelId | Report channel ID to retrieve | string