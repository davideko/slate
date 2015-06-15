# Bank

## Get All Banks
This endpoint retrieves all bank.

> Sample request

```shell
  curl "http://localhost:8080/api/banks"
  -H "Authorization: Bearer <token>"
```

> Success response

```json
{
  "_embedded" : {
    "banks" : [ {
      "bankName" : "BANK CENTRAL ASIA",
      "_links" : {
        "self" : {
          "href" : "http://localhost:8080/api/banks/1"
        }
      }
    }, {
      "bankName" : "BANK MANDIRI",
      "_links" : {
        "self" : {
          "href" : "http://localhost:8080/api/banks/2"
        }
      }
    }, {
      "bankName" : "BANK INDONESIA",
      "_links" : {
        "self" : {
          "href" : "http://localhost:8080/api/banks/3"
        }
      }
    } ]
  }
}
```

### HTTP Request

`GET http://localhost:8080/api/banks`

