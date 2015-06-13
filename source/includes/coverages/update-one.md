## Update Coverages

This endpoint used to update a coverages object. It can update using <code>PUT</code> for full update or <code>PATCH</code> for partial update

> Sample request PUT

```shell
curl "http://localhost:8080/api/coverages/1"
  -X PUT
  -H "Authorization: Bearer <token>"
  -H "Content-Type: application/json"
  -d '{
        "coverageType":"Liability"
      }'
```

> Sample request PATCH

```shell
curl "http://localhost:8080/api/coverages/1"
  -X PATCH
  -H "Authorization: Bearer <token>"
  -H "Content-Type: application/json"
  -d '{
        "coverageType":"Liability"
      }'
```

> Success response

```json
{
    "coverageType": "Liability",
    "_links": {
        "self": {
            "href": "http://localhost:8080/api/coverages/1"
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

`PUT http://localhost:8080/api/coverages/<coverageId>`

`PATCH http://localhost:8080/api/coverages/<coverageId>`

### URL Parameters

Parameter | Description
--------- | -----------
coverageId | Selected coverages id

### Parameters

Parameter | Description | Format 
--------- | ----------- | ------ 
coverageType | Fill with coverages type | String