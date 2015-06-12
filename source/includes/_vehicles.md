# Vehicles
## Get All Vehicles

This endpoint used to return all vehicles

> Sample request

```shell
curl "http://localhost:8080/api/vehicles"
  -H "Authorization: Bearer <token>"
```

> Success response

```json
{
  "_embedded": {
    "vehicles": [
      {
        "yearModel": "2015",
        "vehicleId": "937d15ef-2c04-40de-a5e6-3a34d5031345",
        "vehicleSerie": {
          "vehicleSerieType": "Test"
        },
        "vehicleAssembly": {
          "vehicleAssemblyType": "Test"
        },
        "vehicleColor": {
          "vehicleColorName": "White"
        },
        "engineNumber": "Test1111111",
        "chassisNumber": "Test111111",
        "certificateNumber": "Test11111",
        "plateNumber": "b1234kkk",
        "_links": {
          "self": {
            "href": "http://localhost:8080/api/vehicles/937d15ef-2c04-40de-a5e6-3a34d5031345{?projection}",
            "templated": true
          },
          "vehicleAssembly": {
            "href": "http://localhost:8080/api/vehicle-assemblies/1"
          },
          "vehicleColor": {
            "href": "http://localhost:8080/api/vehicle-colors/1"
          },
          "vehicleSerie": {
            "href": "http://localhost:8080/api/vehicle-series/1{?projection}",
            "templated": true
          }
        }
      }
    ]
  }
}
```

> Failed response

```json
{
  "error": "because"
}
```

### HTTP Request 

`GET http://localhost:8080/api/vehicles`

## Get a Specific Vehicle

This endpoint get vehicle by <code>vehicleId</code>

> Sample request

```shell
curl "http://localhost:8080/api/vehicles/<vehicleId>"
  -H "Authorization: Bearer <token>"
```

> Success response

```json
{
  "engineNumber": "Test1111111",
  "chassisNumber": "Test111111",
  "certificateNumber": "Test11111",
  "plateNumber": "b1234kkk",
  "yearModel": "2015",
  "_links": {
    "self": {
      "href": "http://localhost:8080/api/vehicles/937d15ef-2c04-40de-a5e6-3a34d5031345{?projection}",
      "templated": true
    },
    "vehicleAssembly": {
      "href": "http://localhost:8080/api/vehicle-assemblies/1"
    },
    "vehicleColor": {
      "href": "http://localhost:8080/api/vehicle-colors/1"
    },
    "vehicleSerie": {
      "href": "http://localhost:8080/api/vehicle-series/1{?projection}",
      "templated": true
    }
  }
}
```

> Failed response

```json
{
  "error": "because"
}
```

### HTTP Request

`GET http://localhost:8080/api/vehicles/<vehicleId>`

### URL Parameters

Parameter | Description
--------- | -----------
vehicleId | Selected vehicle id

## Add New Vehicle

This endpoint used to add new vehicle

> Sample request

```shell
curl "http://localhost:8080/api/vehicles"
  -X POST
  -H "Authorization: Bearer <token>"
  -H "Content-Type: application/json"
  -d '{
        "engineNumber":"123456789",
        "chassisNumber":"a1b2c3d4",
        "certificateNumber":"0999191991999",
        "plateNumber":"B1234ABC",
        "yearModel":"2010",
        "vehicleSerie": "http://localhost:8080/api/vehicle-series/1",
        "vehicleColor" : "http://localhost:8080/api/vehicle-colors/1",
        "vehicleAssembly":"http://localhost:8080/api/vehicle-assemblies/1"
      }'
```

> Success response

```json
  {
      "engineNumber": "123456789",
      "chassisNumber": "a1b2c3d4",
      "certificateNumber": "0999191991999",
      "plateNumber": "B1234ABC",
      "yearModel": "2010",
      "_links": {
          "self": {
              "href": "http://localhost:8080/api/vehicles/fa6a0d05-b700-47d8-abf9-1e19b250fd71{?projection}",
              "templated": true
          },
          "vehicleAssembly": {
              "href": "http://localhost:8080/api/vehicle-assemblies/1"
          },
          "vehicleColor": {
              "href": "http://localhost:8080/api/vehicle-colors/1"
          },
          "vehicleSerie": {
              "href": "http://localhost:8080/api/vehicle-series/1{?projection}",
              "templated": true
          }
      }
  }
```

> Failed response

```json
{
  "error": "because"
}
```

### HTTP Request

`POST http://localhost:8080/api/vehicles`

### Parameters

Parameter | Description
--------- | -----------
engineNumber | Fill with vehicle engine number
chassisNumber | Fill with vehicle chassis number
certificateNumber | Fill with vehicle certificate number
plateNumber | Fill with vehicle plate number
yearModel | Fill with vehicle year model
vehicleAssembly | Fill with vehicleAssembly object url id
vehicleColor | Fill with vehicleColor object url id
vehicleSerie | Fill with vehicleSerie object url id

## Update Vehicle

This endpoint used to update a vehicle object. It can update using <code>PUT</code> for full update or <code>PATCH</code> for partial update

> Sample request PUT

```shell
curl "http://localhost:8080/api/vehicles/<vehicleId>"
  -X PUT
  -H "Authorization: Bearer <token>"
  -H "Content-Type: application/json"
  -d '{
        "engineNumber":"12341234",
        "chassisNumber":"a1b2c3d4",
        "certificateNumber":"0999191991999",
        "plateNumber":"B1234ABC",
        "yearModel":"2010",
        "vehicleSerie": "http://localhost:8080/api/vehicle-series/1",
        "vehicleColor" : "http://localhost:8080/api/vehicle-colors/1",
        "vehicleAssembly":"http://localhost:8080/api/vehicle-assemblies/1"
      }'
```

> Sample request PATCH

```shell
curl "http://localhost:8080/api/vehicle/<vehicleId>"
  -X PATCH
  -H "Authorization: Bearer <token>"
  -H "Content-Type: application/json"
  -d '{
        "engineNumber":"12341234"
      }'
```

> Success response

```json
{
    "engineNumber": "12341234",
    "chassisNumber": "a1b2c3d4",
    "certificateNumber": "0999191991999",
    "plateNumber": "B1234ABC",
    "yearModel": "2010",
      "_links": {
          "self": {
              "href": "http://localhost:8080/api/vehicles/fa6a0d05-b700-47d8-abf9-1e19b250fd71{?projection}",
              "templated": true
          },
          "vehicleAssembly": {
              "href": "http://localhost:8080/api/vehicle-assemblies/1"
          },
          "vehicleColor": {
              "href": "http://localhost:8080/api/vehicle-colors/1"
          },
          "vehicleSerie": {
              "href": "http://localhost:8080/api/vehicle-series/1{?projection}",
              "templated": true
          }
      }
}
```

> Failed response

```json
{
  "error": "because"
}
```

### HTTP Request

`PUT http://localhost:8080/api/vehicles/<vehicleId>`

`PATCH http://localhost:8080/api/vehicles/<vehicleId>`

### URL Parameters

Parameter | Description
--------- | -----------
vehicleId | Selected vehicle id

### Parameters

Parameter | Description
--------- | -----------
engineNumber | Fill with vehicle engine number
chassisNumber | Fill with vehicle chassis number
certificateNumber | Fill with vehicle certificate number
plateNumber | Fill with vehicle plate number
yearModel | Fill with vehicle year model
vehicleAssembly | Fill with vehicleAssembly object url id
vehicleColor | Fill with vehicleColor object url id
vehicleSerie | Fill with vehicleSerie object url id

## Delete a Specific Vehicle

This endpoint delete vehicle object by <code>vehicleId</code>

> Sample request 

```shell
curl "http://localhost:8080/api/vehicles/<vehicleId>"
  -X DELETE
  -H "Authorization: Bearer <token>"
```

> Success response

```json
{
  "message":"deleted"
}
```

> Failed response

```json
{
  "error": "because"
}
```

### HTTP Request

`DELETE http://localhost:8080/api/vehicles/<vehicleId>`

### URL Parameters

Parameter | Description
--------- | -----------
vehicleId | Selected vehicle id