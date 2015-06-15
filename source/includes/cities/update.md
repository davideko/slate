## Update City
This endpoint will update city by ID.

> Sample request PUT

```shell
  curl "http://localhost:8080/api/cities/1"
  -X PUT
  -H "Authorization: Bearer <token>"
  -d '{
    "cityName" : "DJAKARTA"
  }'
```

> Sample request PATCH

```shell
  curl "http://localhost:8080/api/cities/1"
  -X PATCH
  -H "Authorization: Bearer <token>"
  -d '{
    "cityName" : "DJAKARTA"
  }'
```

> Success response

```json
{
  "cityName" : "DJAKARTA",
  "_links" : {
    "self" : {
      "href" : "http://localhost:8080/api/cities/1"
    }
  }
}
```

### HTTP Request

`PUT http://localhost:8080/api/cities/{cityId}`

`PATCH http://localhost:8080/api/cities/{cityId}`

### URL Parameters

Parameter | Description | Format
--------- | ----------- | ---------
cityId | City ID to update | integer

### Parameters

Parameter | Description | Format
--------- | ----------- | ---------
cityName | New city name | String