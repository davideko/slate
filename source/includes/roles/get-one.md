
## Get a Specific Role
This endpoint retrieves specific role.

> Sample request

```shell
  curl "http://localhost:8080/api/roles/1"
  -H "Authorization: Bearer <token>"
```

> Success response

```json
{
  "roleType" : "Manager",
  "_links" : {
    "self" : {
      "href" : "http://localhost:8080/api/roles/1"
    }
  }
}
```

### HTTP Request

`GET http://localhost:8080/api/roles/{roleId}`

### URL Parameters

Parameter | Description | Format
--------- | ----------- | ---------
roleId | Role ID to retrieve | integer