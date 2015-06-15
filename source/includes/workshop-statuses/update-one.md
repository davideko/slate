## Update Workshop Status

This endpoint used to update a workshop status object. It can update using <code>PUT</code> for full update or <code>PATCH</code> for partial update

> Sample request PUT

```shell
curl "http://localhost:8080/api/workshop-statuses/1"
  -X PUT
  -H "Authorization: Bearer <token>"
  -H "Content-Type: application/json"
  -d '{
        "workshopStatusType":"Off"
      }'
```

> Sample request PATCH

```shell
curl "http://localhost:8080/api/workshop-statuses/1"
  -X PATCH
  -H "Authorization: Bearer <token>"
  -H "Content-Type: application/json"
  -d '{
        "workshopStatusType":"Off"
      }'
```

> Success response

```json
{
    "workshopStatusType": "Off",
    "_links": {
        "self": {
            "href": "http://localhost:8080/api/workshop-statuses/1"
        }
    }
}
```

### HTTP Request

`PUT http://localhost:8080/api/workshop-statuses/{workshopStatusId}`

`PATCH http://localhost:8080/api/workshop-statuses/{workshopStatusId}`

### URL Parameters

Parameter | Description
--------- | -----------
workshopStatusId | Selected workshop status id

### Parameters

Parameter | Description | Format 
--------- | ----------- | ------ 
workshopStatusType | Fill with workshop status type | String