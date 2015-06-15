## Update Driver
This endpoint will update driver by ID.

> Sample request PUT

```shell
  curl "http://localhost:8080/api/drivers/5fc53083-4d3e-4546-97b8-b2cfd23612cc"
  -X PUT
  -H "Authorization: Bearer <token>"
  -d '{
    "driverName" : "Ridwan Budiman",
    "driverAddress" : "Green Garden",
    "driverPhone" : "123456",
    "driverFax" : "123456",
    "driverHandphone" : "123456",
    "driverEmail" : "123456",
    "driverLicenseId" : "1234567890",
    "driverLicenseIssueDate" : "2015-06-03"
  }'
```

> Sample request PATCH

```shell
  curl "http://localhost:8080/api/5fc53083-4d3e-4546-97b8-b2cfd23612cc"
  -X PATCH
  -H "Authorization: Bearer <token>"
  -d '{
    "driverName" : "Ridwan Budiman",
    "driverAddress" : "Green Garden"
  }'
```

> Success response

```json
{
  "driverName" : "Ridwan Budiman",
  "driverAddress" : "Green Garden",
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

`PUT http://localhost:8080/api/drivers/{driverId}`

`PATCH http://localhost:8080/api/drivers/{driverId}`

### URL Parameters

Parameter | Description | Format
--------- | ----------- | ---------
driverId | Driver ID to update | string

### Parameters

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