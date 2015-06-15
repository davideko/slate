
## Get a Specific City
This endpoint retrieves specific city.

> Sample request

```shell
  curl "http://localhost:8080/api/cities/1"
  -H "Authorization: Bearer <token>"
```

> Sucessful response

```json
{
  "cityName" : "JAKARTA",
  "_links" : {
    "self" : {
      "href" : "http://localhost:8080/api/cities/1"
    }
  }
}
```

### HTTP Request

`GET http://localhost:8080/api/cities/{cityId}`

### URL Parameters

Parameter | Description | Data Type
--------- | ----------- | ---------
cityId | City ID to retrieve | string