# Coverages
## Get All Coverages

This endpoint used to return all coverages

> Sample request

```shell
curl "http://localhost:8080/api/coverages"
  -H "Authorization: Bearer <token>"
```

> Success response

```json
{
    "_embedded": {
        "coverages": [
            {
                "coverageType": "CASCO",
                "_links": {
                    "self": {
                        "href": "http://localhost:8080/api/coverages/1"
                    }
                }
            },
            {
                "coverageType": "Collision",
                "_links": {
                    "self": {
                        "href": "http://localhost:8080/api/coverages/2"
                    }
                }
            },
            {
                "coverageType": "Comprehensive",
                "_links": {
                    "self": {
                        "href": "http://localhost:8080/api/coverages/3"
                    }
                }
            },
            {
                "coverageType": "TPL",
                "_links": {
                    "self": {
                        "href": "http://localhost:8080/api/coverages/4"
                    }
                }
            }
        ]
    }
}
```

### HTTP Request 

`GET http://localhost:8080/api/coverages`