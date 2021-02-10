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
            "S": "TripRequest#TripRequestLocalTrip:LocalTrip#TripRequestStatus:DRAFTED#TripRequestRequesterName:Nana#TripRequestTravelMode:RentalCar#TripRequestCoveredByOther:CoveredByOwnCompany"
        },
        "TripRequestLocalTrip": {
            "S": "LocalTrip"
        },
        "TripRequestRequesterName": {
            "S": "Nana"
        },
        "TripRequestRequesterId": {
            "S": "93551f78-c2e2-4d47-bc5e-e2dad7ce5ba8"
        },
        "EntityItemId": {
            "S": "TripRequest:0b08932129b10a03ab2836efa16343e8"
        },
        "TripRequestStatus": {
            "S": "DRAFTED"
        },
        "TripRequestPurpose": {
            "S": "Test Trip Request"
        },
        "TripRequestReturnDateTime": {
            "S": "2021-02-03 10:30:00"
        },
        "TripRequestCoveredByOther": {
            "S": "CoveredByOwnCompany"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "TripRequestDepartureDateTime": {
            "S": "2021-01-31 8:03:00"
        },
        "TripRequestTravelMode": {
            "S": "RentalCar"
        },
        "TripRequestTripRoute": {
            "L": [
                {
                    "M": {
                        "Date": {
                            "S": "2021-02-09"
                        },
                        "Route": {
                            "L": [
                                {
                                    "M": {
                                        "From": {
                                            "M": {
                                                "LocationLevel1": {
                                                    "M": {
                                                        "LocationLevel1Id": {
                                                            "S": "b2d5cda7-5943-4b28-bf45-c41aaa7839b1"
                                                        },
                                                        "LocationLevel1Name": {
                                                            "S": "Takeo"
                                                        },
                                                        "LocationLevel2": {
                                                            "M": {
                                                                "LocationLevel2Id": {
                                                                    "S": "2108"
                                                                },
                                                                "LocationLevel3": {
                                                                    "M": {
                                                                        "LocationLevel3Id": {
                                                                            "S": "210802"
                                                                        },
                                                                        "LocationLevel3Name": {
                                                                            "S": "Sangkat Roka Knong"
                                                                        },
                                                                        "LocationLevel4": {
                                                                            "M": {
                                                                                "LocationLevel4Name": {
                                                                                    "S": "Snaor"
                                                                                },
                                                                                "LocationLevel4Id": {
                                                                                    "S": "21080212"
                                                                                }
                                                                            }
                                                                        }
                                                                    }
                                                                },
                                                                "LocationLevel2Name": {
                                                                    "S": "Krong Doun Kaev"
                                                                }
                                                            }
                                                        }
                                                    }
                                                }
                                            }
                                        },
                                        "To": {
                                            "M": {
                                                "LocationLevel1": {
                                                    "M": {
                                                        "LocationLevel1Id": {
                                                            "S": "ca2bc9a4-b6a3-4870-99e2-c038179d2068"
                                                        },
                                                        "LocationLevel1Name": {
                                                            "S": "Phnom Penh"
                                                        },
                                                        "LocationLevel2": {
                                                            "M": {
                                                                "LocationLevel2Id": {
                                                                    "S": "1206"
                                                                },
                                                                "LocationLevel3": {
                                                                    "M": {
                                                                        "LocationLevel3Id": {
                                                                            "S": "120611"
                                                                        },
                                                                        "LocationLevel3Name": {
                                                                            "S": "Boeng Tompun 1"
                                                                        },
                                                                        "LocationLevel4": {
                                                                            "M": {
                                                                                "LocationLevel4Name": {
                                                                                    "S": "Sansam Kosal I"
                                                                                },
                                                                                "LocationLevel4Id": {
                                                                                    "S": "12061106"
                                                                                }
                                                                            }
                                                                        }
                                                                    }
                                                                },
                                                                "LocationLevel2Name": {
                                                                    "S": "Khan Mean Chey"
                                                                }
                                                            }
                                                        }
                                                    }
                                                }
                                            }
                                        }
                                    }
                                },
                                {
                                    "M": {
                                        "From": {
                                            "M": {
                                                "LocationLevel1": {
                                                    "M": {
                                                        "LocationLevel1Id": {
                                                            "S": "ca2bc9a4-b6a3-4870-99e2-c038179d2068"
                                                        },
                                                        "LocationLevel1Name": {
                                                            "S": "Phnom Penh"
                                                        },
                                                        "LocationLevel2": {
                                                            "M": {
                                                                "LocationLevel2Id": {
                                                                    "S": "1206"
                                                                },
                                                                "LocationLevel3": {
                                                                    "M": {
                                                                        "LocationLevel3Id": {
                                                                            "S": "120611"
                                                                        },
                                                                        "LocationLevel3Name": {
                                                                            "S": "Boeng Tompun 1"
                                                                        },
                                                                        "LocationLevel4": {
                                                                            "M": {
                                                                                "LocationLevel4Name": {
                                                                                    "S": "Sansam Kosal I"
                                                                                },
                                                                                "LocationLevel4Id": {
                                                                                    "S": "12061106"
                                                                                }
                                                                            }
                                                                        }
                                                                    }
                                                                },
                                                                "LocationLevel2Name": {
                                                                    "S": "Khan Mean Chey"
                                                                }
                                                            }
                                                        }
                                                    }
                                                }
                                            }
                                        },
                                        "To": {
                                            "M": {
                                                "LocationLevel1": {
                                                    "M": {
                                                        "LocationLevel1Id": {
                                                            "S": "b2d5cda7-5943-4b28-bf45-c41aaa7839b1"
                                                        },
                                                        "LocationLevel1Name": {
                                                            "S": "Takeo"
                                                        },
                                                        "LocationLevel2": {
                                                            "M": {
                                                                "LocationLevel2Id": {
                                                                    "S": "2108"
                                                                },
                                                                "LocationLevel3": {
                                                                    "M": {
                                                                        "LocationLevel3Id": {
                                                                            "S": "210802"
                                                                        },
                                                                        "LocationLevel3Name": {
                                                                            "S": "Sangkat Roka Knong"
                                                                        },
                                                                        "LocationLevel4": {
                                                                            "M": {
                                                                                "LocationLevel4Name": {
                                                                                    "S": "Snaor"
                                                                                },
                                                                                "LocationLevel4Id": {
                                                                                    "S": "21080212"
                                                                                }
                                                                            }
                                                                        }
                                                                    }
                                                                },
                                                                "LocationLevel2Name": {
                                                                    "S": "Krong Doun Kaev"
                                                                }
                                                            }
                                                        }
                                                    }
                                                }
                                            }
                                        }
                                    }
                                }
                            ]
                        }
                    }
                },
                {
                    "M": {
                        "Date": {
                            "S": "2021-02-10"
                        },
                        "Route": {
                            "L": [
                                {
                                    "M": {
                                        "From": {
                                            "M": {
                                                "LocationLevel1": {
                                                    "M": {
                                                        "LocationLevel1Id": {
                                                            "S": "ca2bc9a4-b6a3-4870-99e2-c038179d2068"
                                                        },
                                                        "LocationLevel1Name": {
                                                            "S": "Phnom Penh"
                                                        },
                                                        "LocationLevel2": {
                                                            "M": {
                                                                "LocationLevel2Id": {
                                                                    "S": "1206"
                                                                },
                                                                "LocationLevel3": {
                                                                    "M": {
                                                                        "LocationLevel3Id": {
                                                                            "S": "120611"
                                                                        },
                                                                        "LocationLevel3Name": {
                                                                            "S": "Boeng Tompun 1"
                                                                        },
                                                                        "LocationLevel4": {
                                                                            "M": {
                                                                                "LocationLevel4Name": {
                                                                                    "S": "Sansam Kosal I"
                                                                                },
                                                                                "LocationLevel4Id": {
                                                                                    "S": "12061106"
                                                                                }
                                                                            }
                                                                        }
                                                                    }
                                                                },
                                                                "LocationLevel2Name": {
                                                                    "S": "Khan Mean Chey"
                                                                }
                                                            }
                                                        }
                                                    }
                                                }
                                            }
                                        },
                                        "To": {
                                            "M": {
                                                "LocationLevel1": {
                                                    "M": {
                                                        "LocationLevel1Id": {
                                                            "S": "b2d5cda7-5943-4b28-bf45-c41aaa7839b1"
                                                        },
                                                        "LocationLevel1Name": {
                                                            "S": "Phnom Penh"
                                                        },
                                                        "LocationLevel2": {
                                                            "M": {
                                                                "LocationLevel2Id": {
                                                                    "S": "2108"
                                                                },
                                                                "LocationLevel3": {
                                                                    "M": {
                                                                        "LocationLevel3Id": {
                                                                            "S": "210802"
                                                                        },
                                                                        "LocationLevel3Name": {
                                                                            "S": "Kraing Thnung"
                                                                        },
                                                                        "LocationLevel4": {
                                                                            "M": {
                                                                                "LocationLevel4Name": {
                                                                                    "S": "Kraing Angkrang"
                                                                                },
                                                                                "LocationLevel4Id": {
                                                                                    "S": "21080212"
                                                                                }
                                                                            }
                                                                        }
                                                                    }
                                                                },
                                                                "LocationLevel2Name": {
                                                                    "S": "Senson"
                                                                }
                                                            }
                                                        }
                                                    }
                                                }
                                            }
                                        }
                                    }
                                }
                            ]
                        }
                    }
                }
            ]
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
{
    "TripRequest": {
        "TripRequestLocalTrip": "LocalTrip",
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
            ],
            "Shop": [
                {
                    "ShopId": "d8d6f92d-c683-4480-bc45-8324599f550d",
                    "ShopName": "Sumsung"
                }
            ]
                
        }
    }

}
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
trip-request-id | The ID of the trip request to delete information

### HTTP Response
> The above HTTP request, if successful, will return Json structured like this:

# Trip Expense
## View Detail of Trip Expense

### HTTP Request
`GET v1/trip-requests/{trip_request_id}/tripExpense/{id}`

### Query Paramaeters
Parameter                           | Description
---------                           | -----------
trip_request_id                     | The ID of the trip request to retrieve information
id                                  | The ID of the trip expense to get info detail

### HTTP Response
> The above HTTP request, if successful, will return Json structured like this:

```json
{
    "data": [
        {
            "id": 41,
            "trip_request_id": 2,
            "date": "2021-01-26",
            "type": "Meal",
            "description": "Breakfast (2.00$), Lunch (5.00$), Diner (5.00$)",
            "amount": "10.00",
            "notes": null,
            "created_at": "2021-01-26T07:40:58.000000Z",
            "updated_at": "2021-01-26T07:40:58.000000Z"
        }
    ],
    "message": "Trip Expense retrieved Successfully"
}
```
## Record detail of Trip Expense

### HTTP Request
`GET v1/trip-requests/{trip_request_id}/tripExpense/{id}`

### Query Paramaeters
Parameter                           | Description
---------                           | -----------
trip_request_id                     | The ID of the trip request to retrieve information

### Body Request
```json
{
    "aiml:TripAllowance/TripGeoScope": "LocalTrip",
    "departureDate": "2020-12-31",
    "departureTime": "15:00:00",
    "returnDate": "2021-01-03",
    "returnTime": "11:30:00",
    "aiml:TripAllowance/CoveringAgent": "CoveredByOwnCompany",
    "travelSegment": "PhnomPenh-Takeo",
    "date":[
        {
            "aiml:TripAllowance/DepartureFrom": "PhnomPenh",
            "aiml:TripAllowance/DepartureDateTime": "2020-12-31 8:00",
            "aiml:TripAllowance/StayDate":"",
            "aiml:TripAllowance/ReturnFrom": "Takeo",
            "aiml:TripAllowance/ReturnDateTime": "2021-01-03 17:00",
            "aiml:TripAllowance/TravelDistance": "PhnomPenh-Takeo",
            "aiml:TripAllowance/InAreaTravelMode":"PublicTransport",
            "aiml:TripAllowance/NumberOfPeople": "1"
        }
    ],
    "param":"TripAllowance/Trip"
}
```
### HTTP Response
> The above HTTP request, if successful, will return Json structured like this:

```json
{
    "data": [
        {
            "id": 78,
            "trip_request_id": 2,
            "date": "2020-12-31",
            "type": "Travel Fee (Departure)",
            "description": "From Phnom Penh at 3:00 PM to Takeo",
            "amount": "5.00",
            "notes": null,
            "created_at": "2021-02-02T11:28:06.000000Z",
            "updated_at": "2021-02-02T11:28:06.000000Z"
        },
        {
            "id": 79,
            "trip_request_id": 2,
            "date": "2020-12-31",
            "type": "Meal",
            "description": "Breakfast (2.00$), Lunch (5.00$), Diner (5.00$)",
            "amount": "12.00",
            "notes": null,
            "created_at": "2021-02-02T11:28:06.000000Z",
            "updated_at": "2021-02-02T11:28:06.000000Z"
        },
        {
            "id": 80,
            "trip_request_id": 2,
            "date": "2020-12-31",
            "type": "In-area Travel",
            "description": "Travels in Takeo",
            "amount": "3.00",
            "notes": null,
            "created_at": "2021-02-02T11:28:06.000000Z",
            "updated_at": "2021-02-02T11:28:06.000000Z"
        },
        {
            "id": 81,
            "trip_request_id": 2,
            "date": "2020-12-31",
            "type": "Accommodation",
            "description": "Alone stay per night",
            "amount": "15.00",
            "notes": null,
            "created_at": "2021-02-02T11:28:06.000000Z",
            "updated_at": "2021-02-02T11:28:06.000000Z"
        },
        {
            "id": 82,
            "trip_request_id": 2,
            "date": "2021-01-01",
            "type": "Meal",
            "description": "Breakfast (2.00$), Lunch (5.00$), Diner (5.00$)",
            "amount": "12.00",
            "notes": null,
            "created_at": "2021-02-02T11:28:06.000000Z",
            "updated_at": "2021-02-02T11:28:06.000000Z"
        },
        {
            "id": 83,
            "trip_request_id": 2,
            "date": "2021-01-01",
            "type": "In-area Travel",
            "description": "Travels in Takeo",
            "amount": "3.00",
            "notes": null,
            "created_at": "2021-02-02T11:28:06.000000Z",
            "updated_at": "2021-02-02T11:28:06.000000Z"
        },
        {
            "id": 84,
            "trip_request_id": 2,
            "date": "2021-01-01",
            "type": "Accommodation",
            "description": "Alone stay per night",
            "amount": "15.00",
            "notes": null,
            "created_at": "2021-02-02T11:28:06.000000Z",
            "updated_at": "2021-02-02T11:28:06.000000Z"
        },
        {
            "id": 85,
            "trip_request_id": 2,
            "date": "2021-01-02",
            "type": "Meal",
            "description": "Breakfast (2.00$), Lunch (5.00$), Diner (5.00$)",
            "amount": "12.00",
            "notes": null,
            "created_at": "2021-02-02T11:28:06.000000Z",
            "updated_at": "2021-02-02T11:28:06.000000Z"
        },
        {
            "id": 86,
            "trip_request_id": 2,
            "date": "2021-01-02",
            "type": "In-area Travel",
            "description": "Travels in Takeo",
            "amount": "3.00",
            "notes": null,
            "created_at": "2021-02-02T11:28:06.000000Z",
            "updated_at": "2021-02-02T11:28:06.000000Z"
        },
        {
            "id": 87,
            "trip_request_id": 2,
            "date": "2021-01-02",
            "type": "Accommodation",
            "description": "Alone stay per night",
            "amount": "15.00",
            "notes": null,
            "created_at": "2021-02-02T11:28:06.000000Z",
            "updated_at": "2021-02-02T11:28:06.000000Z"
        },
        {
            "id": 88,
            "trip_request_id": 2,
            "date": "2021-01-03",
            "type": "Meal",
            "description": "Breakfast (2.00$), Lunch (5.00$), Diner (5.00$)",
            "amount": "2.00",
            "notes": null,
            "created_at": "2021-02-02T11:28:06.000000Z",
            "updated_at": "2021-02-02T11:28:06.000000Z"
        },
        {
            "id": 89,
            "trip_request_id": 2,
            "date": "2021-01-03",
            "type": "In-area Travel",
            "description": "Travels in Takeo",
            "amount": "3.00",
            "notes": null,
            "created_at": "2021-02-02T11:28:06.000000Z",
            "updated_at": "2021-02-02T11:28:06.000000Z"
        },
        {
            "id": 90,
            "trip_request_id": 2,
            "date": "2021-01-03",
            "type": "Accommodation",
            "description": "Alone stay per night",
            "amount": "0.00",
            "notes": null,
            "created_at": "2021-02-02T11:28:06.000000Z",
            "updated_at": "2021-02-02T11:28:06.000000Z"
        },
        {
            "id": 91,
            "trip_request_id": 2,
            "date": "2021-01-03",
            "type": "Travel Fee (Return)",
            "description": "From Takeo at 11:30 AM to Phnom Penh",
            "amount": "5.00",
            "notes": null,
            "created_at": "2021-02-02T11:28:06.000000Z",
            "updated_at": "2021-02-02T11:28:06.000000Z"
        }
    ],
    "message": "Trip Adlevel1 Created Successfully"
}
```

## Update the Trip Expense by id

### HTTP Request
`PUT v1/trip-requests/{trip_request_id}/tripExpense/{id}`

### Query Paramaeters
Parameter                           | Description
---------                           | -----------
trip_request_id                     | The ID of the trip request to retrieve information
id                                  | The ID of the trip expense to update information

### Body Request
```json
{
    "amount": "10.00",
    "notes": "Test amount"
}
```
### HTTP Response
> The above HTTP request, if successful, will return Json structured like this:

```json
{
    "data": {
        "id": 88,
        "trip_request_id": 2,
        "date": "2021-01-03",
        "type": "Meal",
        "description": "Breakfast (2.00$), Lunch (5.00$), Diner (5.00$)",
        "amount": "10.00",
        "notes": "Test amount",
        "created_at": "2021-02-02T11:28:06.000000Z",
        "updated_at": "2021-02-03T01:34:36.000000Z"
    },
    "message": "Trip Expense Updated Successfully"
}
```

# Countries
## Get All Countries

### HTTP Request
`GET organization-svc/api/locations/countries`

### HTTP Response
> The above HTTP request, if successful, will return Json structured like this:

```json
[
    {
        "CountryIso_3166_2": {
            "S": "SB"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "EntityItemId": {
            "S": "Country:0003a74397fab2aa0d15c2d383c36eef"
        },
        "CountryIso_3166_3": {
            "S": "SLB"
        },
        "CountryName": {
            "S": "Solomon Islands"
        }
    },
    {
        "CountryIso_3166_2": {
            "S": "CN"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "EntityItemId": {
            "S": "Country:00c763e8e6895f6224cc56eef69d37c2"
        },
        "CountryIso_3166_3": {
            "S": "CHN"
        },
        "CountryName": {
            "S": "China"
        }
    },
    {
        "CountryIso_3166_2": {
            "S": "NR"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "EntityItemId": {
            "S": "Country:00e8c77c4aa9534224b424fe0ad6623f"
        },
        "CountryIso_3166_3": {
            "S": "NRU"
        },
        "CountryName": {
            "S": "Nauru"
        }
    }
]
```

# Province
## Get All Province

### HTTP Request
`GET organization-svc/api/locations/provinces`

### HTTP Response
> The above HTTP request, if successful, will return Json structured like this:

```json
[
    {
        "LocationLevel1Code": {
            "S": "03"
        },
        "EntityItemId": {
            "S": "LocationLevel1:67189629fc119919e1c8a2d65c80402f"
        },
        "CompositeAccessPatterns": {
            "S": "LocationLevel1#Country:e05d7f46e40731dd0ae0760543eb5596#CountryName:Cambodia"
        },
        "CountryName": {
            "S": "Cambodia"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "CountryId": {
            "S": "Country:e05d7f46e40731dd0ae0760543eb5596"
        },
        "LocationLevel1Name": {
            "S": "Kampong Cham"
        },
        "LocationLevel1KhmerName": {
            "S": "កំពង់ចាម"
        }
    },
    {
        "LocationLevel1Code": {
            "S": "02"
        },
        "EntityItemId": {
            "S": "LocationLevel1:7ed870110dc3d34491b73fe37f02f370"
        },
        "CompositeAccessPatterns": {
            "S": "LocationLevel1#Country:e05d7f46e40731dd0ae0760543eb5596#CountryName:Cambodia"
        },
        "CountryName": {
            "S": "Cambodia"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "CountryId": {
            "S": "Country:e05d7f46e40731dd0ae0760543eb5596"
        },
        "LocationLevel1Name": {
            "S": "Battambang"
        },
        "LocationLevel1KhmerName": {
            "S": "បាត់ដំបង"
        }
    },
    {
        "LocationLevel1Code": {
            "S": "01"
        },
        "EntityItemId": {
            "S": "LocationLevel1:fee79c83882b347f5bf2c4fd8cb3566f"
        },
        "CompositeAccessPatterns": {
            "S": "LocationLevel1#Country:e05d7f46e40731dd0ae0760543eb5596#CountryName:Cambodia"
        },
        "CountryName": {
            "S": "Cambodia"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "CountryId": {
            "S": "Country:e05d7f46e40731dd0ae0760543eb5596"
        },
        "LocationLevel1Name": {
            "S": "Banteay Meanchey"
        },
        "LocationLevel1KhmerName": {
            "S": "បន្ទាយមានជ័យ"
        }
    }
]
```
### HTTP Request Filter 
`GET organization-svc/api/locations/provinces?contains=Country:e05d7f46e40731dd0ae0760543eb5596#CountryName:Cambodia`

### Query Paramaeters
Parameter                   | Description
---------                   | -----------
Country                     | Is the id of the country that covert to uuid.
CountryName                 | Is the name of the country.

### HTTP Response Filter
> The above HTTP request, if successful, will return Json structured like this:

```json
[
{
        "LocationLevel1Code": {
            "S": "13"
        },
        "EntityItemId": {
            "S": "LocationLevel1:0ab897ddf8a29241d630ab4429c4b0d9"
        },
        "CompositeAccessPatterns": {
            "S": "LocationLevel1#Country:e05d7f46e40731dd0ae0760543eb5596#CountryName:Cambodia"
        },
        "CountryName": {
            "S": "Cambodia"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "CountryId": {
            "S": "Country:e05d7f46e40731dd0ae0760543eb5596"
        },
        "LocationLevel1Name": {
            "S": "Preah Vihear"
        },
        "LocationLevel1KhmerName": {
            "S": "ព្រះវិហារ"
        }
    },
    {
        "LocationLevel1Code": {
            "S": "11"
        },
        "EntityItemId": {
            "S": "LocationLevel1:111b3abe7795b6231a75523c37148713"
        },
        "CompositeAccessPatterns": {
            "S": "LocationLevel1#Country:e05d7f46e40731dd0ae0760543eb5596#CountryName:Cambodia"
        },
        "CountryName": {
            "S": "Cambodia"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "CountryId": {
            "S": "Country:e05d7f46e40731dd0ae0760543eb5596"
        },
        "LocationLevel1Name": {
            "S": "Mondul Kiri"
        },
        "LocationLevel1KhmerName": {
            "S": "មណ្ឌលគិរី"
        }
    }
]
```

# Districts
## Get All districts

### HTTP Request
`GET organization-svc/api/locations/districts`

### HTTP Response
> The above HTTP request, if successful, will return Json structured like this:

```json
[
    {
        "LocationLevel2KhmerName": {
            "S": "ស្រីសន្ធរ"
        },
        "LocationLevel1Id": {
            "S": "LocationLevel1:67189629fc119919e1c8a2d65c80402f"
        },
        "EntityItemId": {
            "S": "LocationLevel2:029d52772c42cf101560c4c52d929d5d"
        },
        "CompositeAccessPatterns": {
            "S": "LocationLevel2#LocationLevel1:67189629fc119919e1c8a2d65c80402f#LocationLevel1Name:Kampong Cham"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "LocationLevel1Name": {
            "S": "Kampong Cham"
        },
        "LocationLevel2Name": {
            "S": "Srei Santhor"
        },
        "LocationLevel2Code": {
            "S": "0314"
        }
    },
    {
        "LocationLevel2KhmerName": {
            "S": "ភ្នំស្រុក"
        },
        "LocationLevel1Id": {
            "S": "LocationLevel1:fee79c83882b347f5bf2c4fd8cb3566f"
        },
        "EntityItemId": {
            "S": "LocationLevel2:03c340c1c96e51312d7113f980b5eb5e"
        },
        "CompositeAccessPatterns": {
            "S": "LocationLevel2#LocationLevel1:fee79c83882b347f5bf2c4fd8cb3566f#LocationLevel1Name:Banteay Meanchey"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "LocationLevel1Name": {
            "S": "Banteay Meanchey"
        },
        "LocationLevel2Name": {
            "S": "Phnum Srok"
        },
        "LocationLevel2Code": {
            "S": "0103"
        }
    }
]
```

### HTTP Request Filter 
`GET organization-svc/api/locations/districts?contains=LocationLevel1:422886d8599c6cb51557a0da3423f43c#LocationLevel1Name:Takeo`

### Query Paramaeters
Parameter                   | Description
---------                   | -----------
LocationLevel1              | Is the id of the province that covert to uuid.
LocationLevel1Name          | Is the name of the province.

### HTTP Response Filter
> The above HTTP request, if successful, will return Json structured like this:

```json
[
    {
        "LocationLevel2KhmerName": {
            "S": "ដូនកែវ"
        },
        "LocationLevel1Id": {
            "S": "LocationLevel1:422886d8599c6cb51557a0da3423f43c"
        },
        "EntityItemId": {
            "S": "LocationLevel2:0b289bfd5d789cb4d5436d7f426ad839"
        },
        "CompositeAccessPatterns": {
            "S": "LocationLevel2#LocationLevel1:422886d8599c6cb51557a0da3423f43c#LocationLevel1Name:Takeo"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "LocationLevel1Name": {
            "S": "Takeo"
        },
        "LocationLevel2Name": {
            "S": "Doun Kaev"
        },
        "LocationLevel2Code": {
            "S": "2108"
        }
    },
    {
        "LocationLevel2KhmerName": {
            "S": "បាទី"
        },
        "LocationLevel1Id": {
            "S": "LocationLevel1:422886d8599c6cb51557a0da3423f43c"
        },
        "EntityItemId": {
            "S": "LocationLevel2:706c8226fa639cc261f056025151aa62"
        },
        "CompositeAccessPatterns": {
            "S": "LocationLevel2#LocationLevel1:422886d8599c6cb51557a0da3423f43c#LocationLevel1Name:Takeo"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "LocationLevel1Name": {
            "S": "Takeo"
        },
        "LocationLevel2Name": {
            "S": "Bati"
        },
        "LocationLevel2Code": {
            "S": "2102"
        }
    }
]
```

# Communes
## Get All communes

### HTTP Request
`GET organization-svc/api/locations/communes`

### HTTP Response
> The above HTTP request, if successful, will return Json structured like this:

```json
[
    {
        "LocationLevel3Name": {
            "S": "Damril"
        },
        "EntityItemId": {
            "S": "LocationLevel3:001922002831aae1fe4f6d660d32456d"
        },
        "LocationLevel2Id": {
            "S": "LocationLevel2:73b7d51328eab8c2b34fbb51bc2ccefb"
        },
        "CompositeAccessPatterns": {
            "S": "LocationLevel3#LocationLevel2:73b7d51328eab8c2b34fbb51bc2ccefb#LocationLevel2Name:Ou Reang Ov"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "LocationLevel2Name": {
            "S": "Ou Reang Ov"
        },
        "LocationLevel3KhmerName": {
            "S": "ដំរិល"
        },
        "LocationLevel3Code": {
            "S": "250403"
        }
    },
    {
        "LocationLevel3Name": {
            "S": "Krang Dei Vay"
        },
        "EntityItemId": {
            "S": "LocationLevel3:00b27092931ce4550ffca0afe8928c40"
        },
        "LocationLevel2Id": {
            "S": "LocationLevel2:43415b8b6ab8b1c9e542f7da5eb136d5"
        },
        "CompositeAccessPatterns": {
            "S": "LocationLevel3#LocationLevel2:43415b8b6ab8b1c9e542f7da5eb136d5#LocationLevel2Name:Phnum Sruoch"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "LocationLevel2Name": {
            "S": "Phnum Sruoch"
        },
        "LocationLevel3KhmerName": {
            "S": "ក្រាំងដីវ៉ាយ"
        },
        "LocationLevel3Code": {
            "S": "050605"
        }
    }
]
```
### HTTP Request Filter 
`GET organization-svc/api/locations/communes?contains=LocationLevel2:0b289bfd5d789cb4d5436d7f426ad839#LocationLevel2Name:Doun Kaev`

### Query Paramaeters
Parameter                   | Description
---------                   | -----------
LocationLevel2              | Is the id of the district that covert to uuid.
LocationLevel2Name          | Is the name of the district.

### HTTP Response Filter
> The above HTTP request, if successful, will return Json structured like this:

```json
[
    {
        "LocationLevel3Name": {
            "S": "Roka Knong"
        },
        "EntityItemId": {
            "S": "LocationLevel3:0974848effdedabe74730bfe597b7067"
        },
        "LocationLevel2Id": {
            "S": "LocationLevel2:0b289bfd5d789cb4d5436d7f426ad839"
        },
        "CompositeAccessPatterns": {
            "S": "LocationLevel3#LocationLevel2:0b289bfd5d789cb4d5436d7f426ad839#LocationLevel2Name:Doun Kaev"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "LocationLevel2Name": {
            "S": "Doun Kaev"
        },
        "LocationLevel3KhmerName": {
            "S": "រកាក្នុង"
        },
        "LocationLevel3Code": {
            "S": "210802"
        }
    },
    {
        "LocationLevel3Name": {
            "S": "Roka Krau"
        },
        "EntityItemId": {
            "S": "LocationLevel3:39c5749804bc8318c94a9fcba70d069a"
        },
        "LocationLevel2Id": {
            "S": "LocationLevel2:0b289bfd5d789cb4d5436d7f426ad839"
        },
        "CompositeAccessPatterns": {
            "S": "LocationLevel3#LocationLevel2:0b289bfd5d789cb4d5436d7f426ad839#LocationLevel2Name:Doun Kaev"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "LocationLevel2Name": {
            "S": "Doun Kaev"
        },
        "LocationLevel3KhmerName": {
            "S": "រកាក្រៅ"
        },
        "LocationLevel3Code": {
            "S": "210803"
        }
    },
    {
        "LocationLevel3Name": {
            "S": "Baray"
        },
        "EntityItemId": {
            "S": "LocationLevel3:d6440f5391b68e53822f4451fc039ecb"
        },
        "LocationLevel2Id": {
            "S": "LocationLevel2:0b289bfd5d789cb4d5436d7f426ad839"
        },
        "CompositeAccessPatterns": {
            "S": "LocationLevel3#LocationLevel2:0b289bfd5d789cb4d5436d7f426ad839#LocationLevel2Name:Doun Kaev"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "LocationLevel2Name": {
            "S": "Doun Kaev"
        },
        "LocationLevel3KhmerName": {
            "S": "បារាយណ៍"
        },
        "LocationLevel3Code": {
            "S": "210801"
        }
    }
]
```
# Villages
## Get All villages

### HTTP Request
`GET organization-svc/api/locations/villages`

### HTTP Response
> The above HTTP request, if successful, will return Json structured like this:

```json
[
    {
        "LocationLevel3Name": {
            "S": "Rohal"
        },
        "EntityItemId": {
            "S": "LocationLevel4:00010964629e272de1c53626cf9284e2"
        },
        "CompositeAccessPatterns": {
            "S": "LocationLevel4#LocationLevel3:f6d397999fbabfbfa3ce9c17bce7b3d8#LocationLevel3Name:Rohal"
        },
        "LocationLevel4KhmerName": {
            "S": "ស្នាយ"
        },
        "LocationLevel4Code": {
            "S": "01040605"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "LocationLevel3Id": {
            "S": "LocationLevel3:f6d397999fbabfbfa3ce9c17bce7b3d8"
        },
        "LocationLevel4Name": {
            "S": "Snay"
        }
    },
    {
        "LocationLevel3Name": {
            "S": "Ou Mlu"
        },
        "EntityItemId": {
            "S": "LocationLevel4:00099b4b2b8c0a44beea20294a9bb8a2"
        },
        "CompositeAccessPatterns": {
            "S": "LocationLevel4#LocationLevel3:b4397a4cc8406529514cd8cbe6fc156b#LocationLevel3Name:Ou Mlu"
        },
        "LocationLevel4KhmerName": {
            "S": "អូរប្រឡោះ"
        },
        "LocationLevel4Code": {
            "S": "03150605"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "LocationLevel3Id": {
            "S": "LocationLevel3:b4397a4cc8406529514cd8cbe6fc156b"
        },
        "LocationLevel4Name": {
            "S": "Ou Pralaoh"
        }
    },
    {
        "LocationLevel3Name": {
            "S": "Sragnae"
        },
        "EntityItemId": {
            "S": "LocationLevel4:000ddaddb43521b970359cdd9be7476f"
        },
        "CompositeAccessPatterns": {
            "S": "LocationLevel4#LocationLevel3:c0e60fc6c03d6c9608e678e70f3e3986#LocationLevel3Name:Sragnae"
        },
        "LocationLevel4KhmerName": {
            "S": "ត្រពាំងរូង"
        },
        "LocationLevel4Code": {
            "S": "03131208"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "LocationLevel3Id": {
            "S": "LocationLevel3:c0e60fc6c03d6c9608e678e70f3e3986"
        },
        "LocationLevel4Name": {
            "S": "Trapeang Rung"
        }
    }
]
```

### HTTP Request Filter 
`GET organization-svc/api/locations/villages?contains=LocationLevel3:d6440f5391b68e53822f4451fc039ecb#LocationLevel3Name:Baray Kaev`

### Query Paramaeters
Parameter                   | Description
---------                   | -----------
LocationLevel3              | Is the id of the communes that covert to uuid.
LocationLevel3Name          | Is the name of the communes.

### HTTP Response Filter
> The above HTTP request, if successful, will return Json structured like this:

```json
[
    {
        "LocationLevel3Name": {
            "S": "Baray"
        },
        "EntityItemId": {
            "S": "LocationLevel4:08a398d5762b83b247714472094ff015"
        },
        "CompositeAccessPatterns": {
            "S": "LocationLevel4#LocationLevel3:d6440f5391b68e53822f4451fc039ecb#LocationLevel3Name:Baray"
        },
        "LocationLevel4KhmerName": {
            "S": "ក្រាំងតាពូង"
        },
        "LocationLevel4Code": {
            "S": "21080113"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "LocationLevel3Id": {
            "S": "LocationLevel3:d6440f5391b68e53822f4451fc039ecb"
        },
        "LocationLevel4Name": {
            "S": "Krang Ta Pung"
        }
    },
    {
        "LocationLevel3Name": {
            "S": "Baray"
        },
        "EntityItemId": {
            "S": "LocationLevel4:0aee6625d7809bd49453f77b42554492"
        },
        "CompositeAccessPatterns": {
            "S": "LocationLevel4#LocationLevel3:d6440f5391b68e53822f4451fc039ecb#LocationLevel3Name:Baray"
        },
        "LocationLevel4KhmerName": {
            "S": "ជ្រោយប្រឃរ"
        },
        "LocationLevel4Code": {
            "S": "21080104"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "LocationLevel3Id": {
            "S": "LocationLevel3:d6440f5391b68e53822f4451fc039ecb"
        },
        "LocationLevel4Name": {
            "S": "Chrouy Prakhor"
        }
    },
    {
        "LocationLevel3Name": {
            "S": "Baray"
        },
        "EntityItemId": {
            "S": "LocationLevel4:10077a6ce405bbb3d4465d52715ab798"
        },
        "CompositeAccessPatterns": {
            "S": "LocationLevel4#LocationLevel3:07bdde0902576757d6deff54f884bda7#LocationLevel3Name:Baray"
        },
        "LocationLevel4KhmerName": {
            "S": "ពោធិ៍ពីរ"
        },
        "LocationLevel4Code": {
            "S": "06010311"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "LocationLevel3Id": {
            "S": "LocationLevel3:07bdde0902576757d6deff54f884bda7"
        },
        "LocationLevel4Name": {
            "S": "Pou Pir"
        }
    }
]
```
