## Update Cs Status

This endpoint used to update a cs status object. It can update using <code>PUT</code> for full update or <code>PATCH</code> for partial update

> Sample request PUT

```shell
curl "http://localhost:8080/api/cs-statuses/1"
  -X PUT
  -H "Authorization: Bearer <token>"
  -H "Content-Type: application/json"
  -d '{
        "csStatusType":"New Junior"
      }'
```

> Sample request PATCH

```shell
curl "http://localhost:8080/api/cs-statuses/1"
  -X PATCH
  -H "Authorization: Bearer <token>"
  -H "Content-Type: application/json"
  -d '{
        "csStatusType":"New Junior"
      }'
```

> Success response

```json
{
    "csStatusType": "New Junior",
    "_links": {
        "self": {
            "href": "http://localhost:8080/api/cs-statuses/1"
        }
    }
}
```

### HTTP Request

`PUT http://localhost:8080/api/cs-statuses/{csStatusId}`

`PATCH http://localhost:8080/api/cs-statuses/{csStatusId}`

### URL Parameters

Parameter | Description
--------- | -----------
csStatusId | Selected cs status id

### Parameters

Parameter | Description | Format 
--------- | ----------- | ------ 
csStatusType | Fill with cs status type | String