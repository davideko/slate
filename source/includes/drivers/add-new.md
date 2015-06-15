## Add New Driver
This endpoint will create new driver.

> Sample request

```shell
  curl "http://localhost:8080/api/drivers"
  -X POST
  -H "Authorization: Bearer <token>"
  -d '{
    "driverName" : "Ridwan Budimans",
    "driverAddress" : "Green Gardens",
    "driverPhone" : "123456",
    "driverFax" : "123456",
    "driverHandphone" : "123456",
    "driverEmail" : "123456",
    "driverLicenseId" : "1234567890",
    "driverLicenseIssueDate" : "2015-06-03"
  }'
```

> Success response

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

`POST http://localhost:8080/api/drivers`

###  Parameters

Parameter | Description | Format
--------- | ----------- | ---------
driverName | New driver name | string
driverAddress | New driver address | string
driverPhone | New driver phone | string
driverFax | New driver fax | string
driverHandphone | New driver phone | string
driverEmail | New driver email | string
driverLicenseId | New driver license id | string
driverLicenseIssueDate | New driver license issue date | datetime

