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