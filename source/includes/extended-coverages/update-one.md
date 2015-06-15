## Update Premium Status

This endpoint used to update a extended coverage object. It can update using <code>PUT</code> for full update or <code>PATCH</code> for partial update

> Sample request PUT

```shell
curl "http://localhost:8080/api/extended-coverages/1"
  -X PUT
  -H "Authorization: Bearer <token>"
  -H "Content-Type: application/json"
  -d '{
        "extendedCoverageType":"Erosion"
      }'
```

> Sample request PATCH

```shell
curl "http://localhost:8080/api/extended-coverages/1"
  -X PATCH
  -H "Authorization: Bearer <token>"
  -H "Content-Type: application/json"
  -d '{
        "extendedCoverageType":"Erosion"
      }'
```

> Success response

```json
{
    "extendedCoverageType": "Erosion",
    "_links": {
        "self": {
            "href": "http://localhost:8080/api/extended-coverages/1"
        }
    }
}
```

### HTTP Request

`PUT http://localhost:8080/api/extended-coverages/{extendedCoverageId}`

`PATCH http://localhost:8080/api/extended-coverages/{extendedCoverageId}`

### URL Parameters

Parameter | Description
--------- | -----------
extendedCoverageId | Selected extended coverage id

### Parameters

Parameter | Description | Format 
--------- | ----------- | ------ 
extendedCoverageType | Fill with extended coverage type | String