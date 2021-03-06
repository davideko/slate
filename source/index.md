---
title: BCA Insurance API Documentation

language_tabs:
  - shell

toc_footers:
  - <a href='http://github.com/tripit/slate'>Documentation Powered by Slate</a>

includes:

  - accidents/get-all
  - accidents/get-one
  - accidents/create-one
  - accidents/update-one
  - accidents/delete-one

  - banks/get-all
  - banks/get-one
  - banks/add-new
  - banks/update
  - banks/delete

  - cities/get-all
  - cities/get-one
  - cities/add-new
  - cities/update
  - cities/delete

  - claimants/get-all
  - claimants/get-one
  - claimants/add-new
  - claimants/update
  - claimants/delete

  - coverages/get-all
  - coverages/get-one
  - coverages/create-one
  - coverages/update-one
  - coverages/delete-one

  - cs-statuses/get-all
  - cs-statuses/get-one
  - cs-statuses/create-one
  - cs-statuses/update-one
  - cs-statuses/delete-one

  - drivers/get-all
  - drivers/get-one
  - drivers/add-new
  - drivers/update
  - drivers/delete

  - employees/get-all
  - employees/get-one
  - employees/add-new
  - employees/update
  - employees/delete

  - employees-roles/get-all
  - employees-roles/get-one
  - employees-roles/add-new
  - employees-roles/update
  - employees-roles/delete

  - errors

  - extended-coverages/get-all
  - extended-coverages/get-one
  - extended-coverages/create-one
  - extended-coverages/update-one
  - extended-coverages/delete-one

  - loss-categories/get-all
  - loss-categories/get-one
  - loss-categories/create-one
  - loss-categories/update-one
  - loss-categories/delete-one

  - loss-causals/get-all
  - loss-causals/get-one
  - loss-causals/create-one
  - loss-causals/update-one
  - loss-causals/delete-one

  - own-risks/get-all
  - own-risks/get-one
  - own-risks/create-one
  - own-risks/update-one
  - own-risks/delete-one

  - insureds/get-all
  - insureds/get-one
  - insureds/create-one
  - insureds/update-one
  - insureds/delete-one

  - policies/get-all
  - policies/get-one
  - policies/create-one
  - policies/update-one
  - policies/delete-one

  - premiums/get-all
  - premiums/search-premium
  - premiums/get-one
  - premiums/get-one-premium-coverage
  - premiums/get-one-premium-extended-coverage
  - premiums/get-one-premium-own-risk
  - premiums/get-one-premium-status
  - premiums/create-one
  - premiums/update-one
  - premiums/delete-one

  - premiums-coverages/get-all
  - premiums-coverages/get-one
  - premiums-coverages/create-one
  - premiums-coverages/update-one
  - premiums-coverages/delete-one

  - premiums-extended-coverages/get-all
  - premiums-extended-coverages/get-one
  - premiums-extended-coverages/create-one
  - premiums-extended-coverages/update-one
  - premiums-extended-coverages/delete-one

  - premiums-own-risks/get-all
  - premiums-own-risks/get-one
  - premiums-own-risks/create-one
  - premiums-own-risks/update-one
  - premiums-own-risks/delete-one

  - premium-statuses/get-all
  - premium-statuses/get-one
  - premium-statuses/create-one
  - premium-statuses/update-one
  - premium-statuses/delete-one

  - relations/get-all
  - relations/get-one
  - relations/add-new
  - relations/update
  - relations/delete

  - reports/get-all
  - reports/get-one
  - reports/search
  - reports/add-new
  - reports/update
  - reports/delete

  - report-channels/get-all
  - report-channels/get-one
  - report-channels/add-new
  - report-channels/update
  - report-channels/delete

  - report-statuses/get-all
  - report-statuses/get-one
  - report-statuses/create-one
  - report-statuses/update-one
  - report-statuses/delete-one

  - roles/get-all
  - roles/get-one
  - roles/add-new
  - roles/update
  - roles/delete

  - surveys/get-all
  - surveys/get-one
  - surveys/create-one
  - surveys/update-one
  - surveys/delete-one

  - surveyor-statuses/get-all
  - surveyor-statuses/get-one
  - surveyor-statuses/create-one
  - surveyor-statuses/update-one
  - surveyor-statuses/delete-one

  - tins/get-all
  - tins/get-one
  - tins/add-new
  - tins/update
  - tins/delete

  - tpls/get-all
  - tpls/get-one
  - tpls/add-new
  - tpls/update
  - tpls/delete

  - tpl-categories/get-all
  - tpl-categories/get-one
  - tpl-categories/add-new
  - tpl-categories/update
  - tpl-categories/delete

  - vehicles/get-all
  - vehicles/get-one
  - vehicles/create-one
  - vehicles/update-one
  - vehicles/delete-one

  - vehicle-assemblies/get-all
  - vehicle-assemblies/get-one
  - vehicle-assemblies/create-one
  - vehicle-assemblies/update-one
  - vehicle-assemblies/delete-one

  - vehicle-brands/get-all
  - vehicle-brands/get-one
  - vehicle-brands/create-one
  - vehicle-brands/update-one
  - vehicle-brands/delete-one

  - vehicle-categories/get-all
  - vehicle-categories/get-one
  - vehicle-categories/create-one
  - vehicle-categories/update-one
  - vehicle-categories/delete-one

  - vehicle-colors/get-all
  - vehicle-colors/get-one
  - vehicle-colors/create-one
  - vehicle-colors/update-one
  - vehicle-colors/delete-one

  - vehicle-models/get-all
  - vehicle-models/get-one
  - vehicle-models/create-one
  - vehicle-models/update-one
  - vehicle-models/delete-one

  - vehicle-series/get-all
  - vehicle-series/get-one
  - vehicle-series/create-one
  - vehicle-series/update-one
  - vehicle-series/delete-one

  - workshops/get-all
  - workshops/get-one
  - workshops/add-new
  - workshops/update
  - workshops/delete

  - workshop-categories/get-all
  - workshop-categories/get-one
  - workshop-categories/add-new
  - workshop-categories/update
  - workshop-categories/delete

  - workshop-details/get-all
  - workshop-details/get-one
  - workshop-details/add-new
  - workshop-details/update
  - workshop-details/delete

  - workshop-fees/get-all
  - workshop-fees/get-one
  - workshop-fees/add-new
  - workshop-fees/update
  - workshop-fees/delete

  - workshop-statuses/get-all
  - workshop-statuses/get-one
  - workshop-statuses/create-one
  - workshop-statuses/update-one
  - workshop-statuses/delete-one

search: true
---

# Introduction

Welcome to the BCA Insurance API !

# Authentication

BCA API uses API <code>token</code> to access for required authentication's resources. Umbrella API expect API <code>token</code> to be included in all API requests to the server in request that look s like following:

<code>curl -H "Authorization: Bearer token" -d data</code>

<aside class="notice">
You must replace <code>token</code> with your personal API token.
</aside>

## Get API Token
This endpoint used to retrieve API <code>token</code> 

> Sample request

```shell
curl "http://localhost:8080/oauth/token"
  -u <clientId>:<clientSecret>
  -d "grant_type=password&username=<user_username>&password=<user_password>"
```
> Success response 

```json
{
    "access_token": "634fbf89-429c-49cc-8d22-736e801cd313",
    "token_type": "bearer",
    "refresh_token": "c8816271-9768-4a4e-9380-6d65b38e2ef1",
    "expires_in": 3599,
    "scope": "write"
}
```

> Failed response if wrong server client id or client secret

```json
{
    "timestamp": 1434364862416,
    "status": 401,
    "error": "Unauthorized",
    "message": "Bad credentials",
    "path": "/oauth/token"
}
```

> Failed response if wrong user account

```json
{
    "error": "invalid_grant",
    "error_description": "Bad credentials"
}
```

### HTTP Request

`POST http://localhost:8080/oauth/token`

### Parameters

Parameter | Description
--------- | -----------
clientId | client id
clientSecret | client secret
grant_type | Set to password
username | user username
password | user password


## Refresh Token

This endpoint used to retrieve API <code>token</code> using <code>refresh_token</code> 

> Sample request

```shell
curl "http://localhost:8080/oauth/token"
  -u <clientId>:<clientSecret>
  -d "grant_type=refresh_token&refresh_token=<refresh_token>"
```

> Success response 

```json
{
    "access_token": "0b3e6652-a520-4440-a0e5-ac0c222bdde8",
    "token_type": "bearer",
    "refresh_token": "d5b09ce9-0a3a-404b-b754-fcea309256ac",
    "expires_in": 3599,
    "scope": "write"
}
```

> Failed response if wrong server client id or client secret

```json
{
    "timestamp": 1434365122623,
    "status": 401,
    "error": "Unauthorized",
    "message": "Bad credentials",
    "path": "/oauth/token"
}
```

> Failed response if wrong refresh token

```json
{
    "error": "invalid_grant",
    "error_description": "Invalid refresh token: <refresh_token>"
}
```

### HTTP Request

`POST http://localhost:8080/oauth/token`

### Parameters

Parameter | Description
--------- | -----------
grant_type| Set to refresh_token
refresh_token | Fill with refresh token from request token