## Update Own Risk

This endpoint used to update a own risk object. It can update using <code>PUT</code> for full update or <code>PATCH</code> for partial update

> Sample request PUT

```shell
curl "http://localhost:8080/api/own-risks/1"
  -X PUT
  -H "Authorization: Bearer <token>"
  -H "Content-Type: application/json"
  -d '{
        "ownRiskType":"Erosion"
      }'
```

> Sample request PATCH

```shell
curl "http://localhost:8080/api/own-risks/1"
  -X PATCH
  -H "Authorization: Bearer <token>"
  -H "Content-Type: application/json"
  -d '{
        "ownRiskType":"Erosion"
      }'
```

> Success response

```json
{
    "ownRiskType": "Erosion",
    "_links": {
        "self": {
            "href": "http://localhost:8080/api/own-risks/1"
        }
    }
}

### HTTP Request

`PUT http://localhost:8080/api/own-risks/{ownRiskId}`

`PATCH http://localhost:8080/api/own-risks/{ownRiskId}`

### URL Parameters

Parameter | Description
--------- | -----------
ownRiskId | Selected own risk id

### Parameters

Parameter | Description | Format 
--------- | ----------- | ------ 
ownRiskType | Fill with own risk type | String