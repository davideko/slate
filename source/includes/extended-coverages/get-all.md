# Extended Coverages
## Get All Extended Coverages

This endpoint used to return all extended coverages

> Sample request

```shell
curl "http://localhost:8080/api/extended-coverages"
  -H "Authorization: Bearer <token>"
```

> Success response

```json
{
    "_embedded": {
        "extendedCoverages": [
            {
                "extendedCoverageType": "Comprehensive",
                "_links": {
                    "self": {
                        "href": "http://localhost:8080/api/extended-coverages/1"
                    }
                }
            },
            {
                "extendedCoverageType": "Flood",
                "_links": {
                    "self": {
                        "href": "http://localhost:8080/api/extended-coverages/2"
                    }
                }
            },
            {
                "extendedCoverageType": "Earthquake",
                "_links": {
                    "self": {
                        "href": "http://localhost:8080/api/extended-coverages/3"
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

`GET http://localhost:8080/api/extended-coverages`