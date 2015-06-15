# Workshop Detail

## Get All Workshop Details
This endpoint retrieves all workshop details.

> Sample request

```shell
  curl "http://localhost:8080/api/workshop-details"
  -H "Authorization: Bearer <token>"
```

> Sucessful response

```json
{
  "_embedded" : {
    "workshopDetails" : [ {
      "workshopManager" : "Nico Natalie",
      "workshopManagerHandphone" : "082120500834",
      "serviceAdvisor" : "David Eko",
      "financeManager" : "Immanuel Resha",
      "financeManagerHandphone" : "1234564455",
      "serviceAdvisorPhone" : "123456789001",
      "_links" : {
        "self" : {
          "href" : "http://localhost:8080/api/workshop-details/4CFEADB9-EAF8-48A7-808A-0CF141A8B99D"
        }
      }
    } ]
  }
}
```

### HTTP Request

`GET http://localhost:8080/api/workshop-details`

