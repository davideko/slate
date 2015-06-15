# Report Channel

## Get All Report Channel
This endpoint retrieves all report channels.

> Sample request

```shell
  curl "http://localhost:8080/api/report-channels"
  -H "Authorization: Bearer <token>"
```

> Sucessful response

```json
{
  "_embedded" : {
    "reportChannels" : [ {
      "reportChannelType" : "HOTLINE CDMA",
      "_links" : {
        "self" : {
          "href" : "http://localhost:8080/api/report-channels/1"
        }
      }
    }, {
      "reportChannelType" : "HOTLINE GSM",
      "_links" : {
        "self" : {
          "href" : "http://localhost:8080/api/report-channels/2"
        }
      }
    }, {
      "reportChannelType" : "DEREK",
      "_links" : {
        "self" : {
          "href" : "http://localhost:8080/api/report-channels/3"
        }
      }
    } ]
  }
}
```

### HTTP Request

`GET http://localhost:8080/api/report-channels`
