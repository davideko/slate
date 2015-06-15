
## Get a Specific Driver
This endpoint retrieves specific driver.

> Sample request

```shell
  curl "http://localhost:8080/api/drivers/5fc53083-4d3e-4546-97b8-b2cfd23612cc"
  -H "Authorization: Bearer <token>"
```

> Sucessful response

```json
{
  "driverName" : "Ridwan Budimans",
  "driverAddress" : "Green Gardens",
  "driverPhone" : "123456",
  "driverFax" : "123456",
  "driverHandphone" : "123456",
  "driverEmail" : "123456",
  "driverLicenseId" : "1234567890",
  "driverLicenseIssueDate" : "2015-06-03",
  "_links" : {
    "self" : {
      "href" : "http://localhost:8080/api/drivers/5fc53083-4d3e-4546-97b8-b2cfd23612cc{?projection}",
      "templated" : true
    },
    "relation" : {
      "href" : "http://localhost:8080/api/relations/1"
    }
  }
}
```

### HTTP Request

`GET http://localhost:8080/api/drivers/{driverId}`

### URL Parameters

Parameter | Description | Data Type
--------- | ----------- | ---------
driverId | Driver ID to retrieve | string