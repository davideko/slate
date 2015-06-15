## Delete Claimant
This endpoint will delete claimant by ID.

> Sample request

```shell
  curl "http://localhost:8080/api/claimants/0bf56d35-1dc2-4826-a6e0-9e67397c6283"
  -X DELETE
  -H "Authorization: Bearer <token>"
```

> Success response <code>HTTP 204 No Content</code>

### HTTP Request

`DELETE http://localhost:8080/api/claimants/{claimantId}`

### URL Parameters

Parameter | Description | Format
--------- | ----------- | ---------
claimantId | Claimant ID to delete | String