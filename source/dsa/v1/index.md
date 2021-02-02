# DSA API Documentation

# Introduction
This document guides you on how to work with resources at the backend of DSA service via API endpoints. Those resources include Trip Requests, etc.

# Authentication
### Header Request
Key             | Value
----            | -----
Authorization   | Bearer Token
Content-Type    | application/json    

# Trip requests
## Get all Trip Request

### HTTP Request
`GET dsa-svc/api/v1/trip-requests`

### Query Paramaeters
Parameter                   | Description
---------                   | -----------
TripRequestDestination      | Is the destination you go to trip.
TripRequestStatus           | Requester has the status DRAFTED, APPROVED, and REJECTED.
TripRequestRequesterName    | Is the name of creator trip request.


### HTTP Response
> The above HTTP request, if successful, will return Json structured like this:

```json
[
    {
        "CompositeAccessPatterns": {
            "S": "TripRequest#TripRequestLocalTrip:Local#TripRequestStatus:DRAFTED#TripRequestRequesterName:Son#TripRequestTravelMode:PublicTransport#TripRequestCoveredByOther:CoveredByOwnCompany"
        },
        "TripRequestLocalTrip": {
            "S": "Local"
        },
        "TripRequestRequesterName": {
            "S": "Son"
        },
        "TripRequestRequesterId": {
            "S": "2"
        },
        "EntityItemId": {
            "S": "TripRequest:9866369c5fe5329d740f6ea9a5ebebd3"
        },
        "TripRequestStatus": {
            "S": "DRAFTED"
        },
        "TripRequestPurpose": {
            "S": "Test"
        },
        "TripRequestReturnDateTime": {
            "S": "2021-01-30 10:03:00"
        },
        "TripRequestNotes": {
            "S": "Test"
        },
        "TripRequestCoveredByOther": {
            "S": "CoveredByOwnCompany"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "TripRequestDepartureDateTime": {
            "S": "2021-01-28 10:03:00"
        },
        "TripRequestTravelMode": {
            "S": "PublicTransport"
        }
    },
    {
        "CompositeAccessPatterns": {
            "S": "TripRequest#TripRequestLocalTrip:Local#TripRequestStatus:DRAFTED#TripRequestRequesterName:Son#TripRequestTravelMode:PublicTransport#TripRequestCoveredByOther:CoveredByOwnCompany#TripRequestDestination:Siem Reap#TripRequestJoinTraveler:Sreyta"
        },
        "TripRequestJoinTraveler": {
            "S": "Sreyta"
        },
        "TripRequestLocalTrip": {
            "S": "Local"
        },
        "TripRequestRequesterName": {
            "S": "Son"
        },
        "TripRequestRequesterId": {
            "S": "2"
        },
        "EntityItemId": {
            "S": "TripRequest:b1fbe6c8cad2b1c7ee99d13ee881cc54"
        },
        "TripRequestStatus": {
            "S": "DRAFTED"
        },
        "TripRequestPurpose": {
            "S": "Test"
        },
        "TripRequestReturnDateTime": {
            "S": "2021-01-30 10:03:00"
        },
        "TripRequestDestination": {
            "S": "Siem Reap"
        },
        "TripRequestCoveredByOther": {
            "S": "CoveredByOwnCompany"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "TripRequestDepartureDateTime": {
            "S": "2021-01-28 10:03:00"
        },
        "TripRequestTravelMode": {
            "S": "PublicTransport"
        }
    },
    {
        "CompositeAccessPatterns": {
            "S": "TripRequest#TripRequestLocalTrip:Local#TripRequestStatus:DRAFTED#TripRequestRequesterName:Rotha#TripRequestTravelMode:RentalCar#TripRequestCoveredByOther:CoveredByOwnCompany#TripRequestDestination:Takeo#TripRequestJoinTraveler:Samai"
        },
        "TripRequestJoinTraveler": {
            "S": "Samai"
        },
        "TripRequestLocalTrip": {
            "S": "Local"
        },
        "TripRequestRequesterName": {
            "S": "Rotha"
        },
        "TripRequestRequesterId": {
            "S": "3"
        },
        "EntityItemId": {
            "S": "TripRequest:f2b6b297c3b286f293a4955a02b9fab3"
        },
        "TripRequestStatus": {
            "S": "DRAFTED"
        },
        "TripRequestPurpose": {
            "S": "Test"
        },
        "TripRequestReturnDateTime": {
            "S": "2021-01-30 10:03:00"
        },
        "TripRequestDestination": {
            "S": "Takeo"
        },
        "TripRequestCoveredByOther": {
            "S": "CoveredByOwnCompany"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "TripRequestDepartureDateTime": {
            "S": "2021-01-28 10:03:00"
        },
        "TripRequestTravelMode": {
            "S": "RentalCar"
        }
    }
]
```

### HTTP Request Filter 
`GET dsa-svc/api/v1/trip-requests?contains=TripRequestRequesterName:Son`

### HTTP Response Filter
> The above HTTP request, if successful, will return Json structured like this:

```json
[
    {
        "CompositeAccessPatterns": {
            "S": "TripRequest#TripRequestLocalTrip:Local#TripRequestStatus:DRAFTED#TripRequestRequesterName:Son#TripRequestTravelMode:PublicTransport#TripRequestCoveredByOther:CoveredByOwnCompany"
        },
        "TripRequestLocalTrip": {
            "S": "Local"
        },
        "TripRequestRequesterName": {
            "S": "Son"
        },
        "TripRequestRequesterId": {
            "S": "2"
        },
        "EntityItemId": {
            "S": "TripRequest:9866369c5fe5329d740f6ea9a5ebebd3"
        },
        "TripRequestStatus": {
            "S": "DRAFTED"
        },
        "TripRequestPurpose": {
            "S": "Test"
        },
        "TripRequestReturnDateTime": {
            "S": "2021-01-30 10:03:00"
        },
        "TripRequestNotes": {
            "S": "Test"
        },
        "TripRequestCoveredByOther": {
            "S": "CoveredByOwnCompany"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "TripRequestDepartureDateTime": {
            "S": "2021-01-28 10:03:00"
        },
        "TripRequestTravelMode": {
            "S": "PublicTransport"
        }
    },
    {
        "CompositeAccessPatterns": {
            "S": "TripRequest#TripRequestLocalTrip:Local#TripRequestStatus:DRAFTED#TripRequestRequesterName:Son#TripRequestTravelMode:PublicTransport#TripRequestCoveredByOther:CoveredByOwnCompany#TripRequestDestination:Siem Reap#TripRequestJoinTraveler:Sreyta"
        },
        "TripRequestJoinTraveler": {
            "S": "Sreyta"
        },
        "TripRequestLocalTrip": {
            "S": "Local"
        },
        "TripRequestRequesterName": {
            "S": "Son"
        },
        "TripRequestRequesterId": {
            "S": "2"
        },
        "EntityItemId": {
            "S": "TripRequest:b1fbe6c8cad2b1c7ee99d13ee881cc54"
        },
        "TripRequestStatus": {
            "S": "DRAFTED"
        },
        "TripRequestPurpose": {
            "S": "Test"
        },
        "TripRequestReturnDateTime": {
            "S": "2021-01-30 10:03:00"
        },
        "TripRequestDestination": {
            "S": "Siem Reap"
        },
        "TripRequestCoveredByOther": {
            "S": "CoveredByOwnCompany"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "TripRequestDepartureDateTime": {
            "S": "2021-01-28 10:03:00"
        },
        "TripRequestTravelMode": {
            "S": "PublicTransport"
        }
    }
]
```


## Create Trip Request
### HTTP Request
`POST dsa-svc/api/v1/trip-requests`

### Body Request

```json
[
    {
        "TripRequest": {
            "TripRequestLocalTrip": "Local",
            "TripRequestDepartureDateTime": "2021-01-31 8:03:00",
            "TripRequestReturnDateTime": "2021-02-03 10:30:00",
            "TripRequestStatus": "DRAFTED",
            "TripRequestRequesterId": "93551f78-c2e2-4d47-bc5e-e2dad7ce5ba8",
            "TripRequestRequesterName": "Nana",
            "TripRequestPurpose": "Test Trip Request",
            "TripRequestTravelMode": "RentalCar",
            "TripRequestCoveredByOther": "CoveredByOwnCompany",
            "Children": {
                "TripRoute": [
                    {
                        "Date": "2021-01-31",
                        "Route": [
                            { 
                                "From": {
                                    "LocationLevel1": {
                                        "LocationLevel1Id": "b2d5cda7-5943-4b28-bf45-c41aaa7839b1",
                                        "LocationLevel1Name": "Takeo",
                                        "LocationLevel2": {
                                            "LocationLevel2Id": "2108",
                                            "LocationLevel2Name": "Krong Doun Kaev",
                                            "LocationLevel3": {
                                                "LocationLevel3Id": "210802",
                                                "LocationLevel3Name": "Sangkat Roka Knong",
                                                "LocationLevel4": {
                                                    "LocationLevel4Id": "21080212",
                                                    "LocationLevel4Name": "Snaor"
                                                }
                                            }
                                        }
                                    }
                                },
                                "To": {
                                    "LocationLevel1": {
                                        "LocationLevel1Id": "ca2bc9a4-b6a3-4870-99e2-c038179d2068",
                                        "LocationLevel1Name": "Phnom Penh",
                                        "LocationLevel2": {
                                            "LocationLevel2Id": "1206",
                                            "LocationLevel2Name": "Khan Mean Chey",
                                            "LocationLevel3": {
                                                "LocationLevel3Id": "120611",
                                                "LocationLevel3Name": "Boeng Tompun 1",
                                                "LocationLevel4": {
                                                    "LocationLevel4Id": "12061106",
                                                    "LocationLevel4Name": "Sansam Kosal I"
                                                }
                                            }
                                        }
                                    }
                                }
                            }
                        ]
                    }
                ],
                "JointTraveler": [
                    {
                        "JointTravelerEmployeePersonId": "d8d6f92d-c683-4480-bc45-8324599f550d",
                        "JointTravelerPersonName": "Lily"
                    }
                ]
            }
        }
    }
]
```

### HTTP Response
> The above HTTP request, if successful, will return Json structured like this:

```json
    [
        {
            "ConsumedCapacity": {
                "TableName": "DsaDev",
                "CapacityUnits": 1
            },
            "@metadata": {
                "statusCode": 200,
                "effectiveUri": "https://dynamodb.ap-southeast-1.amazonaws.com",
                "headers": {
                    "server": "Server",
                    "date": "Fri, 29 Jan 2021 03:42:05 GMT",
                    "content-type": "application/x-amz-json-1.0",
                    "content-length": "63",
                    "connection": "keep-alive",
                    "x-amzn-requestid": "K7RJCER1N6EE23VO284K9S7NPVVV4KQNSO5AEMVJF66Q9ASUAAJG",
                    "x-amz-crc32": "3143598553"
                },
                "transferStats": {
                    "http": [
                        []
                    ]
                }
            }
        }
    ]
```

## Update Trip Request

### HTTP Request
`PUT dsa-svc/api/v1/trip-requests/{trip-request-id}`

### Query Paramaeters
Parameter       | Description
---------       | -----------
trip-request-id | The ID of the trip request to update information

### Body Request


### HTTP Response
> The above HTTP request, if successful, will return Json structured like this:

## Get Info Detail Of Trip Request
### HTTP Request
`GET dsa-svc/api/v1/trip-requests/{trip-request-id}`

### Query Paramaeters
Parameter       | Description
---------       | -----------
trip-request-id | The ID of the trip request to update information

### HTTP Response
> The above HTTP request, if successful, will return Json structured like this:

## Delete Info Of Trip Request
### HTTP Request
`DELETE dsa-svc/api/v1/trip-requests/{trip-request-id}`

### Query Paramaeters
Parameter       | Description
---------       | -----------
trip-request-id | The ID of the trip request to delte information

### HTTP Response
> The above HTTP request, if successful, will return Json structured like this:

# Trip Expense


# AdministrativeDivision1stLevel
## Get All AdLevel1

### HTTP Request
`GET dsa-svc/api/v1/adLevel1`

### Query Paramaeters
Parameter                           | Description
---------                           | -----------
AdministrativeDivision1stLevelName  | Is the name of autonomous municipality and province
### HTTP Response
> The above HTTP request, if successful, will return Json structured like this:


