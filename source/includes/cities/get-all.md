# Cities

## Get All City
This endpoint retrieves all city.

> Sample request

```shell
  curl "http://localhost:8080/api/cities"
  -H "Authorization: Bearer <token>"
```

> Success response

```json
{
  "_embedded" : {
    "cities" : [ {
      "cityName" : "JAKARTA",
      "_links" : {
        "self" : {
          "href" : "http://localhost:8080/api/cities/1"
        }
      }
    }, {
      "cityName" : "BANDUNG",
      "_links" : {
        "self" : {
          "href" : "http://localhost:8080/api/cities/2"
        }
      }
    } ]
  }
}
```

### HTTP Request

`GET http://localhost:8080/api/cities`

