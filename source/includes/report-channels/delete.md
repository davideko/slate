## Delete Report Channel
This endpoint delete report channel by ID.

> Sample request

```shell
  curl "http://localhost:8080/api/report-channels/1"
  -X DELETE
  -H "Authorization: Bearer <token>"
```

> Success response <code>HTTP 204 No Content</code>

### HTTP Request

`DELETE http://localhost:8080/api/report-channels/{reportChannelId}`

### URL Parameters

Parameter | Description | Format
--------- | ----------- | ---------
reportChannelId | Report channel ID to update | String