## Add New City
This endpoint will create new city.

> Sample request

```shell
  curl "http://localhost:8080/api/cities"
  -X POST
  -H "Authorization: Bearer <token>"
  -d '{
    "cityName" : "JAKARTA"
  }'
```

> Success response

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

`POST http://localhost:8080/api/cities`

###  Parameters

Parameter | Description | Format
--------- | ----------- | ---------
cityName | New city name | String
