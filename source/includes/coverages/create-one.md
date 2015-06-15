## Add New Coverage

This endpoint used to add new coverage

> Sample request

```shell
curl "http://localhost:8080/api/coverages"
  -X POST
  -H "Authorization: Bearer <token>"
  -H "Content-Type: application/json"
  -d '{
        "coverageType":"CASCO"
      }'
```

> Success response

```json
{
    "coverageType": "CASCO",
    "_links": {
        "self": {
            "href": "http://localhost:8080/api/coverages/1"
        }
    }
}
```

### HTTP Request

`POST http://localhost:8080/api/coverages`

### Parameters

Parameter | Description | Format 
--------- | ----------- | ------ 
coverageType | Fill with coverage type | String 