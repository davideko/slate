# Errors

> Response might look like this

```json
{
  "timestamp": 1434364722886,
  "status": 405,
  "error": "Method Not Allowed",
  "exception": "org.springframework.web.HttpRequestMethodNotSupportedException",
  "message": "Request method 'POST' not supported",
  "path": "/api/accidents/1"
}
```

The BCA Insurance API uses the following error codes:

Error Code | Meaning | Description
---------- | ------- | -----------
400 | Bad Request  | Your request bad
401 | Unauthorized | Your API key is wrong
403 | Forbidden | The resource requested is hidden for administrators only
404 | Not Found | The specified resource could not be found
405 | Method Not Allowed | You tried to access a resource with an invalid method
500 | Internal Server Error | We had a problem with our server. Try again later.