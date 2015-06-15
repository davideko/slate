## Add New Workshop Status

This endpoint used to add new workshop status

> Sample request

```shell
curl "http://localhost:8080/api/workshop-statuses"
  -X POST
  -H "Authorization: Bearer <token>"
  -H "Content-Type: application/json"
  -d '{
        "workshopStatusType":"Partner"
      }'
```

> Success response

```json
{
    "workshopStatusType": "Partner",
    "_links": {
        "self": {
            "href": "http://localhost:8080/api/workshop-statuses/1"
        }
    }
}
```

> Failed response

```json
{
  "error": "because"
}
```

### HTTP Request

`POST http://localhost:8080/api/workshop-statuses`

### Parameters

Parameter | Description | Format 
--------- | ----------- | ------ 
workshopStatusType | Fill with workshop status type | String 