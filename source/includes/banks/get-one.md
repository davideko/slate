
## Get a Specific Bank
This endpoint retrieves specific bank.

> Sample request

```shell
  curl "http://localhost:8080/api/banks/1"
  -H "Authorization: Bearer <token>"
```

> Sucessful response

```json
{
  "bankName" : "BANK CENTRAL ASIA",
  "_links" : {
    "self" : {
      "href" : "http://localhost:8080/api/banks/1"
    }
  }
}
```

### HTTP Request

`GET http://localhost:8080/api/banks/{bankId}`

### URL Parameters

Parameter | Description | Data Type
--------- | ----------- | ---------
bankId | Bank ID to retrieve | string