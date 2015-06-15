## Add New Extended Coverage

This endpoint used to add new extended coverage

> Sample request

```shell
curl "http://localhost:8080/api/extended-coverages"
  -X POST
  -H "Authorization: Bearer <token>"
  -H "Content-Type: application/json"
  -d '{
        "extendedCoverageType":"Comprehensive"
      }'
```

> Success response

```json
{
    "extendedCoverageType": "Comprehensive",
    "_links": {
        "self": {
            "href": "http://localhost:8080/api/extended-coverages/1"
        }
    }
}
```

### HTTP Request

`POST http://localhost:8080/api/extended-coverages`

### Parameters

Parameter | Description | Format 
--------- | ----------- | ------ 
extendedCoverageType | Fill with extended coverage type | String 