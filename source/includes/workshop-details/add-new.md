## Add New Workshop Detail
This endpoint will create new workshop detail.

> Sample request

```shell
  curl "http://localhost:8080/api/workshop-details"
  -X POST
  -H "Authorization: Bearer <token>"
  -d '{
    "workshopManager" : "Nico Natalie",
    "workshopManagerHandphone" : "082120500834",
    "serviceAdvisor" : "David Eko",
    "financeManager" : "Immanuel Resha",
    "financeManagerHandphone" : "1234564455",
    "serviceAdvisorPhone" : "123456789001"
  }'
```

> Sucessful response

```json
{
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
}
```

### HTTP Request

`POST http://localhost:8080/api/workshop-details`

###  Parameters

Parameter | Description | Data Type
--------- | ----------- | ---------
workshopManager | New Workshop manager name | string
workshopManagerHandphone | New workshop manager handphone | string
financeManager | New finance manager name | string
financeManagerHandphone | New finance manager handhpone | string
serviceAdvisorPhone | New service advisor phone string
serviceAdvisor | New service advisor name | string