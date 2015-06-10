---
title: API Documentation

language_tabs:
  - shell

toc_footers:
  - <a href='#'>Sign Up for a Developer Key</a>
  - <a href='http://github.com/tripit/slate'>Documentation Powered by Slate</a>

includes:
  - errors

search: true
---

# Introduction

Welcome to the Umbrella API !

# Authentication

Umbrella API uses API <code>token</code> to access for required authentication's resources. Umbrella API expect API <code>token</code> to be included in all API requests to the server in request that look s like following:

<code>curl -H "Authorization: Bearer <code>token</code>" -d "data"</code>

<aside class="notice">
You must replace <code>token</code> with your personal API key.
</aside>

## Get API Token

> Sample request

```shell
curl "http://localhost:8080/api/oauth/token"
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

This endpoint used to retrieve API <code>token</code> 

### HTTP Request

`POST http://localhost:8080/api/oauth/token`

### Parameters

Parameter | Description
--------- | -----------
clientId | client id.
clientSecret | client secret.
grant_type | Set to password.
username | user username.
password | user password.


## Refresh Token

> Sample request

```shell
curl "http://localhost:8080/api/oauth/token"
  -u <clientId>:<clientSecret>
  -d "grant_type=refresh_token&refresh_token=<refresh_token>"
```

> Success Response

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

This endpoint used to retrieve API <code>token</code> using <code>refresh_token</code> 

### HTTP Request

`POST http://localhost:8080/api/oauth/token`

### Parameters

Parameter | Description
--------- | -----------
grant_type| Set to refresh_token.
refresh_token | Fill with refresh token from request token.


# Reports

## Get All Reports

> Sample request

```shell
curl "http://localhost:8080/api/reports"
  -H "Authorization: Bearer <token>"
```

> Success response

```json
  {
    "_links": {
        "self": {
            "href": "http://localhost:8080/api/reports{?page,size,sort}",
            "templated": true
        }
    },
    "_embedded": {
        "reports": [
            {
                "reportDate": "2015-06-10",
                "reportedBy": "Eobard Thawn",
                "reportNote": "Watch out Barry",
                "ownRisk": 100000,
                "_embedded": {
                    "workshop": {
                        "bank": {
                            "bankName": "bank"
                        },
                        "workshopId": "d5dc370b-e301-4421-a913-a61026221636",
                        "tin": {
                            "taxIdentificationName": "siapa",
                            "taxIdentificationAddress": "jalan mana"
                        },
                        "city": {
                            "cityName": "Jakarta"
                        },
                        "workshopDetail": {
                            "workshopManager": "test",
                            "workshopManagerHandphone": "coba",
                            "serviceAdvisor": "ini",
                            "financeManager": "aaa",
                            "financeManagerHandphone": "088888",
                            "serviceAdvisorPhone": null
                        },
                        "workshopFee": {
                            "pph23": 1111,
                            "sparePartServicePercentage": 1111,
                            "sparePartPpn": 1111,
                            "sparePartPercentage": 11111,
                            "sparePartDiscount": 1111,
                            "servicePpn": 1111,
                            "servicePercentage": 1111,
                            "serviceDiscount": 1111,
                            "salvageDiscount": 11111,
                            "isTaxIncluded": true
                        },
                        "workshopCategory": {
                            "workshopCategoryType": "test"
                        },
                        "workshopName": "Bengkel test",
                        "workshopPicHandphone": "089898989",
                        "accountNumber": "090989898888888888",
                        "workshopEmail": "dvd@gmmm",
                        "workshopPicTitle": "ini",
                        "workshopFax": "0423455",
                        "feeSystemValue": 1111,
                        "workshopPic": "dia",
                        "workshopAddress": "jalan test",
                        "workshopPhone": "08888",
                        "isFeeSystem": true,
                        "isSupplier": true,
                        "isOnline": true,
                        "onlineDate": "2015-06-10",
                        "isActive": true
                    },
                    "claimant": {
                        "claimantId": "e3f5ff17-9875-4ca1-b23b-a4d84e8f90f7",
                        "relation": {
                            "relationType": "test"
                        },
                        "claimantAddress": "jalan test",
                        "claimantFax": "8989898",
                        "claimantPhone": "0000",
                        "claimantEmail": "dvdvddv@ahbhsb",
                        "claimantHandphone": "1112222",
                        "claimantName": "test"
                    }
                },
                "_links": {
                    "self": {
                        "href": "http://localhost:8080/api/reports/c8a373f2-7ed8-4602-b16d-d33a467becf3"
                    },
                    "csStatus": {
                        "href": "http://localhost:8080/api/reports/c8a373f2-7ed8-4602-b16d-d33a467becf3/csStatus"
                    },
                    "surveyorEmployee": {
                        "href": "http://localhost:8080/api/reports/c8a373f2-7ed8-4602-b16d-d33a467becf3/surveyorEmployee"
                    },
                    "reportChannel": {
                        "href": "http://localhost:8080/api/reports/c8a373f2-7ed8-4602-b16d-d33a467becf3/reportChannel"
                    },
                    "lossCausal": {
                        "href": "http://localhost:8080/api/reports/c8a373f2-7ed8-4602-b16d-d33a467becf3/lossCausal"
                    },
                    "workshopStatus": {
                        "href": "http://localhost:8080/api/reports/c8a373f2-7ed8-4602-b16d-d33a467becf3/workshopStatus"
                    },
                    "csEmployee": {
                        "href": "http://localhost:8080/api/reports/c8a373f2-7ed8-4602-b16d-d33a467becf3/csEmployee"
                    },
                    "premium": {
                        "href": "http://localhost:8080/api/reports/c8a373f2-7ed8-4602-b16d-d33a467becf3/premium"
                    },
                    "reportStatus": {
                        "href": "http://localhost:8080/api/reports/c8a373f2-7ed8-4602-b16d-d33a467becf3/reportStatus"
                    },
                    "survey": {
                        "href": "http://localhost:8080/api/reports/c8a373f2-7ed8-4602-b16d-d33a467becf3/survey"
                    },
                    "driver": {
                        "href": "http://localhost:8080/api/reports/c8a373f2-7ed8-4602-b16d-d33a467becf3/driver"
                    },
                    "surveyorStatus": {
                        "href": "http://localhost:8080/api/reports/c8a373f2-7ed8-4602-b16d-d33a467becf3/surveyorStatus"
                    }
                }
            },
            {
                "reportDate": "2015-06-10",
                "reportedBy": "Barry Allen",
                "reportNote": "Watch out for the reverse flash",
                "ownRisk": 500000,
                "_embedded": {
                    "workshop": {
                        "bank": {
                            "bankName": "bank"
                        },
                        "workshopId": "d5dc370b-e301-4421-a913-a61026221636",
                        "tin": {
                            "taxIdentificationName": "siapa",
                            "taxIdentificationAddress": "jalan mana"
                        },
                        "city": {
                            "cityName": "Jakarta"
                        },
                        "workshopDetail": {
                            "workshopManager": "test",
                            "workshopManagerHandphone": "coba",
                            "serviceAdvisor": "ini",
                            "financeManager": "aaa",
                            "financeManagerHandphone": "088888",
                            "serviceAdvisorPhone": null
                        },
                        "workshopFee": {
                            "pph23": 1111,
                            "sparePartServicePercentage": 1111,
                            "sparePartPpn": 1111,
                            "sparePartPercentage": 11111,
                            "sparePartDiscount": 1111,
                            "servicePpn": 1111,
                            "servicePercentage": 1111,
                            "serviceDiscount": 1111,
                            "salvageDiscount": 11111,
                            "isTaxIncluded": true
                        },
                        "workshopCategory": {
                            "workshopCategoryType": "test"
                        },
                        "workshopName": "Bengkel test",
                        "workshopPicHandphone": "089898989",
                        "accountNumber": "090989898888888888",
                        "workshopEmail": "dvd@gmmm",
                        "workshopPicTitle": "ini",
                        "workshopFax": "0423455",
                        "feeSystemValue": 1111,
                        "workshopPic": "dia",
                        "workshopAddress": "jalan test",
                        "workshopPhone": "08888",
                        "isFeeSystem": true,
                        "isSupplier": true,
                        "isOnline": true,
                        "onlineDate": "2015-06-10",
                        "isActive": true
                    },
                    "claimant": {
                        "claimantId": "e3f5ff17-9875-4ca1-b23b-a4d84e8f90f7",
                        "relation": {
                            "relationType": "test"
                        },
                        "claimantAddress": "jalan test",
                        "claimantFax": "8989898",
                        "claimantPhone": "0000",
                        "claimantEmail": "dvdvddv@ahbhsb",
                        "claimantHandphone": "1112222",
                        "claimantName": "test"
                    }
                },
                "_links": {
                    "self": {
                        "href": "http://localhost:8080/api/reports/deb45d4b-2fe4-47ea-aad7-b5ed04aaa2f2"
                    },
                    "csStatus": {
                        "href": "http://localhost:8080/api/reports/deb45d4b-2fe4-47ea-aad7-b5ed04aaa2f2/csStatus"
                    },
                    "surveyorEmployee": {
                        "href": "http://localhost:8080/api/reports/deb45d4b-2fe4-47ea-aad7-b5ed04aaa2f2/surveyorEmployee"
                    },
                    "reportChannel": {
                        "href": "http://localhost:8080/api/reports/deb45d4b-2fe4-47ea-aad7-b5ed04aaa2f2/reportChannel"
                    },
                    "lossCausal": {
                        "href": "http://localhost:8080/api/reports/deb45d4b-2fe4-47ea-aad7-b5ed04aaa2f2/lossCausal"
                    },
                    "workshopStatus": {
                        "href": "http://localhost:8080/api/reports/deb45d4b-2fe4-47ea-aad7-b5ed04aaa2f2/workshopStatus"
                    },
                    "csEmployee": {
                        "href": "http://localhost:8080/api/reports/deb45d4b-2fe4-47ea-aad7-b5ed04aaa2f2/csEmployee"
                    },
                    "premium": {
                        "href": "http://localhost:8080/api/reports/deb45d4b-2fe4-47ea-aad7-b5ed04aaa2f2/premium"
                    },
                    "reportStatus": {
                        "href": "http://localhost:8080/api/reports/deb45d4b-2fe4-47ea-aad7-b5ed04aaa2f2/reportStatus"
                    },
                    "survey": {
                        "href": "http://localhost:8080/api/reports/deb45d4b-2fe4-47ea-aad7-b5ed04aaa2f2/survey"
                    },
                    "driver": {
                        "href": "http://localhost:8080/api/reports/deb45d4b-2fe4-47ea-aad7-b5ed04aaa2f2/driver"
                    },
                    "surveyorStatus": {
                        "href": "http://localhost:8080/api/reports/deb45d4b-2fe4-47ea-aad7-b5ed04aaa2f2/surveyorStatus"
                    }
                }
            }
        ]
    },
    "page": {
        "size": 20,
        "totalElements": 2,
        "totalPages": 1,
        "number": 0
    }
  }
```
This endpoint return all reports

### HTTP Request

`GET http://localhost:8080/api/reports`

## Get Report By Id

> Sample Request

> Success Response

This endpoint create new report

## Create New Report

> Sample request

```shell
curl "http://localhost:8080/api/reports"
  -H "Authorization: Bearer <token>"
  -H "Content -Type: application/json"
  -d '{
    "reportDate":"2015-06-10",
    "reportedBy":"Barry Allen",
    "reportNote":"Watch out for the reverse flash",
    "ownRisk":"500000",
    "reportChannel":"http://localhost:8080/api/report-channels/1",
    "lossCausal":"http://localhost:8080/api/loss-causals/1",
    "premium":"http://localhost:8080/api/premiums/1ffc0022-6e51-43b3-b4b5-649634fd086c",
    "survey":"http://localhost:8080/api/surveys/d5c1e5ae-9bf8-4b13-93d3-947fd74ba24d",
    "claimant":"http://localhost:8080/api/claimants/e3f5ff17-9875-4ca1-b23b-a4d84e8f90f7",
    "driver":"http://localhost:8080/api/drivers/07581e6a-2c58-4ac9-8833-51ab494f74b0",
    "csEmployee":"http://localhost:8080/api/employees/7ba187de-c73d-4ca7-b7d4-c593169352fe",
    "csStatus":"http://localhost:8080/api/cs-statuses/1",
    "surveyorEmployee":"http://localhost:8080/api/employees/8567ef78-876a-4219-8190-88404a536902",
    "surveyorStatus":"http://localhost:8080/api/surveyor-statuses/1",
    "workshop":"http://localhost:8080/api/workshops/d5dc370b-e301-4421-a913-a61026221636",
    "workshopStatus":"http://localhost:8080/api/workshop-statuses/1",
    "reportStatus":"http://localhost:8080/api/report-statuses/1"
      }'
```

> Success response

```json
  {
      "reportDate": "2015-06-10T00:00:00.000+0000",
      "reportedBy": "Irris West",
      "reportNote": "Fill the note",
      "ownRisk": 1000000,
      "_embedded": {
          "workshop": {
              "bank": {
                  "bankName": "bank"
              },
              "workshopId": "d5dc370b-e301-4421-a913-a61026221636",
              "tin": {
                  "taxIdentificationName": "siapa",
                  "taxIdentificationAddress": "jalan mana"
              },
              "city": {
                  "cityName": "Jakarta"
              },
              "workshopDetail": {
                  "workshopManager": "test",
                  "workshopManagerHandphone": "coba",
                  "serviceAdvisor": "ini",
                  "financeManager": "aaa",
                  "financeManagerHandphone": "088888",
                  "serviceAdvisorPhone": null
              },
              "workshopFee": {
                  "pph23": 1111,
                  "sparePartServicePercentage": 1111,
                  "sparePartPpn": 1111,
                  "sparePartPercentage": 11111,
                  "sparePartDiscount": 1111,
                  "servicePpn": 1111,
                  "servicePercentage": 1111,
                  "serviceDiscount": 1111,
                  "salvageDiscount": 11111,
                  "isTaxIncluded": true
              },
              "workshopCategory": {
                  "workshopCategoryType": "test"
              },
              "workshopName": "Bengkel test",
              "workshopPicHandphone": "089898989",
              "accountNumber": "090989898888888888",
              "workshopEmail": "dvd@gmmm",
              "workshopPicTitle": "ini",
              "workshopFax": "0423455",
              "feeSystemValue": 1111,
              "workshopPic": "dia",
              "workshopAddress": "jalan test",
              "workshopPhone": "08888",
              "isFeeSystem": true,
              "isSupplier": true,
              "isOnline": true,
              "onlineDate": "2015-06-10",
              "isActive": true
          },
          "claimant": {
              "claimantId": "e3f5ff17-9875-4ca1-b23b-a4d84e8f90f7",
              "relation": {
                  "relationType": "test"
              },
              "claimantAddress": "jalan test",
              "claimantFax": "8989898",
              "claimantPhone": "0000",
              "claimantEmail": "dvdvddv@ahbhsb",
              "claimantHandphone": "1112222",
              "claimantName": "test"
          }
      },
      "_links": {
          "self": {
              "href": "http://localhost:8080/api/reports/cd4e6eea-990e-4c16-b99d-e8dd4a4da9d4"
          },
          "csStatus": {
              "href": "http://localhost:8080/api/reports/cd4e6eea-990e-4c16-b99d-e8dd4a4da9d4/csStatus"
          },
          "claimant": {
              "href": "http://localhost:8080/api/reports/cd4e6eea-990e-4c16-b99d-e8dd4a4da9d4/claimant"
          },
          "surveyorEmployee": {
              "href": "http://localhost:8080/api/reports/cd4e6eea-990e-4c16-b99d-e8dd4a4da9d4/surveyorEmployee"
          },
          "reportChannel": {
              "href": "http://localhost:8080/api/reports/cd4e6eea-990e-4c16-b99d-e8dd4a4da9d4/reportChannel"
          },
          "lossCausal": {
              "href": "http://localhost:8080/api/reports/cd4e6eea-990e-4c16-b99d-e8dd4a4da9d4/lossCausal"
          },
          "workshopStatus": {
              "href": "http://localhost:8080/api/reports/cd4e6eea-990e-4c16-b99d-e8dd4a4da9d4/workshopStatus"
          },
          "csEmployee": {
              "href": "http://localhost:8080/api/reports/cd4e6eea-990e-4c16-b99d-e8dd4a4da9d4/csEmployee"
          },
          "premium": {
              "href": "http://localhost:8080/api/reports/cd4e6eea-990e-4c16-b99d-e8dd4a4da9d4/premium"
          },
          "workshop": {
              "href": "http://localhost:8080/api/reports/cd4e6eea-990e-4c16-b99d-e8dd4a4da9d4/workshop"
          },
          "reportStatus": {
              "href": "http://localhost:8080/api/reports/cd4e6eea-990e-4c16-b99d-e8dd4a4da9d4/reportStatus"
          },
          "survey": {
              "href": "http://localhost:8080/api/reports/cd4e6eea-990e-4c16-b99d-e8dd4a4da9d4/survey"
          },
          "driver": {
              "href": "http://localhost:8080/api/reports/cd4e6eea-990e-4c16-b99d-e8dd4a4da9d4/driver"
          },
          "surveyorStatus": {
              "href": "http://localhost:8080/api/reports/cd4e6eea-990e-4c16-b99d-e8dd4a4da9d4/surveyorStatus"
          }
      }
  }
```

This endpoint create new report

### HTTP Request

`POST http://localhost:8080/api/reports`

Parameter | Description
--------- | -----------
grant_type| Set to refresh_token.
refresh_token | Fill with refresh token from request token.


## Update Report By Id

> Sample request

> Success response

This endpoint create new report

### HTTP Request

`POST http://localhost:8080/api/reports`

Parameter | Description
--------- | -----------
grant_type| Set to refresh_token.
refresh_token | Fill with refresh token from request token.

## Delete Report

> Sample request

> Success response

This endpoint create new report

### HTTP Request

`POST http://localhost:8080/api/reports`

Parameter | Description
--------- | -----------
grant_type| Set to refresh_token.
refresh_token | Fill with refresh token from request token.