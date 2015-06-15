## Add New Own Risk

This endpoint used to add new own risk

> Sample request

```shell
curl "http://localhost:8080/api/own-risks"
  -X POST
  -H "Authorization: Bearer <token>"
  -H "Content-Type: application/json"
  -d '{
        "ownRiskType":"Flood"
      }'
```

> Success response

```json
{
    "ownRiskType": "Flood",
    "_links": {
        "self": {
            "href": "http://localhost:8080/api/own-risks/1"
        }
    }
}
```

### HTTP Request

`POST http://localhost:8080/api/own-risks`

### Parameters

Parameter | Description | Format 
--------- | ----------- | ------ 
ownRiskType | Fill with own risk type | String 