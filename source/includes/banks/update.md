## Update Bank
This endpoint will update bank by ID.

> Sample request PUT

```shell
  curl "http://localhost:8080/api/banks/1"
  -X PUT
  -H "Authorization: Bearer <token>"
  -d '{
    "bankName" : "BANK DJARUM"
  }'
```

> Sample request PATCH

```shell
  curl "http://localhost:8080/api/banks/1"
  -X PATCH
  -H "Authorization: Bearer <token>"
  -d '{
    "bankName" : "BANK DJARUM"
  }'
```

> Sucessful response

```json
{
  "bankName" : "BANK DJARUM",
  "_links" : {
    "self" : {
      "href" : "http://localhost:8080/api/banks/1"
    }
  }
}
```

### HTTP Request

`PUT http://localhost:8080/api/banks/{bankId}`

`PATCH http://localhost:8080/api/banks/{bankId}`

### URL Parameters

Parameter | Description | Data Type
--------- | ----------- | ---------
bankId | Bank ID to update | integer

### Parameters

Parameter | Description | Data Type
--------- | ----------- | ---------
bankName | New bank name | string