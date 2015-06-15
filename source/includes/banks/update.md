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

> Success response

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

Parameter | Description | Format
--------- | ----------- | ---------
bankId | Bank ID to update | integer

### Parameters

Parameter | Description | Format
--------- | ----------- | ---------
bankName | New bank name | string