## Add New Vehicle

This endpoint used to add new vehicle

> Sample request

```shell
curl "http://localhost:8080/api/vehicles"
  -X POST
  -H "Authorization: Bearer <token>"
  -H "Content-Type: application/json"
  -d '{
        "engineNumber":"R27T54318876",
        "chassisNumber":"ASDFG12309Y877458",
        "certificateNumber":"B4352282728928",
        "plateNumber":"B 7788 KKK",
        "yearModel":"2010",
        "vehicleSerie": "http://localhost:8080/api/vehicle-series/1",
        "vehicleColor" : "http://localhost:8080/api/vehicle-colors/1",
        "vehicleAssembly":"http://localhost:8080/api/vehicle-assemblies/1"
      }'
```

> Success response

```json
{
    "engineNumber": "R27T54318876",
    "chassisNumber": "ASDFG12309Y877458",
    "certificateNumber": "B4352282728928",
    "plateNumber": "B 7788 KKK",
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

Parameter | Description | Format
--------- | ----------- | ------
engineNumber | Fill with vehicle engine number | String
chassisNumber | Fill with vehicle chassis number | String
certificateNumber | Fill with vehicle certificate number | String
plateNumber | Fill with vehicle plate number | String
yearModel | Fill with vehicle year model | String
vehicleAssembly | Fill with vehicleAssembly object url id | String
vehicleColor | Fill with vehicleColor object url id | String
vehicleSerie | Fill with vehicleSerie object url id | String