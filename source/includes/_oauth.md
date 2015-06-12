# Authentication

Umbrella API uses API <code>token</code> to access for required authentication's resources. Umbrella API expect API <code>token</code> to be included in all API requests to the server in request that look s like following:

<code>curl -H "Authorization: Bearer <code>token</code>" -d "data"</code>

<aside class="notice">
You must replace <code>token</code> with your personal API key.
</aside>

## Get API Token

This endpoint used to retrieve API <code>token</code>

> Sample request

```shell
curl "http://localhost:8080/oauth/token"
  -X POST
  -u <clientId>:<clientSecret>
  -d "grant_type=password&username=<user_username>&password=<user_password>"
```
> Success response 

```json
{
  "access_token": "7f9471ff-5d7b-4aee-92ca-f13d9c66c37a",
  "token_type": "bearer",
  "refresh_token": "d5b09ce9-0a3a-404b-b754-fcea309256ac",
  "expires_in": 3599,
  "scope": "write"
}
```

> Failed response

```json
{
  "timestamp": 1433945751615,
  "status": 401,
  "error": "Unauthorized",
  "message": "Bad credentials",
  "path": "/oauth/token"
}
```

### HTTP Request

`POST http://localhost:8080/oauth/token`

### Parameters

Parameter | Description
--------- | -----------
clientId | Used in basic auth, fill with client id
clientSecret | Used in basic auth, fill with client secret
grant_type | Fill grant type with password
username | Fill with your username
password | Fill with your password

## Refresh Token

This endpoint used to retrieve API <code>token</code> using <code>refresh_token</code>.

> Sample request

```shell
curl "http://localhost:8080/oauth/token"
  -X POST
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

> Failed Response

```json
  {
    "timestamp": 1433945751615,
    "status": 401,
    "error": "Unauthorized",
    "message": "Bad credentials",
    "path": "/oauth/token"
  }
```

### HTTP Request

`POST http://localhost:8080/oauth/token`

### Parameters

Parameter | Description
--------- | -----------
grant_type| Set to refresh_token
refresh_token | Fill with refresh token from request token
