## Update Accident

This endpoint used to update a accident object. It can update using <code>PUT</code> for full update or <code>PATCH</code> for partial update

> Sample request PUT

```shell
curl "http://localhost:8080/api/accidents/3f016e51-07db-42ea-b20b-822b0a6eecdb"
  -X PUT
  -H "Authorization: Bearer <token>"
  -H "Content-Type: application/json"
  -d '{
        "accidentDate":"2015-06-14",
        "accidentLocation":"Jakarta",
        "vehicleSpeed":"100",
        "damage":"100000",
        "policeStation":"Polda Slipi",
        "witnesses":"none",
        "vehicleUsage":"casual",
        "lossCategory":"http://localhost:8080/api/loss-categories/1",
        "city":"http://localhost:8080/api/cities/1",
        "tpl":"http://localhost:8080/api/tpls/",
        "report":"http://localhost:8080/api/reports/"
      }'
```

> Sample request PATCH

```shell
curl "http://localhost:8080/api/accidents/3f016e51-07db-42ea-b20b-822b0a6eecdb"
  -X PATCH
  -H "Authorization: Bearer <token>"
  -H "Content-Type: application/json"
  -d '{
        "policeStation":"Polda Slipi"
      }'
```

> Success response

```json
{
    "accidentDate": "2015-06-14",
    "accidentLocation": "Jakarta",
    "vehicleSpeed": "100",
    "damage": "10000",
    "policeStation": "Polda Slipi",
    "witnesses": "none",
    "vehicleUsage": "casual",
    "_embedded": {
        "tpl": {
            "tplValue": 1000000,
            "tplAddress": "Pulogadung",
            "tplDamage": "Full damage",
            "tplName": "Jon Snow",
            "tplPhone": "08598887898",
            "tplMake": "insured",
            "tplCategory": {
                "tplCategoryType": "Type 1"
            },
            "tplId": "7d55e8c2-4eca-4f11-b74c-64d8f36775a6",
            "tplPlateNumber": "B 8888 KKK"
        }
    },
    "_links": {
        "self": {
            "href": "http://localhost:8080/api/accidents/3f016e51-07db-42ea-b20b-822b0a6eecdb"
        },
        "lossCategory": {
            "href": "http://localhost:8080/api/accidents/3f016e51-07db-42ea-b20b-822b0a6eecdb/lossCategory"
        },
        "tpl": {
            "href": "http://localhost:8080/api/accidents/3f016e51-07db-42ea-b20b-822b0a6eecdb/tpl"
        },
        "report": {
            "href": "http://localhost:8080/api/accidents/3f016e51-07db-42ea-b20b-822b0a6eecdb/report"
        },
        "city": {
            "href": "http://localhost:8080/api/accidents/3f016e51-07db-42ea-b20b-822b0a6eecdb/city"
        }
    }
}
```

### HTTP Request

`PUT http://localhost:8080/api/accidents/<accidentId>`

`PATCH http://localhost:8080/api/accidents/<accidentId>`

### URL Parameters

Parameter | Description
--------- | -----------
accidentId | Selected accident id

### Parameters

Parameter | Description | Format 
--------- | ----------- | ------ 
accidentDate | Fill with accident date | String (date)
accidentLocation | Fill with accident location | String
vehicleSpeed | Fill with vehicle speed | String
damage | Fill with damage | String
policeStation | Fill with police station | String
witnesses | Fill with witnesses | String
vehicleUsage | Fill with vehicle usage | String
lossCategory | Fill with loss category object url id | String
city | Fill with city object url id | String
tpl | Fill with tpl object url id | String
report | Fill with report object url id | String