## Update Workshop Detail
This endpoint will update workshop detail by ID.

> Sample request PUT

```shell
  curl "http://localhost:8080/api/workshop-details/4CFEADB9-EAF8-48A7-808A-0CF141A8B99D"
  -X PUT
  -H "Authorization: Bearer <token>"
  -d '{
    "workshopManager" : "Nico",
    "workshopManagerHandphone" : "082120500834",
    "serviceAdvisor" : "David Eko",
    "financeManager" : "Immanuel Resha",
    "financeManagerHandphone" : "1234564455",
    "serviceAdvisorPhone" : "123456789001"
  }'
```

> Sample request PATCH

```shell
  curl "http://localhost:8080/api/workshop-details/4CFEADB9-EAF8-48A7-808A-0CF141A8B99D"
  -X PATCH
  -H "Authorization: Bearer <token>"
  -d '{
    "workshopManager" : "Nico",
    "workshopManagerHandphone" : "082120500834",
    "serviceAdvisor" : "David Eko",
    "financeManager" : "Immanuel Resha",
    "financeManagerHandphone" : "1234564455",
    "serviceAdvisorPhone" : "123456789001"
  }'
```

> Success response

```json
{
  "workshopManager" : "Nico",
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
}
```

### HTTP Request

`PUT http://localhost:8080/api/workshop-details/{workshopDetailId}`

`PATCH http://localhost:8080/api/workshop-details/{workshopDetailId}`

### URL Parameters

Parameter | Description | Format
--------- | ----------- | ---------
workshopDetailId | Workshop detail ID to update | string

### Parameters

Parameter | Description | Format
--------- | ----------- | ---------