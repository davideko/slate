# Accidents
## Get All Accidents

This endpoint used to return all accidents

> Sample request

```shell
curl "http://localhost:8080/api/accidents"
  -H "Authorization: Bearer <token>"
```

> Success response

```json
{
    "_embedded": {
        "accidents": [
            {
                "accidentDate": "2015-06-14",
                "accidentLocation": "Jakarta",
                "vehicleSpeed": "100",
                "damage": "10000",
                "policeStation": "Polda",
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
                    "report": {
                        "href": "http://localhost:8080/api/accidents/3f016e51-07db-42ea-b20b-822b0a6eecdb/report"
                    },
                    "city": {
                        "href": "http://localhost:8080/api/accidents/3f016e51-07db-42ea-b20b-822b0a6eecdb/city"
                    }
                }
            }
        ]
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

`GET http://localhost:8080/api/accidents`