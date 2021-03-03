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

### Body Request

```json 
{
    "Resource": "aiml:dsa:trip-request/*",
    "Operation": "dsa:item-operation:Retrieve"
}
```
            
### HTTP Response
> The above HTTP request, if successful, will return Json structured like this:

```json
[
    {
        "CompositeAccessPatterns": {
            "S": "TripRequest#TripRequestLocalTrip:LocalTrip#TripRequestStatus:Drafted#TripRequestRequesterName:Sreyta#TripRequestTravelMode:PublicTransport#TripRequestCoveredByOther:CoveredByOwnCompany"
        },
        "TripRequestLocalTrip": {
            "S": "LocalTrip"
        },
        "TripRequestRequesterName": {
            "S": "Sreyta"
        },
        "TripRequestRequesterId": {
            "S": "93551f78-c2e2-4d47-bc5e-e2dad7ce5ba8"
        },
        "EntityItemId": {
            "S": "TripRequest:190fb791ce8eedee2c013d10796838b2"
        },
        "TripRequestStatus": {
            "S": "Drafted"
        },
        "TripRequestPurpose": {
            "S": "Last Test Update Trip Request"
        },
        "TripRequestReturnDateTime": {
            "S": "2021-03-07 8:30"
        },
        "TripRequestTripDailyExpense": {
            "L": [
                {
                    "M": {
                        "TripDailyExpenseDate": {
                            "S": "2021-03-04"
                        },
                        "TripDailyExpenseNotes": {
                            "S": "Null"
                        },
                        "TripDailyExpenseDescription": {
                            "S": "Breakfast (2.00.$), Lunch (5.00.$), Diner (5.00.$)"
                        },
                        "TripDailyExpenseType": {
                            "S": "Meal"
                        },
                        "TripDailyExpenseAmount": {
                            "S": "12.00"
                        }
                    }
                },
                {
                    "M": {
                        "TripDailyExpenseDate": {
                            "S": "2021-03-04"
                        },
                        "TripDailyExpenseNotes": {
                            "S": "Null"
                        },
                        "TripDailyExpenseDescription": {
                            "S": "In-area Travel"
                        },
                        "TripDailyExpenseType": {
                            "S": "In-area Travel"
                        },
                        "TripDailyExpenseAmount": {
                            "S": "3.00"
                        }
                    }
                },
                {
                    "M": {
                        "TripDailyExpenseDate": {
                            "S": "2021-03-04"
                        },
                        "TripDailyExpenseNotes": {
                            "S": "Null"
                        },
                        "TripDailyExpenseDescription": {
                            "S": "Alone stay per night"
                        },
                        "TripDailyExpenseType": {
                            "S": "Accommodation"
                        },
                        "TripDailyExpenseAmount": {
                            "S": "15.00"
                        }
                    }
                },
                {
                    "M": {
                        "TripDailyExpenseDate": {
                            "S": "2021-03-04"
                        },
                        "TripDailyExpenseNotes": {
                            "S": "null"
                        },
                        "TripDailyExpenseDescription": {
                            "S": "From Phnum Sruoch to Kracheh"
                        },
                        "TripDailyExpenseType": {
                            "S": "Travel Fee"
                        },
                        "TripDailyExpenseAmount": {
                            "S": "10.00"
                        }
                    }
                },
                {
                    "M": {
                        "TripDailyExpenseDate": {
                            "S": "2021-03-05"
                        },
                        "TripDailyExpenseNotes": {
                            "S": "Null"
                        },
                        "TripDailyExpenseDescription": {
                            "S": "Breakfast (2.00.$), Lunch (5.00.$), Diner (5.00.$)"
                        },
                        "TripDailyExpenseType": {
                            "S": "Meal"
                        },
                        "TripDailyExpenseAmount": {
                            "S": "12.00"
                        }
                    }
                },
                {
                    "M": {
                        "TripDailyExpenseDate": {
                            "S": "2021-03-05"
                        },
                        "TripDailyExpenseNotes": {
                            "S": "Null"
                        },
                        "TripDailyExpenseDescription": {
                            "S": "In-area Travel"
                        },
                        "TripDailyExpenseType": {
                            "S": "In-area Travel"
                        },
                        "TripDailyExpenseAmount": {
                            "S": "3.00"
                        }
                    }
                },
                {
                    "M": {
                        "TripDailyExpenseDate": {
                            "S": "2021-03-05"
                        },
                        "TripDailyExpenseNotes": {
                            "S": "Null"
                        },
                        "TripDailyExpenseDescription": {
                            "S": "Alone stay per night"
                        },
                        "TripDailyExpenseType": {
                            "S": "Accommodation"
                        },
                        "TripDailyExpenseAmount": {
                            "S": "15.00"
                        }
                    }
                },
                {
                    "M": {
                        "TripDailyExpenseDate": {
                            "S": "2021-03-05"
                        },
                        "TripDailyExpenseNotes": {
                            "S": "null"
                        },
                        "TripDailyExpenseDescription": {
                            "S": "From Kracheh to Prek Prasab"
                        },
                        "TripDailyExpenseType": {
                            "S": "Travel Fee"
                        },
                        "TripDailyExpenseAmount": {
                            "S": "3.00"
                        }
                    }
                },
                {
                    "M": {
                        "TripDailyExpenseDate": {
                            "S": "2021-03-06"
                        },
                        "TripDailyExpenseNotes": {
                            "S": "Null"
                        },
                        "TripDailyExpenseDescription": {
                            "S": "Breakfast (2.00.$), Lunch (5.00.$), Diner (5.00.$)"
                        },
                        "TripDailyExpenseType": {
                            "S": "Meal"
                        },
                        "TripDailyExpenseAmount": {
                            "S": "12.00"
                        }
                    }
                },
                {
                    "M": {
                        "TripDailyExpenseDate": {
                            "S": "2021-03-06"
                        },
                        "TripDailyExpenseNotes": {
                            "S": "TEST LINE EXPENSE"
                        },
                        "TripDailyExpenseDescription": {
                            "S": "In-area Travel"
                        },
                        "TripDailyExpenseType": {
                            "S": "In-area Travel"
                        },
                        "TripDailyExpenseAmount": {
                            "S": "3.00"
                        }
                    }
                },
                {
                    "M": {
                        "TripDailyExpenseDate": {
                            "S": "2021-03-06"
                        },
                        "TripDailyExpenseNotes": {
                            "S": "Null"
                        },
                        "TripDailyExpenseDescription": {
                            "S": "Alone stay per night"
                        },
                        "TripDailyExpenseType": {
                            "S": "Accommodation"
                        },
                        "TripDailyExpenseAmount": {
                            "S": "15.00"
                        }
                    }
                },
                {
                    "M": {
                        "TripDailyExpenseDate": {
                            "S": "2021-03-06"
                        },
                        "TripDailyExpenseNotes": {
                            "S": "null"
                        },
                        "TripDailyExpenseDescription": {
                            "S": "From Kracheh to Prek Prasab"
                        },
                        "TripDailyExpenseType": {
                            "S": "Travel Fee"
                        },
                        "TripDailyExpenseAmount": {
                            "S": "3.00"
                        }
                    }
                },
                {
                    "M": {
                        "TripDailyExpenseDate": {
                            "S": "2021-03-07"
                        },
                        "TripDailyExpenseNotes": {
                            "S": "Null"
                        },
                        "TripDailyExpenseDescription": {
                            "S": "Breakfast (2.00.$), Lunch (5.00.$), Diner (5.00.$)"
                        },
                        "TripDailyExpenseType": {
                            "S": "Meal"
                        },
                        "TripDailyExpenseAmount": {
                            "S": "12.00"
                        }
                    }
                },
                {
                    "M": {
                        "TripDailyExpenseDate": {
                            "S": "2021-03-07"
                        },
                        "TripDailyExpenseNotes": {
                            "S": "Null"
                        },
                        "TripDailyExpenseDescription": {
                            "S": "In-area Travel"
                        },
                        "TripDailyExpenseType": {
                            "S": "In-area Travel"
                        },
                        "TripDailyExpenseAmount": {
                            "S": "3.00"
                        }
                    }
                },
                {
                    "M": {
                        "TripDailyExpenseDate": {
                            "S": "2021-03-07"
                        },
                        "TripDailyExpenseNotes": {
                            "S": "Null"
                        },
                        "TripDailyExpenseDescription": {
                            "S": "Alone stay per night"
                        },
                        "TripDailyExpenseType": {
                            "S": "Accommodation"
                        },
                        "TripDailyExpenseAmount": {
                            "S": "0.00"
                        }
                    }
                },
                {
                    "M": {
                        "TripDailyExpenseDate": {
                            "S": "2021-03-07"
                        },
                        "TripDailyExpenseNotes": {
                            "S": "TEST DATA UPDATED"
                        },
                        "TripDailyExpenseDescription": {
                            "S": "From Prek Prasab to Phnum Sruoch"
                        },
                        "TripDailyExpenseType": {
                            "S": "Travel Fee"
                        },
                        "TripDailyExpenseAmount": {
                            "S": "3.00"
                        }
                    }
                }
            ]
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "TripRequestCoveredByOther": {
            "S": "CoveredByOwnCompany"
        },
        "TripRequestDepartureDateTime": {
            "S": "2021-03-04 7:30"
        },
        "TripRequestTravelMode": {
            "S": "PublicTransport"
        },
        "TripRequestTripRoute": {
            "L": [
                {
                    "M": {
                        "ReturnRoute": {
                            "M": {
                                "Date": {
                                    "S": "2021-03-07 8:30"
                                },
                                "Route": {
                                    "M": {
                                        "From": {
                                            "M": {
                                                "LocationLevel1": {
                                                    "M": {
                                                        "LocationLevel1Id": {
                                                            "S": "LocationLevel1:c8d910d391a4314482aa4bfd61ede378"
                                                        },
                                                        "LocationLevel1Name": {
                                                            "S": "Kratie"
                                                        },
                                                        "LocationLevel2": {
                                                            "M": {
                                                                "LocationLevel2Id": {
                                                                    "S": "LocationLevel2:e703ab5ab8328937e8b7a91d3c17d210"
                                                                },
                                                                "LocationLevel2Name": {
                                                                    "S": "Prek Prasab"
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
                                                            "S": "LocationLevel1:f142a3e8ca8f5df1462dd36ad22245e5"
                                                        },
                                                        "LocationLevel1Name": {
                                                            "S": "Kampong Speu"
                                                        },
                                                        "LocationLevel2": {
                                                            "M": {
                                                                "LocationLevel2Id": {
                                                                    "S": "LocationLevel2:43415b8b6ab8b1c9e542f7da5eb136d5"
                                                                },
                                                                "LocationLevel2Name": {
                                                                    "S": "Phnum Sruoch"
                                                                }
                                                            }
                                                        }
                                                    }
                                                }
                                            }
                                        }
                                    }
                                }
                            }
                        },
                        "OtherRoute": {
                            "L": [
                                {
                                    "M": {
                                        "Date": {
                                            "S": "2021-03-05 8:30"
                                        },
                                        "Route": {
                                            "M": {
                                                "Shop": {
                                                    "L": [
                                                        {
                                                            "M": {
                                                                "ShopId": {
                                                                    "S": "59564083-7e2c-4c79-8345-0b7d178f0355"
                                                                },
                                                                "ShopName": {
                                                                    "S": "Samsung LG"
                                                                }
                                                            }
                                                        }
                                                    ]
                                                },
                                                "From": {
                                                    "M": {
                                                        "LocationLevel1": {
                                                            "M": {
                                                                "LocationLevel1Id": {
                                                                    "S": "LocationLevel1:c8d910d391a4314482aa4bfd61ede378"
                                                                },
                                                                "LocationLevel1Name": {
                                                                    "S": "Kratie"
                                                                },
                                                                "LocationLevel2": {
                                                                    "M": {
                                                                        "LocationLevel2Id": {
                                                                            "S": "LocationLevel2:b5fb20fadc9552021625383e30e44d88"
                                                                        },
                                                                        "LocationLevel2Name": {
                                                                            "S": "Kracheh"
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
                                                                    "S": "LocationLevel1:c8d910d391a4314482aa4bfd61ede378"
                                                                },
                                                                "LocationLevel1Name": {
                                                                    "S": "Kratie"
                                                                },
                                                                "LocationLevel2": {
                                                                    "M": {
                                                                        "LocationLevel2Id": {
                                                                            "S": "LocationLevel2:e703ab5ab8328937e8b7a91d3c17d210"
                                                                        },
                                                                        "LocationLevel2Name": {
                                                                            "S": "Prek Prasab"
                                                                        }
                                                                    }
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
                                        "Date": {
                                            "S": "2021-03-06 10:30"
                                        },
                                        "Route": {
                                            "M": {
                                                "Shop": {
                                                    "L": [
                                                        {
                                                            "M": {
                                                                "ShopId": {
                                                                    "S": "1088dd48-a325-4c32-95ea-7802dcca3c5c"
                                                                },
                                                                "ShopName": {
                                                                    "S": "Samsung"
                                                                }
                                                            }
                                                        }
                                                    ]
                                                },
                                                "From": {
                                                    "M": {
                                                        "LocationLevel1": {
                                                            "M": {
                                                                "LocationLevel1Id": {
                                                                    "S": "LocationLevel1:c8d910d391a4314482aa4bfd61ede378"
                                                                },
                                                                "LocationLevel1Name": {
                                                                    "S": "Kratie"
                                                                },
                                                                "LocationLevel2": {
                                                                    "M": {
                                                                        "LocationLevel2Id": {
                                                                            "S": "LocationLevel2:b5fb20fadc9552021625383e30e44d88"
                                                                        },
                                                                        "LocationLevel2Name": {
                                                                            "S": "Kracheh"
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
                                                                    "S": "LocationLevel1:c8d910d391a4314482aa4bfd61ede378"
                                                                },
                                                                "LocationLevel1Name": {
                                                                    "S": "Kratie"
                                                                },
                                                                "LocationLevel2": {
                                                                    "M": {
                                                                        "LocationLevel2Id": {
                                                                            "S": "LocationLevel2:e703ab5ab8328937e8b7a91d3c17d210"
                                                                        },
                                                                        "LocationLevel2Name": {
                                                                            "S": "Prek Prasab"
                                                                        }
                                                                    }
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
                        },
                        "DepartureRoute": {
                            "M": {
                                "Date": {
                                    "S": "2021-03-04 7:30"
                                },
                                "Route": {
                                    "M": {
                                        "Shop": {
                                            "L": [
                                                {
                                                    "M": {
                                                        "ShopId": {
                                                            "S": "59564083-7e2c-4c79-8345-0b7d178f0355"
                                                        },
                                                        "ShopName": {
                                                            "S": "Samsung LG"
                                                        }
                                                    }
                                                },
                                                {
                                                    "M": {
                                                        "ShopId": {
                                                            "S": "d5739d3d-0992-49fe-86c9-25d0015e735c"
                                                        },
                                                        "ShopName": {
                                                            "S": "Samsung Galaxy Store"
                                                        }
                                                    }
                                                }
                                            ]
                                        },
                                        "From": {
                                            "M": {
                                                "LocationLevel1": {
                                                    "M": {
                                                        "LocationLevel1Id": {
                                                            "S": "LocationLevel1:f142a3e8ca8f5df1462dd36ad22245e5"
                                                        },
                                                        "LocationLevel1Name": {
                                                            "S": "Kampong Speu"
                                                        },
                                                        "LocationLevel2": {
                                                            "M": {
                                                                "LocationLevel2Id": {
                                                                    "S": "LocationLevel2:43415b8b6ab8b1c9e542f7da5eb136d5"
                                                                },
                                                                "LocationLevel2Name": {
                                                                    "S": "Phnum Sruoch"
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
                                                            "S": "LocationLevel1:c8d910d391a4314482aa4bfd61ede378"
                                                        },
                                                        "LocationLevel1Name": {
                                                            "S": "Kratie"
                                                        },
                                                        "LocationLevel2": {
                                                            "M": {
                                                                "LocationLevel2Id": {
                                                                    "S": "LocationLevel2:b5fb20fadc9552021625383e30e44d88"
                                                                },
                                                                "LocationLevel2Name": {
                                                                    "S": "Kracheh"
                                                                }
                                                            }
                                                        }
                                                    }
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
]
```

> The above HTTP request, if failure, will return Json structured like this:

```json
{
    "Resource": "aiml:dsa:trip-request/*",
    "Operation": "dsa:item-operation:Retrieves",
    "Message": "You're denied from performing the operation."
}
```

### HTTP Request Filter 
`GET dsa-svc/api/v1/trip-requests?contains=TripRequestRequesterName:Jonh`

### HTTP Response Filter
> The above HTTP request, if successful, will return Json structured like this:

```json
[
    {
        "CompositeAccessPatterns": {
            "S": "TripRequest#TripRequestLocalTrip:LocalTrip#TripRequestRequesterName:Jonh#TripRequestTravelMode:CompanyCar#TripRequestCoveredByOther:CoveredByOwnCompany"
        },
        "TripRequestLocalTrip": {
            "S": "LocalTrip"
        },
        "TripRequestRequesterName": {
            "S": "Jonh"
        },
        "TripRequestRequesterId": {
            "S": "93551f78-c2e2-4d47-bc5e-e2dad7ce5ba8"
        },
        "EntityItemId": {
            "S": "TripRequest:36aea7b372b7f0a7416e7af0f34e5146"
        },
        "TripRequestPurpose": {
            "S": "Test Shop On host server"
        },
        "TripRequestReturnDateTime": {
            "S": "2021-02-27 8:30"
        },
        "TripRequestTripDailyExpense": {
            "L": [
                {
                    "M": {
                        "TripDailyExpenseDate": {
                            "S": "2021-02-22"
                        },
                        "TripDailyExpenseNotes": {
                            "S": "Test Update trip expense"
                        },
                        "TripDailyExpenseDescription": {
                            "S": "Breakfast (2.00.$), Lunch (5.00.$), Diner (5.00.$)"
                        },
                        "TripDailyExpenseType": {
                            "S": "Meal"
                        },
                        "TripDailyExpenseAmount": {
                            "S": "12.00"
                        }
                    }
                },
                {
                    "M": {
                        "TripDailyExpenseDate": {
                            "S": "2021-02-22"
                        },
                        "TripDailyExpenseNotes": {
                            "S": "test"
                        },
                        "TripDailyExpenseDescription": {
                            "S": "In-area Travel"
                        },
                        "TripDailyExpenseType": {
                            "S": "In-area Travel"
                        },
                        "TripDailyExpenseAmount": {
                            "S": "3.00"
                        }
                    }
                },
                {
                    "M": {
                        "TripDailyExpenseDate": {
                            "S": "2021-02-22"
                        },
                        "TripDailyExpenseNotes": {
                            "S": "Share Stay Per Night"
                        },
                        "TripDailyExpenseDescription": {
                            "S": "Alone stay per night"
                        },
                        "TripDailyExpenseType": {
                            "S": "Accommodation"
                        },
                        "TripDailyExpenseAmount": {
                            "S": "20.00"
                        }
                    }
                },
                {
                    "M": {
                        "TripDailyExpenseDate": {
                            "S": "2021-02-23"
                        },
                        "TripDailyExpenseNotes": {
                            "S": "Null"
                        },
                        "TripDailyExpenseDescription": {
                            "S": "Breakfast (2.00.$), Lunch (5.00.$), Diner (5.00.$)"
                        },
                        "TripDailyExpenseType": {
                            "S": "Meal"
                        },
                        "TripDailyExpenseAmount": {
                            "S": "12.00"
                        }
                    }
                },
                {
                    "M": {
                        "TripDailyExpenseDate": {
                            "S": "2021-02-23"
                        },
                        "TripDailyExpenseNotes": {
                            "S": "Null"
                        },
                        "TripDailyExpenseDescription": {
                            "S": "In-area Travel"
                        },
                        "TripDailyExpenseType": {
                            "S": "In-area Travel"
                        },
                        "TripDailyExpenseAmount": {
                            "S": "3.00"
                        }
                    }
                },
                {
                    "M": {
                        "TripDailyExpenseDate": {
                            "S": "2021-02-23"
                        },
                        "TripDailyExpenseNotes": {
                            "S": "Null"
                        },
                        "TripDailyExpenseDescription": {
                            "S": "Alone stay per night"
                        },
                        "TripDailyExpenseType": {
                            "S": "Accommodation"
                        },
                        "TripDailyExpenseAmount": {
                            "S": "0.00"
                        }
                    }
                },
                {
                    "M": {
                        "TripDailyExpenseDate": {
                            "S": "2021-02-22"
                        },
                        "TripDailyExpenseNotes": {
                            "S": "null"
                        },
                        "TripDailyExpenseDescription": {
                            "S": "From Kracheh to Phnum Sruoch"
                        },
                        "TripDailyExpenseType": {
                            "S": "Travel Fee"
                        },
                        "TripDailyExpenseAmount": {
                            "S": "10.00"
                        }
                    }
                },
                {
                    "M": {
                        "TripDailyExpenseDate": {
                            "S": "2021-02-22"
                        },
                        "TripDailyExpenseNotes": {
                            "S": "null"
                        },
                        "TripDailyExpenseDescription": {
                            "S": "From Kracheh to Prek Prasab"
                        },
                        "TripDailyExpenseType": {
                            "S": "Travel Fee"
                        },
                        "TripDailyExpenseAmount": {
                            "S": "3.00"
                        }
                    }
                },
                {
                    "M": {
                        "TripDailyExpenseDate": {
                            "S": "2021-02-23"
                        },
                        "TripDailyExpenseNotes": {
                            "S": "null"
                        },
                        "TripDailyExpenseDescription": {
                            "S": "From Phnum Sruoch to Prek Prasab"
                        },
                        "TripDailyExpenseType": {
                            "S": "Travel Fee"
                        },
                        "TripDailyExpenseAmount": {
                            "S": "8.00"
                        }
                    }
                }
            ]
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "TripRequestCoveredByOther": {
            "S": "CoveredByOwnCompany"
        },
        "TripRequestDepartureDateTime": {
            "S": "2021-02-26 7:30"
        },
        "TripRequestTravelMode": {
            "S": "CompanyCar"
        },
        "TripRequestTripRoute": {
            "L": [
                {
                    "M": {
                        "ReturnRoute": {
                            "M": {
                                "Date": {
                                    "S": "2021-02-27 8:30"
                                },
                                "Route": {
                                    "M": {
                                        "From": {
                                            "M": {
                                                "LocationLevel1": {
                                                    "M": {
                                                        "LocationLevel1Id": {
                                                            "S": "LocationLevel1:c8d910d391a4314482aa4bfd61ede378"
                                                        },
                                                        "LocationLevel1Name": {
                                                            "S": "Kratie"
                                                        },
                                                        "LocationLevel2": {
                                                            "M": {
                                                                "LocationLevel2Id": {
                                                                    "S": "LocationLevel2:e703ab5ab8328937e8b7a91d3c17d210"
                                                                },
                                                                "LocationLevel2Name": {
                                                                    "S": "Prek Prasab"
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
                                                            "S": "LocationLevel1:f142a3e8ca8f5df1462dd36ad22245e5"
                                                        },
                                                        "LocationLevel1Name": {
                                                            "S": "Kampong Speu"
                                                        },
                                                        "LocationLevel2": {
                                                            "M": {
                                                                "LocationLevel2Id": {
                                                                    "S": "LocationLevel2:43415b8b6ab8b1c9e542f7da5eb136d5"
                                                                },
                                                                "LocationLevel2Name": {
                                                                    "S": "Phnum Sruoch"
                                                                }
                                                            }
                                                        }
                                                    }
                                                }
                                            }
                                        }
                                    }
                                }
                            }
                        },
                        "OtherRoute": {
                            "L": [
                                {
                                    "M": {
                                        "Date": {
                                            "S": "2021-02-26 8:30"
                                        },
                                        "Route": {
                                            "M": {
                                                "Shop": {
                                                    "L": [
                                                        {
                                                            "M": {
                                                                "ShopId": {
                                                                    "S": "59564083-7e2c-4c79-8345-0b7d178f0355"
                                                                },
                                                                "ShopName": {
                                                                    "S": "Samsung LG"
                                                                }
                                                            }
                                                        }
                                                    ]
                                                },
                                                "From": {
                                                    "M": {
                                                        "LocationLevel1": {
                                                            "M": {
                                                                "LocationLevel1Id": {
                                                                    "S": "LocationLevel1:c8d910d391a4314482aa4bfd61ede378"
                                                                },
                                                                "LocationLevel1Name": {
                                                                    "S": "Kratie"
                                                                },
                                                                "LocationLevel2": {
                                                                    "M": {
                                                                        "LocationLevel2Id": {
                                                                            "S": "LocationLevel2:b5fb20fadc9552021625383e30e44d88"
                                                                        },
                                                                        "LocationLevel2Name": {
                                                                            "S": "Kracheh"
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
                                                                    "S": "LocationLevel1:c8d910d391a4314482aa4bfd61ede378"
                                                                },
                                                                "LocationLevel1Name": {
                                                                    "S": "Kratie"
                                                                },
                                                                "LocationLevel2": {
                                                                    "M": {
                                                                        "LocationLevel2Id": {
                                                                            "S": "LocationLevel2:e703ab5ab8328937e8b7a91d3c17d210"
                                                                        },
                                                                        "LocationLevel2Name": {
                                                                            "S": "Prek Prasab"
                                                                        }
                                                                    }
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
                                        "Date": {
                                            "S": "2021-02-26 10:30"
                                        },
                                        "Route": {
                                            "M": {
                                                "Shop": {
                                                    "L": [
                                                        {
                                                            "M": {
                                                                "ShopId": {
                                                                    "S": "1088dd48-a325-4c32-95ea-7802dcca3c5c"
                                                                },
                                                                "ShopName": {
                                                                    "S": "Samsung"
                                                                }
                                                            }
                                                        }
                                                    ]
                                                },
                                                "From": {
                                                    "M": {
                                                        "LocationLevel1": {
                                                            "M": {
                                                                "LocationLevel1Id": {
                                                                    "S": "LocationLevel1:c8d910d391a4314482aa4bfd61ede378"
                                                                },
                                                                "LocationLevel1Name": {
                                                                    "S": "Kratie"
                                                                },
                                                                "LocationLevel2": {
                                                                    "M": {
                                                                        "LocationLevel2Id": {
                                                                            "S": "LocationLevel2:b5fb20fadc9552021625383e30e44d88"
                                                                        },
                                                                        "LocationLevel2Name": {
                                                                            "S": "Kracheh"
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
                                                                    "S": "LocationLevel1:c8d910d391a4314482aa4bfd61ede378"
                                                                },
                                                                "LocationLevel1Name": {
                                                                    "S": "Kratie"
                                                                },
                                                                "LocationLevel2": {
                                                                    "M": {
                                                                        "LocationLevel2Id": {
                                                                            "S": "LocationLevel2:e703ab5ab8328937e8b7a91d3c17d210"
                                                                        },
                                                                        "LocationLevel2Name": {
                                                                            "S": "Prek Prasab"
                                                                        }
                                                                    }
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
                        },
                        "DepartureRoute": {
                            "M": {
                                "Date": {
                                    "S": "2021-02-26 7:30"
                                },
                                "Route": {
                                    "M": {
                                        "Shop": {
                                            "L": [
                                                {
                                                    "M": {
                                                        "ShopId": {
                                                            "S": "59564083-7e2c-4c79-8345-0b7d178f0355"
                                                        },
                                                        "ShopName": {
                                                            "S": "Samsung LG"
                                                        }
                                                    }
                                                },
                                                {
                                                    "M": {
                                                        "ShopId": {
                                                            "S": "d5739d3d-0992-49fe-86c9-25d0015e735c"
                                                        },
                                                        "ShopName": {
                                                            "S": "Samsung Galaxy Store"
                                                        }
                                                    }
                                                }
                                            ]
                                        },
                                        "From": {
                                            "M": {
                                                "LocationLevel1": {
                                                    "M": {
                                                        "LocationLevel1Id": {
                                                            "S": "LocationLevel1:f142a3e8ca8f5df1462dd36ad22245e5"
                                                        },
                                                        "LocationLevel1Name": {
                                                            "S": "Kampong Speu"
                                                        },
                                                        "LocationLevel2": {
                                                            "M": {
                                                                "LocationLevel2Id": {
                                                                    "S": "LocationLevel2:43415b8b6ab8b1c9e542f7da5eb136d5"
                                                                },
                                                                "LocationLevel2Name": {
                                                                    "S": "Phnum Sruoch"
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
                                                            "S": "LocationLevel1:c8d910d391a4314482aa4bfd61ede378"
                                                        },
                                                        "LocationLevel1Name": {
                                                            "S": "Kratie"
                                                        },
                                                        "LocationLevel2": {
                                                            "M": {
                                                                "LocationLevel2Id": {
                                                                    "S": "LocationLevel2:b5fb20fadc9552021625383e30e44d88"
                                                                },
                                                                "LocationLevel2Name": {
                                                                    "S": "Kracheh"
                                                                }
                                                            }
                                                        }
                                                    }
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
        "TripRequestDepartureDateTime": "2021-02-26 7:30",
        "TripRequestReturnDateTime": "2021-02-27 8:30",
        "TripRequestRequesterId": "93551f78-c2e2-4d47-bc5e-e2dad7ce5ba8",
        "TripRequestRequesterName": "Jonh",
        "TripRequestPurpose": "Test Shop On host server",
        "TripRequestTravelMode": "PublicTransport",
        "TripRequestCoveredByOther": "CoveredByPartner",
        "Children": {
            "TripRoute": [
                {
                    "DepartureRoute":{
                        "Date": "2021-02-26 7:30",
                        "Route": { 
                            "From": {
                                "LocationLevel1": {
                                    "LocationLevel1Id": "LocationLevel1:f142a3e8ca8f5df1462dd36ad22245e5",
                                    "LocationLevel1Name": "Kampong Speu",
                                    "LocationLevel2": {
                                        "LocationLevel2Id": "LocationLevel2:43415b8b6ab8b1c9e542f7da5eb136d5",
                                        "LocationLevel2Name": "Phnum Sruoch"
                                    }
                                }
                            },
                            "To": {
                                "LocationLevel1": {
                                    "LocationLevel1Id": "LocationLevel1:c8d910d391a4314482aa4bfd61ede378",
                                    "LocationLevel1Name": "Kratie",
                                    "LocationLevel2": {
                                        "LocationLevel2Id": "LocationLevel2:b5fb20fadc9552021625383e30e44d88",
                                        "LocationLevel2Name": "Kracheh"
                                    }
                                }
                            },
                            "Shop": [
                                {
                                    "ShopId": "59564083-7e2c-4c79-8345-0b7d178f0355",
                                    "ShopName": "Samsung LG"
                                },
                                {
                                    "ShopId": "d5739d3d-0992-49fe-86c9-25d0015e735c",
                                    "ShopName": "Samsung Galaxy Store"
                                }
                            ]
                        }
                    },
                    "OtherRoute":[
                        {
                            "Date": "2021-02-26 8:30",
                            "Route":{ 
                                "From": {
                                    "LocationLevel1": {
                                        "LocationLevel1Id": "LocationLevel1:c8d910d391a4314482aa4bfd61ede378",
                                        "LocationLevel1Name": "Kratie",
                                        "LocationLevel2": {
                                            "LocationLevel2Id": "LocationLevel2:b5fb20fadc9552021625383e30e44d88",
                                            "LocationLevel2Name": "Kracheh"
                                        }
                                    }
                                },
                                "To": {
                                    "LocationLevel1": {
                                        "LocationLevel1Id": "LocationLevel1:c8d910d391a4314482aa4bfd61ede378",
                                        "LocationLevel1Name": "Kratie",
                                        "LocationLevel2": {
                                            "LocationLevel2Id": "LocationLevel2:e703ab5ab8328937e8b7a91d3c17d210",
                                            "LocationLevel2Name": "Prek Prasab"
                                        }
                                    }
                                },
                                "Shop": [
                                    {
                                        "ShopId": "59564083-7e2c-4c79-8345-0b7d178f0355",
                                        "ShopName": "Samsung LG"
                                    }
                                ]
                            }
                        },
                        {
                            "Date": "2021-02-26 10:30",
                            "Route":{ 
                                "From": {
                                    "LocationLevel1": {
                                        "LocationLevel1Id": "LocationLevel1:c8d910d391a4314482aa4bfd61ede378",
                                        "LocationLevel1Name": "Kratie",
                                        "LocationLevel2": {
                                            "LocationLevel2Id": "LocationLevel2:b5fb20fadc9552021625383e30e44d88",
                                            "LocationLevel2Name": "Kracheh"
                                        }
                                    }
                                },
                                "To": {
                                    "LocationLevel1": {
                                        "LocationLevel1Id": "LocationLevel1:c8d910d391a4314482aa4bfd61ede378",
                                        "LocationLevel1Name": "Kratie",
                                        "LocationLevel2": {
                                            "LocationLevel2Id": "LocationLevel2:e703ab5ab8328937e8b7a91d3c17d210",
                                            "LocationLevel2Name": "Prek Prasab"
                                        }
                                    }
                                },
                                "Shop": [
                                    {
                                        "ShopId": "1088dd48-a325-4c32-95ea-7802dcca3c5c",
                                        "ShopName": "Samsung"
                                    }
                                ]
                            }
                        }
                    ],
                    "ReturnRoute":{
                        "Date": "2021-02-27 8:30",
                        "Route":{ 
                            "From": {
                                "LocationLevel1": {
                                    "LocationLevel1Id": "LocationLevel1:c8d910d391a4314482aa4bfd61ede378",
                                    "LocationLevel1Name": "Kratie",
                                    "LocationLevel2": {
                                        "LocationLevel2Id": "LocationLevel2:e703ab5ab8328937e8b7a91d3c17d210",
                                        "LocationLevel2Name": "Prek Prasab"
                                    }
                                }
                            },
                            "To": {
                                "LocationLevel1": {
                                    "LocationLevel1Id": "LocationLevel1:f142a3e8ca8f5df1462dd36ad22245e5",
                                    "LocationLevel1Name": "Kampong Speu",
                                    "LocationLevel2": {
                                        "LocationLevel2Id": "LocationLevel2:43415b8b6ab8b1c9e542f7da5eb136d5",
                                        "LocationLevel2Name": "Phnum Sruoch"
                                    }
                                }
                            }
                        }
                    }
                }
            ] 
        }
    },
    "PreviousStatus": "null",
    "Operation": "dsa:item-operation:Create"
}

```

### HTTP Response
> The above HTTP request, if successful, will return Json structured like this:

```json
{
    "CompositeAccessPatterns": {
        "S": "TripRequest#TripRequestLocalTrip:LocalTrip#TripRequestStatus:Drafted#TripRequestRequesterName:Jonh#TripRequestTravelMode:PublicTransport#TripRequestCoveredByOther:CoveredByPartner"
    },
    "TripRequestLocalTrip": {
        "S": "LocalTrip"
    },
    "TripRequestRequesterName": {
        "S": "Jonh"
    },
    "TripRequestRequesterId": {
        "S": "93551f78-c2e2-4d47-bc5e-e2dad7ce5ba8"
    },
    "EntityItemId": {
        "S": "TripRequest:9187db0081aac0add2c43100d28a0d77"
    },
    "TripRequestStatus": {
        "S": "Drafted"
    },
    "TripRequestPurpose": {
        "S": "Test Shop On host server"
    },
    "TripRequestTripDailyExpense": {
        "L": [
            {
                "M": {
                    "TripDailyExpenseDate": {
                        "S": "2021-02-26"
                    },
                    "TripDailyExpenseNotes": {
                        "S": "Null"
                    },
                    "TripDailyExpenseDescription": {
                        "S": "Lump Sum"
                    },
                    "TripDailyExpenseType": {
                        "S": "Lump Sum"
                    },
                    "TripDailyExpenseAmount": {
                        "S": "10.00"
                    }
                }
            },
            {
                "M": {
                    "TripDailyExpenseDate": {
                        "S": "2021-02-26"
                    },
                    "TripDailyExpenseNotes": {
                        "S": "null"
                    },
                    "TripDailyExpenseDescription": {
                        "S": "From Phnum Sruoch to Kracheh"
                    },
                    "TripDailyExpenseType": {
                        "S": "Travel Fee"
                    },
                    "TripDailyExpenseAmount": {
                        "S": "10.00"
                    }
                }
            },
            {
                "M": {
                    "TripDailyExpenseDate": {
                        "S": "2021-02-26"
                    },
                    "TripDailyExpenseNotes": {
                        "S": "null"
                    },
                    "TripDailyExpenseDescription": {
                        "S": "From Kracheh to Prek Prasab"
                    },
                    "TripDailyExpenseType": {
                        "S": "Travel Fee"
                    },
                    "TripDailyExpenseAmount": {
                        "S": "3.00"
                    }
                }
            },
            {
                "M": {
                    "TripDailyExpenseDate": {
                        "S": "2021-02-26"
                    },
                    "TripDailyExpenseNotes": {
                        "S": "null"
                    },
                    "TripDailyExpenseDescription": {
                        "S": "From Kracheh to Prek Prasab"
                    },
                    "TripDailyExpenseType": {
                        "S": "Travel Fee"
                    },
                    "TripDailyExpenseAmount": {
                        "S": "3.00"
                    }
                }
            },
            {
                "M": {
                    "TripDailyExpenseDate": {
                        "S": "2021-02-27"
                    },
                    "TripDailyExpenseNotes": {
                        "S": "Null"
                    },
                    "TripDailyExpenseDescription": {
                        "S": "Lump Sum"
                    },
                    "TripDailyExpenseType": {
                        "S": "Lump Sum"
                    },
                    "TripDailyExpenseAmount": {
                        "S": "10.00"
                    }
                }
            },
            {
                "M": {
                    "TripDailyExpenseDate": {
                        "S": "2021-02-27"
                    },
                    "TripDailyExpenseNotes": {
                        "S": "null"
                    },
                    "TripDailyExpenseDescription": {
                        "S": "From Prek Prasab to Phnum Sruoch"
                    },
                    "TripDailyExpenseType": {
                        "S": "Travel Fee"
                    },
                    "TripDailyExpenseAmount": {
                        "S": "3.00"
                    }
                }
            }
        ]
    },
    "TripRequestReturnDateTime": {
        "S": "2021-02-27 8:30"
    },
    "TripRequestCoveredByOther": {
        "S": "CoveredByPartner"
    },
    "TenantId": {
        "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
    },
    "TripRequestDepartureDateTime": {
        "S": "2021-02-26 7:30"
    },
    "TripRequestTravelMode": {
        "S": "PublicTransport"
    },
    "TripRequestTripRoute": {
        "L": [
            {
                "M": {
                    "ReturnRoute": {
                        "M": {
                            "Date": {
                                "S": "2021-02-27 8:30"
                            },
                            "Route": {
                                "M": {
                                    "From": {
                                        "M": {
                                            "LocationLevel1": {
                                                "M": {
                                                    "LocationLevel1Id": {
                                                        "S": "LocationLevel1:c8d910d391a4314482aa4bfd61ede378"
                                                    },
                                                    "LocationLevel1Name": {
                                                        "S": "Kratie"
                                                    },
                                                    "LocationLevel2": {
                                                        "M": {
                                                            "LocationLevel2Id": {
                                                                "S": "LocationLevel2:e703ab5ab8328937e8b7a91d3c17d210"
                                                            },
                                                            "LocationLevel2Name": {
                                                                "S": "Prek Prasab"
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
                                                        "S": "LocationLevel1:f142a3e8ca8f5df1462dd36ad22245e5"
                                                    },
                                                    "LocationLevel1Name": {
                                                        "S": "Kampong Speu"
                                                    },
                                                    "LocationLevel2": {
                                                        "M": {
                                                            "LocationLevel2Id": {
                                                                "S": "LocationLevel2:43415b8b6ab8b1c9e542f7da5eb136d5"
                                                            },
                                                            "LocationLevel2Name": {
                                                                "S": "Phnum Sruoch"
                                                            }
                                                        }
                                                    }
                                                }
                                            }
                                        }
                                    }
                                }
                            }
                        }
                    },
                    "OtherRoute": {
                        "L": [
                            {
                                "M": {
                                    "Date": {
                                        "S": "2021-02-26 8:30"
                                    },
                                    "Route": {
                                        "M": {
                                            "Shop": {
                                                "L": [
                                                    {
                                                        "M": {
                                                            "ShopId": {
                                                                "S": "59564083-7e2c-4c79-8345-0b7d178f0355"
                                                            },
                                                            "ShopName": {
                                                                "S": "Samsung LG"
                                                            }
                                                        }
                                                    }
                                                ]
                                            },
                                            "From": {
                                                "M": {
                                                    "LocationLevel1": {
                                                        "M": {
                                                            "LocationLevel1Id": {
                                                                "S": "LocationLevel1:c8d910d391a4314482aa4bfd61ede378"
                                                            },
                                                            "LocationLevel1Name": {
                                                                "S": "Kratie"
                                                            },
                                                            "LocationLevel2": {
                                                                "M": {
                                                                    "LocationLevel2Id": {
                                                                        "S": "LocationLevel2:b5fb20fadc9552021625383e30e44d88"
                                                                    },
                                                                    "LocationLevel2Name": {
                                                                        "S": "Kracheh"
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
                                                                "S": "LocationLevel1:c8d910d391a4314482aa4bfd61ede378"
                                                            },
                                                            "LocationLevel1Name": {
                                                                "S": "Kratie"
                                                            },
                                                            "LocationLevel2": {
                                                                "M": {
                                                                    "LocationLevel2Id": {
                                                                        "S": "LocationLevel2:e703ab5ab8328937e8b7a91d3c17d210"
                                                                    },
                                                                    "LocationLevel2Name": {
                                                                        "S": "Prek Prasab"
                                                                    }
                                                                }
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
                                    "Date": {
                                        "S": "2021-02-26 10:30"
                                    },
                                    "Route": {
                                        "M": {
                                            "Shop": {
                                                "L": [
                                                    {
                                                        "M": {
                                                            "ShopId": {
                                                                "S": "1088dd48-a325-4c32-95ea-7802dcca3c5c"
                                                            },
                                                            "ShopName": {
                                                                "S": "Samsung"
                                                            }
                                                        }
                                                    }
                                                ]
                                            },
                                            "From": {
                                                "M": {
                                                    "LocationLevel1": {
                                                        "M": {
                                                            "LocationLevel1Id": {
                                                                "S": "LocationLevel1:c8d910d391a4314482aa4bfd61ede378"
                                                            },
                                                            "LocationLevel1Name": {
                                                                "S": "Kratie"
                                                            },
                                                            "LocationLevel2": {
                                                                "M": {
                                                                    "LocationLevel2Id": {
                                                                        "S": "LocationLevel2:b5fb20fadc9552021625383e30e44d88"
                                                                    },
                                                                    "LocationLevel2Name": {
                                                                        "S": "Kracheh"
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
                                                                "S": "LocationLevel1:c8d910d391a4314482aa4bfd61ede378"
                                                            },
                                                            "LocationLevel1Name": {
                                                                "S": "Kratie"
                                                            },
                                                            "LocationLevel2": {
                                                                "M": {
                                                                    "LocationLevel2Id": {
                                                                        "S": "LocationLevel2:e703ab5ab8328937e8b7a91d3c17d210"
                                                                    },
                                                                    "LocationLevel2Name": {
                                                                        "S": "Prek Prasab"
                                                                    }
                                                                }
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
                    },
                    "DepartureRoute": {
                        "M": {
                            "Date": {
                                "S": "2021-02-26 7:30"
                            },
                            "Route": {
                                "M": {
                                    "Shop": {
                                        "L": [
                                            {
                                                "M": {
                                                    "ShopId": {
                                                        "S": "59564083-7e2c-4c79-8345-0b7d178f0355"
                                                    },
                                                    "ShopName": {
                                                        "S": "Samsung LG"
                                                    }
                                                }
                                            },
                                            {
                                                "M": {
                                                    "ShopId": {
                                                        "S": "d5739d3d-0992-49fe-86c9-25d0015e735c"
                                                    },
                                                    "ShopName": {
                                                        "S": "Samsung Galaxy Store"
                                                    }
                                                }
                                            }
                                        ]
                                    },
                                    "From": {
                                        "M": {
                                            "LocationLevel1": {
                                                "M": {
                                                    "LocationLevel1Id": {
                                                        "S": "LocationLevel1:f142a3e8ca8f5df1462dd36ad22245e5"
                                                    },
                                                    "LocationLevel1Name": {
                                                        "S": "Kampong Speu"
                                                    },
                                                    "LocationLevel2": {
                                                        "M": {
                                                            "LocationLevel2Id": {
                                                                "S": "LocationLevel2:43415b8b6ab8b1c9e542f7da5eb136d5"
                                                            },
                                                            "LocationLevel2Name": {
                                                                "S": "Phnum Sruoch"
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
                                                        "S": "LocationLevel1:c8d910d391a4314482aa4bfd61ede378"
                                                    },
                                                    "LocationLevel1Name": {
                                                        "S": "Kratie"
                                                    },
                                                    "LocationLevel2": {
                                                        "M": {
                                                            "LocationLevel2Id": {
                                                                "S": "LocationLevel2:b5fb20fadc9552021625383e30e44d88"
                                                            },
                                                            "LocationLevel2Name": {
                                                                "S": "Kracheh"
                                                            }
                                                        }
                                                    }
                                                }
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
```

## Update Trip Request

### HTTP Request
`PUT dsa-svc/api/v1/trip-requests/{trip-request-id}`

### Query Paramaeters
Parameter       | Description
---------       | -----------
trip-request-id | Is the EntityItemId Of trip request

### Body Request

```json
{
    "TripRequest": {
        "TripRequestLocalTrip": "LocalTrip",
        "TripRequestDepartureDateTime": "2021-02-26 7:30",
        "TripRequestReturnDateTime": "2021-02-27 8:30",
        "TripRequestRequesterId": "93551f78-c2e2-4d47-bc5e-e2dad7ce5ba8",
        "TripRequestRequesterName": "Jonh",
        "TripRequestPurpose": "Test Shop On host server",
        "TripRequestTravelMode": "PublicTransport",
        "TripRequestCoveredByOther": "CoveredByPartner",
        "Children": {
            "TripRoute": [
                {
                    "DepartureRoute":{
                        "Date": "2021-02-26 7:30",
                        "Route": { 
                            "From": {
                                "LocationLevel1": {
                                    "LocationLevel1Id": "LocationLevel1:f142a3e8ca8f5df1462dd36ad22245e5",
                                    "LocationLevel1Name": "Kampong Speu",
                                    "LocationLevel2": {
                                        "LocationLevel2Id": "LocationLevel2:43415b8b6ab8b1c9e542f7da5eb136d5",
                                        "LocationLevel2Name": "Phnum Sruoch"
                                    }
                                }
                            },
                            "To": {
                                "LocationLevel1": {
                                    "LocationLevel1Id": "LocationLevel1:c8d910d391a4314482aa4bfd61ede378",
                                    "LocationLevel1Name": "Kratie",
                                    "LocationLevel2": {
                                        "LocationLevel2Id": "LocationLevel2:b5fb20fadc9552021625383e30e44d88",
                                        "LocationLevel2Name": "Kracheh"
                                    }
                                }
                            },
                            "Shop": [
                                {
                                    "ShopId": "59564083-7e2c-4c79-8345-0b7d178f0355",
                                    "ShopName": "Samsung LG"
                                },
                                {
                                    "ShopId": "d5739d3d-0992-49fe-86c9-25d0015e735c",
                                    "ShopName": "Samsung Galaxy Store"
                                }
                            ]
                        }
                    },
                    "OtherRoute":[
                        {
                            "Date": "2021-02-26 8:30",
                            "Route":{ 
                                "From": {
                                    "LocationLevel1": {
                                        "LocationLevel1Id": "LocationLevel1:c8d910d391a4314482aa4bfd61ede378",
                                        "LocationLevel1Name": "Kratie",
                                        "LocationLevel2": {
                                            "LocationLevel2Id": "LocationLevel2:b5fb20fadc9552021625383e30e44d88",
                                            "LocationLevel2Name": "Kracheh"
                                        }
                                    }
                                },
                                "To": {
                                    "LocationLevel1": {
                                        "LocationLevel1Id": "LocationLevel1:c8d910d391a4314482aa4bfd61ede378",
                                        "LocationLevel1Name": "Kratie",
                                        "LocationLevel2": {
                                            "LocationLevel2Id": "LocationLevel2:e703ab5ab8328937e8b7a91d3c17d210",
                                            "LocationLevel2Name": "Prek Prasab"
                                        }
                                    }
                                },
                                "Shop": [
                                    {
                                        "ShopId": "59564083-7e2c-4c79-8345-0b7d178f0355",
                                        "ShopName": "Samsung LG"
                                    }
                                ]
                            }
                        },
                        {
                            "Date": "2021-02-26 10:30",
                            "Route":{ 
                                "From": {
                                    "LocationLevel1": {
                                        "LocationLevel1Id": "LocationLevel1:c8d910d391a4314482aa4bfd61ede378",
                                        "LocationLevel1Name": "Kratie",
                                        "LocationLevel2": {
                                            "LocationLevel2Id": "LocationLevel2:b5fb20fadc9552021625383e30e44d88",
                                            "LocationLevel2Name": "Kracheh"
                                        }
                                    }
                                },
                                "To": {
                                    "LocationLevel1": {
                                        "LocationLevel1Id": "LocationLevel1:c8d910d391a4314482aa4bfd61ede378",
                                        "LocationLevel1Name": "Kratie",
                                        "LocationLevel2": {
                                            "LocationLevel2Id": "LocationLevel2:e703ab5ab8328937e8b7a91d3c17d210",
                                            "LocationLevel2Name": "Prek Prasab"
                                        }
                                    }
                                },
                                "Shop": [
                                    {
                                        "ShopId": "1088dd48-a325-4c32-95ea-7802dcca3c5c",
                                        "ShopName": "Samsung"
                                    }
                                ]
                            }
                        }
                    ],
                    "ReturnRoute":{
                        "Date": "2021-02-27 8:30",
                        "Route":{ 
                            "From": {
                                "LocationLevel1": {
                                    "LocationLevel1Id": "LocationLevel1:c8d910d391a4314482aa4bfd61ede378",
                                    "LocationLevel1Name": "Kratie",
                                    "LocationLevel2": {
                                        "LocationLevel2Id": "LocationLevel2:e703ab5ab8328937e8b7a91d3c17d210",
                                        "LocationLevel2Name": "Prek Prasab"
                                    }
                                }
                            },
                            "To": {
                                "LocationLevel1": {
                                    "LocationLevel1Id": "LocationLevel1:f142a3e8ca8f5df1462dd36ad22245e5",
                                    "LocationLevel1Name": "Kampong Speu",
                                    "LocationLevel2": {
                                        "LocationLevel2Id": "LocationLevel2:43415b8b6ab8b1c9e542f7da5eb136d5",
                                        "LocationLevel2Name": "Phnum Sruoch"
                                    }
                                }
                            }
                        }
                    }
                }
            ] 
        }
    },
}
```

### HTTP Response
> The above HTTP request, if successful, will return Json structured like this:

```json
{
    "CompositeAccessPatterns": {
        "S": "TripRequest#TripRequestLocalTrip:LocalTrip#TripRequestStatus:Drafted#TripRequestRequesterName:Jonh#TripRequestTravelMode:PublicTransport#TripRequestCoveredByOther:CoveredByPartner"
    },
    "TripRequestLocalTrip": {
        "S": "LocalTrip"
    },
    "TripRequestRequesterName": {
        "S": "Jonh"
    },
    "TripRequestRequesterId": {
        "S": "93551f78-c2e2-4d47-bc5e-e2dad7ce5ba8"
    },
    "EntityItemId": {
        "S": "TripRequest:9187db0081aac0add2c43100d28a0d77"
    },
    "TripRequestStatus": {
        "S": "Drafted"
    },
    "TripRequestPurpose": {
        "S": "Test Shop On host server"
    },
    "TripRequestTripDailyExpense": {
        "L": [
            {
                "M": {
                    "TripDailyExpenseDate": {
                        "S": "2021-02-26"
                    },
                    "TripDailyExpenseNotes": {
                        "S": "Null"
                    },
                    "TripDailyExpenseDescription": {
                        "S": "Lump Sum"
                    },
                    "TripDailyExpenseType": {
                        "S": "Lump Sum"
                    },
                    "TripDailyExpenseAmount": {
                        "S": "10.00"
                    }
                }
            },
            {
                "M": {
                    "TripDailyExpenseDate": {
                        "S": "2021-02-26"
                    },
                    "TripDailyExpenseNotes": {
                        "S": "null"
                    },
                    "TripDailyExpenseDescription": {
                        "S": "From Phnum Sruoch to Kracheh"
                    },
                    "TripDailyExpenseType": {
                        "S": "Travel Fee"
                    },
                    "TripDailyExpenseAmount": {
                        "S": "10.00"
                    }
                }
            },
            {
                "M": {
                    "TripDailyExpenseDate": {
                        "S": "2021-02-26"
                    },
                    "TripDailyExpenseNotes": {
                        "S": "null"
                    },
                    "TripDailyExpenseDescription": {
                        "S": "From Kracheh to Prek Prasab"
                    },
                    "TripDailyExpenseType": {
                        "S": "Travel Fee"
                    },
                    "TripDailyExpenseAmount": {
                        "S": "3.00"
                    }
                }
            },
            {
                "M": {
                    "TripDailyExpenseDate": {
                        "S": "2021-02-26"
                    },
                    "TripDailyExpenseNotes": {
                        "S": "null"
                    },
                    "TripDailyExpenseDescription": {
                        "S": "From Kracheh to Prek Prasab"
                    },
                    "TripDailyExpenseType": {
                        "S": "Travel Fee"
                    },
                    "TripDailyExpenseAmount": {
                        "S": "3.00"
                    }
                }
            },
            {
                "M": {
                    "TripDailyExpenseDate": {
                        "S": "2021-02-27"
                    },
                    "TripDailyExpenseNotes": {
                        "S": "Null"
                    },
                    "TripDailyExpenseDescription": {
                        "S": "Lump Sum"
                    },
                    "TripDailyExpenseType": {
                        "S": "Lump Sum"
                    },
                    "TripDailyExpenseAmount": {
                        "S": "10.00"
                    }
                }
            },
            {
                "M": {
                    "TripDailyExpenseDate": {
                        "S": "2021-02-27"
                    },
                    "TripDailyExpenseNotes": {
                        "S": "null"
                    },
                    "TripDailyExpenseDescription": {
                        "S": "From Prek Prasab to Phnum Sruoch"
                    },
                    "TripDailyExpenseType": {
                        "S": "Travel Fee"
                    },
                    "TripDailyExpenseAmount": {
                        "S": "3.00"
                    }
                }
            }
        ]
    },
    "TripRequestReturnDateTime": {
        "S": "2021-02-27 8:30"
    },
    "TripRequestCoveredByOther": {
        "S": "CoveredByPartner"
    },
    "TenantId": {
        "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
    },
    "TripRequestDepartureDateTime": {
        "S": "2021-02-26 7:30"
    },
    "TripRequestTravelMode": {
        "S": "PublicTransport"
    },
    "TripRequestTripRoute": {
        "L": [
            {
                "M": {
                    "ReturnRoute": {
                        "M": {
                            "Date": {
                                "S": "2021-02-27 8:30"
                            },
                            "Route": {
                                "M": {
                                    "From": {
                                        "M": {
                                            "LocationLevel1": {
                                                "M": {
                                                    "LocationLevel1Id": {
                                                        "S": "LocationLevel1:c8d910d391a4314482aa4bfd61ede378"
                                                    },
                                                    "LocationLevel1Name": {
                                                        "S": "Kratie"
                                                    },
                                                    "LocationLevel2": {
                                                        "M": {
                                                            "LocationLevel2Id": {
                                                                "S": "LocationLevel2:e703ab5ab8328937e8b7a91d3c17d210"
                                                            },
                                                            "LocationLevel2Name": {
                                                                "S": "Prek Prasab"
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
                                                        "S": "LocationLevel1:f142a3e8ca8f5df1462dd36ad22245e5"
                                                    },
                                                    "LocationLevel1Name": {
                                                        "S": "Kampong Speu"
                                                    },
                                                    "LocationLevel2": {
                                                        "M": {
                                                            "LocationLevel2Id": {
                                                                "S": "LocationLevel2:43415b8b6ab8b1c9e542f7da5eb136d5"
                                                            },
                                                            "LocationLevel2Name": {
                                                                "S": "Phnum Sruoch"
                                                            }
                                                        }
                                                    }
                                                }
                                            }
                                        }
                                    }
                                }
                            }
                        }
                    },
                    "OtherRoute": {
                        "L": [
                            {
                                "M": {
                                    "Date": {
                                        "S": "2021-02-26 8:30"
                                    },
                                    "Route": {
                                        "M": {
                                            "Shop": {
                                                "L": [
                                                    {
                                                        "M": {
                                                            "ShopId": {
                                                                "S": "59564083-7e2c-4c79-8345-0b7d178f0355"
                                                            },
                                                            "ShopName": {
                                                                "S": "Samsung LG"
                                                            }
                                                        }
                                                    }
                                                ]
                                            },
                                            "From": {
                                                "M": {
                                                    "LocationLevel1": {
                                                        "M": {
                                                            "LocationLevel1Id": {
                                                                "S": "LocationLevel1:c8d910d391a4314482aa4bfd61ede378"
                                                            },
                                                            "LocationLevel1Name": {
                                                                "S": "Kratie"
                                                            },
                                                            "LocationLevel2": {
                                                                "M": {
                                                                    "LocationLevel2Id": {
                                                                        "S": "LocationLevel2:b5fb20fadc9552021625383e30e44d88"
                                                                    },
                                                                    "LocationLevel2Name": {
                                                                        "S": "Kracheh"
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
                                                                "S": "LocationLevel1:c8d910d391a4314482aa4bfd61ede378"
                                                            },
                                                            "LocationLevel1Name": {
                                                                "S": "Kratie"
                                                            },
                                                            "LocationLevel2": {
                                                                "M": {
                                                                    "LocationLevel2Id": {
                                                                        "S": "LocationLevel2:e703ab5ab8328937e8b7a91d3c17d210"
                                                                    },
                                                                    "LocationLevel2Name": {
                                                                        "S": "Prek Prasab"
                                                                    }
                                                                }
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
                                    "Date": {
                                        "S": "2021-02-26 10:30"
                                    },
                                    "Route": {
                                        "M": {
                                            "Shop": {
                                                "L": [
                                                    {
                                                        "M": {
                                                            "ShopId": {
                                                                "S": "1088dd48-a325-4c32-95ea-7802dcca3c5c"
                                                            },
                                                            "ShopName": {
                                                                "S": "Samsung"
                                                            }
                                                        }
                                                    }
                                                ]
                                            },
                                            "From": {
                                                "M": {
                                                    "LocationLevel1": {
                                                        "M": {
                                                            "LocationLevel1Id": {
                                                                "S": "LocationLevel1:c8d910d391a4314482aa4bfd61ede378"
                                                            },
                                                            "LocationLevel1Name": {
                                                                "S": "Kratie"
                                                            },
                                                            "LocationLevel2": {
                                                                "M": {
                                                                    "LocationLevel2Id": {
                                                                        "S": "LocationLevel2:b5fb20fadc9552021625383e30e44d88"
                                                                    },
                                                                    "LocationLevel2Name": {
                                                                        "S": "Kracheh"
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
                                                                "S": "LocationLevel1:c8d910d391a4314482aa4bfd61ede378"
                                                            },
                                                            "LocationLevel1Name": {
                                                                "S": "Kratie"
                                                            },
                                                            "LocationLevel2": {
                                                                "M": {
                                                                    "LocationLevel2Id": {
                                                                        "S": "LocationLevel2:e703ab5ab8328937e8b7a91d3c17d210"
                                                                    },
                                                                    "LocationLevel2Name": {
                                                                        "S": "Prek Prasab"
                                                                    }
                                                                }
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
                    },
                    "DepartureRoute": {
                        "M": {
                            "Date": {
                                "S": "2021-02-26 7:30"
                            },
                            "Route": {
                                "M": {
                                    "Shop": {
                                        "L": [
                                            {
                                                "M": {
                                                    "ShopId": {
                                                        "S": "59564083-7e2c-4c79-8345-0b7d178f0355"
                                                    },
                                                    "ShopName": {
                                                        "S": "Samsung LG"
                                                    }
                                                }
                                            },
                                            {
                                                "M": {
                                                    "ShopId": {
                                                        "S": "d5739d3d-0992-49fe-86c9-25d0015e735c"
                                                    },
                                                    "ShopName": {
                                                        "S": "Samsung Galaxy Store"
                                                    }
                                                }
                                            }
                                        ]
                                    },
                                    "From": {
                                        "M": {
                                            "LocationLevel1": {
                                                "M": {
                                                    "LocationLevel1Id": {
                                                        "S": "LocationLevel1:f142a3e8ca8f5df1462dd36ad22245e5"
                                                    },
                                                    "LocationLevel1Name": {
                                                        "S": "Kampong Speu"
                                                    },
                                                    "LocationLevel2": {
                                                        "M": {
                                                            "LocationLevel2Id": {
                                                                "S": "LocationLevel2:43415b8b6ab8b1c9e542f7da5eb136d5"
                                                            },
                                                            "LocationLevel2Name": {
                                                                "S": "Phnum Sruoch"
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
                                                        "S": "LocationLevel1:c8d910d391a4314482aa4bfd61ede378"
                                                    },
                                                    "LocationLevel1Name": {
                                                        "S": "Kratie"
                                                    },
                                                    "LocationLevel2": {
                                                        "M": {
                                                            "LocationLevel2Id": {
                                                                "S": "LocationLevel2:b5fb20fadc9552021625383e30e44d88"
                                                            },
                                                            "LocationLevel2Name": {
                                                                "S": "Kracheh"
                                                            }
                                                        }
                                                    }
                                                }
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
```

## Get Info Detail Of Trip Request
### HTTP Request
`GET dsa-svc/api/v1/trip-requests/{trip-request-id}`

### Query Paramaeters
Parameter       | Description
---------       | -----------
trip-request-id | Is the EntityItemId Of trip request

### Body Request

```json
{
    "Resource": "aiml:dsa:trip-request/TripRequest:190fb791ce8eedee2c013d10796838b2",
    "Operation": "dsa:item-operation:Retrieve"
}
```

### HTTP Response
> The above HTTP request, if successful, will return Json structured like this:

```json
{
    "CompositeAccessPatterns": {
        "S": "TripRequest#TripRequestLocalTrip:LocalTrip#TripRequestStatus:Drafted#TripRequestRequesterName:Sreyta#TripRequestTravelMode:PublicTransport#TripRequestCoveredByOther:CoveredByOwnCompany"
    },
    "TripRequestLocalTrip": {
        "S": "LocalTrip"
    },
    "TripRequestRequesterName": {
        "S": "Sreyta"
    },
    "TripRequestRequesterId": {
        "S": "93551f78-c2e2-4d47-bc5e-e2dad7ce5ba8"
    },
    "EntityItemId": {
        "S": "TripRequest:190fb791ce8eedee2c013d10796838b2"
    },
    "TripRequestStatus": {
        "S": "Drafted"
    },
    "TripRequestPurpose": {
        "S": "Last Test Update Trip Request"
    },
    "TripRequestReturnDateTime": {
        "S": "2021-03-07 8:30"
    },
    "TripRequestTripDailyExpense": {
        "L": [
            {
                "M": {
                    "TripDailyExpenseDate": {
                        "S": "2021-03-04"
                    },
                    "TripDailyExpenseNotes": {
                        "S": "Null"
                    },
                    "TripDailyExpenseDescription": {
                        "S": "Breakfast (2.00.$), Lunch (5.00.$), Diner (5.00.$)"
                    },
                    "TripDailyExpenseType": {
                        "S": "Meal"
                    },
                    "TripDailyExpenseAmount": {
                        "S": "12.00"
                    }
                }
            },
            {
                "M": {
                    "TripDailyExpenseDate": {
                        "S": "2021-03-04"
                    },
                    "TripDailyExpenseNotes": {
                        "S": "Null"
                    },
                    "TripDailyExpenseDescription": {
                        "S": "In-area Travel"
                    },
                    "TripDailyExpenseType": {
                        "S": "In-area Travel"
                    },
                    "TripDailyExpenseAmount": {
                        "S": "3.00"
                    }
                }
            },
            {
                "M": {
                    "TripDailyExpenseDate": {
                        "S": "2021-03-04"
                    },
                    "TripDailyExpenseNotes": {
                        "S": "Null"
                    },
                    "TripDailyExpenseDescription": {
                        "S": "Alone stay per night"
                    },
                    "TripDailyExpenseType": {
                        "S": "Accommodation"
                    },
                    "TripDailyExpenseAmount": {
                        "S": "15.00"
                    }
                }
            },
            {
                "M": {
                    "TripDailyExpenseDate": {
                        "S": "2021-03-04"
                    },
                    "TripDailyExpenseNotes": {
                        "S": "null"
                    },
                    "TripDailyExpenseDescription": {
                        "S": "From Phnum Sruoch to Kracheh"
                    },
                    "TripDailyExpenseType": {
                        "S": "Travel Fee"
                    },
                    "TripDailyExpenseAmount": {
                        "S": "10.00"
                    }
                }
            },
            {
                "M": {
                    "TripDailyExpenseDate": {
                        "S": "2021-03-05"
                    },
                    "TripDailyExpenseNotes": {
                        "S": "Null"
                    },
                    "TripDailyExpenseDescription": {
                        "S": "Breakfast (2.00.$), Lunch (5.00.$), Diner (5.00.$)"
                    },
                    "TripDailyExpenseType": {
                        "S": "Meal"
                    },
                    "TripDailyExpenseAmount": {
                        "S": "12.00"
                    }
                }
            },
            {
                "M": {
                    "TripDailyExpenseDate": {
                        "S": "2021-03-05"
                    },
                    "TripDailyExpenseNotes": {
                        "S": "Null"
                    },
                    "TripDailyExpenseDescription": {
                        "S": "In-area Travel"
                    },
                    "TripDailyExpenseType": {
                        "S": "In-area Travel"
                    },
                    "TripDailyExpenseAmount": {
                        "S": "3.00"
                    }
                }
            },
            {
                "M": {
                    "TripDailyExpenseDate": {
                        "S": "2021-03-05"
                    },
                    "TripDailyExpenseNotes": {
                        "S": "Null"
                    },
                    "TripDailyExpenseDescription": {
                        "S": "Alone stay per night"
                    },
                    "TripDailyExpenseType": {
                        "S": "Accommodation"
                    },
                    "TripDailyExpenseAmount": {
                        "S": "15.00"
                    }
                }
            },
            {
                "M": {
                    "TripDailyExpenseDate": {
                        "S": "2021-03-05"
                    },
                    "TripDailyExpenseNotes": {
                        "S": "null"
                    },
                    "TripDailyExpenseDescription": {
                        "S": "From Kracheh to Prek Prasab"
                    },
                    "TripDailyExpenseType": {
                        "S": "Travel Fee"
                    },
                    "TripDailyExpenseAmount": {
                        "S": "3.00"
                    }
                }
            },
            {
                "M": {
                    "TripDailyExpenseDate": {
                        "S": "2021-03-06"
                    },
                    "TripDailyExpenseNotes": {
                        "S": "Null"
                    },
                    "TripDailyExpenseDescription": {
                        "S": "Breakfast (2.00.$), Lunch (5.00.$), Diner (5.00.$)"
                    },
                    "TripDailyExpenseType": {
                        "S": "Meal"
                    },
                    "TripDailyExpenseAmount": {
                        "S": "12.00"
                    }
                }
            },
            {
                "M": {
                    "TripDailyExpenseDate": {
                        "S": "2021-03-06"
                    },
                    "TripDailyExpenseNotes": {
                        "S": "TEST LINE EXPENSE"
                    },
                    "TripDailyExpenseDescription": {
                        "S": "In-area Travel"
                    },
                    "TripDailyExpenseType": {
                        "S": "In-area Travel"
                    },
                    "TripDailyExpenseAmount": {
                        "S": "3.00"
                    }
                }
            },
            {
                "M": {
                    "TripDailyExpenseDate": {
                        "S": "2021-03-06"
                    },
                    "TripDailyExpenseNotes": {
                        "S": "Null"
                    },
                    "TripDailyExpenseDescription": {
                        "S": "Alone stay per night"
                    },
                    "TripDailyExpenseType": {
                        "S": "Accommodation"
                    },
                    "TripDailyExpenseAmount": {
                        "S": "15.00"
                    }
                }
            },
            {
                "M": {
                    "TripDailyExpenseDate": {
                        "S": "2021-03-06"
                    },
                    "TripDailyExpenseNotes": {
                        "S": "null"
                    },
                    "TripDailyExpenseDescription": {
                        "S": "From Kracheh to Prek Prasab"
                    },
                    "TripDailyExpenseType": {
                        "S": "Travel Fee"
                    },
                    "TripDailyExpenseAmount": {
                        "S": "3.00"
                    }
                }
            },
            {
                "M": {
                    "TripDailyExpenseDate": {
                        "S": "2021-03-07"
                    },
                    "TripDailyExpenseNotes": {
                        "S": "Null"
                    },
                    "TripDailyExpenseDescription": {
                        "S": "Breakfast (2.00.$), Lunch (5.00.$), Diner (5.00.$)"
                    },
                    "TripDailyExpenseType": {
                        "S": "Meal"
                    },
                    "TripDailyExpenseAmount": {
                        "S": "12.00"
                    }
                }
            },
            {
                "M": {
                    "TripDailyExpenseDate": {
                        "S": "2021-03-07"
                    },
                    "TripDailyExpenseNotes": {
                        "S": "Null"
                    },
                    "TripDailyExpenseDescription": {
                        "S": "In-area Travel"
                    },
                    "TripDailyExpenseType": {
                        "S": "In-area Travel"
                    },
                    "TripDailyExpenseAmount": {
                        "S": "3.00"
                    }
                }
            },
            {
                "M": {
                    "TripDailyExpenseDate": {
                        "S": "2021-03-07"
                    },
                    "TripDailyExpenseNotes": {
                        "S": "Null"
                    },
                    "TripDailyExpenseDescription": {
                        "S": "Alone stay per night"
                    },
                    "TripDailyExpenseType": {
                        "S": "Accommodation"
                    },
                    "TripDailyExpenseAmount": {
                        "S": "0.00"
                    }
                }
            },
            {
                "M": {
                    "TripDailyExpenseDate": {
                        "S": "2021-03-07"
                    },
                    "TripDailyExpenseNotes": {
                        "S": "TEST DATA UPDATED"
                    },
                    "TripDailyExpenseDescription": {
                        "S": "From Prek Prasab to Phnum Sruoch"
                    },
                    "TripDailyExpenseType": {
                        "S": "Travel Fee"
                    },
                    "TripDailyExpenseAmount": {
                        "S": "3.00"
                    }
                }
            }
        ]
    },
    "TenantId": {
        "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
    },
    "TripRequestCoveredByOther": {
        "S": "CoveredByOwnCompany"
    },
    "TripRequestDepartureDateTime": {
        "S": "2021-03-04 7:30"
    },
    "TripRequestTravelMode": {
        "S": "PublicTransport"
    },
    "TripRequestTripRoute": {
        "L": [
            {
                "M": {
                    "ReturnRoute": {
                        "M": {
                            "Date": {
                                "S": "2021-03-07 8:30"
                            },
                            "Route": {
                                "M": {
                                    "From": {
                                        "M": {
                                            "LocationLevel1": {
                                                "M": {
                                                    "LocationLevel1Id": {
                                                        "S": "LocationLevel1:c8d910d391a4314482aa4bfd61ede378"
                                                    },
                                                    "LocationLevel1Name": {
                                                        "S": "Kratie"
                                                    },
                                                    "LocationLevel2": {
                                                        "M": {
                                                            "LocationLevel2Id": {
                                                                "S": "LocationLevel2:e703ab5ab8328937e8b7a91d3c17d210"
                                                            },
                                                            "LocationLevel2Name": {
                                                                "S": "Prek Prasab"
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
                                                        "S": "LocationLevel1:f142a3e8ca8f5df1462dd36ad22245e5"
                                                    },
                                                    "LocationLevel1Name": {
                                                        "S": "Kampong Speu"
                                                    },
                                                    "LocationLevel2": {
                                                        "M": {
                                                            "LocationLevel2Id": {
                                                                "S": "LocationLevel2:43415b8b6ab8b1c9e542f7da5eb136d5"
                                                            },
                                                            "LocationLevel2Name": {
                                                                "S": "Phnum Sruoch"
                                                            }
                                                        }
                                                    }
                                                }
                                            }
                                        }
                                    }
                                }
                            }
                        }
                    },
                    "OtherRoute": {
                        "L": [
                            {
                                "M": {
                                    "Date": {
                                        "S": "2021-03-05 8:30"
                                    },
                                    "Route": {
                                        "M": {
                                            "Shop": {
                                                "L": [
                                                    {
                                                        "M": {
                                                            "ShopId": {
                                                                "S": "59564083-7e2c-4c79-8345-0b7d178f0355"
                                                            },
                                                            "ShopName": {
                                                                "S": "Samsung LG"
                                                            }
                                                        }
                                                    }
                                                ]
                                            },
                                            "From": {
                                                "M": {
                                                    "LocationLevel1": {
                                                        "M": {
                                                            "LocationLevel1Id": {
                                                                "S": "LocationLevel1:c8d910d391a4314482aa4bfd61ede378"
                                                            },
                                                            "LocationLevel1Name": {
                                                                "S": "Kratie"
                                                            },
                                                            "LocationLevel2": {
                                                                "M": {
                                                                    "LocationLevel2Id": {
                                                                        "S": "LocationLevel2:b5fb20fadc9552021625383e30e44d88"
                                                                    },
                                                                    "LocationLevel2Name": {
                                                                        "S": "Kracheh"
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
                                                                "S": "LocationLevel1:c8d910d391a4314482aa4bfd61ede378"
                                                            },
                                                            "LocationLevel1Name": {
                                                                "S": "Kratie"
                                                            },
                                                            "LocationLevel2": {
                                                                "M": {
                                                                    "LocationLevel2Id": {
                                                                        "S": "LocationLevel2:e703ab5ab8328937e8b7a91d3c17d210"
                                                                    },
                                                                    "LocationLevel2Name": {
                                                                        "S": "Prek Prasab"
                                                                    }
                                                                }
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
                                    "Date": {
                                        "S": "2021-03-06 10:30"
                                    },
                                    "Route": {
                                        "M": {
                                            "Shop": {
                                                "L": [
                                                    {
                                                        "M": {
                                                            "ShopId": {
                                                                "S": "1088dd48-a325-4c32-95ea-7802dcca3c5c"
                                                            },
                                                            "ShopName": {
                                                                "S": "Samsung"
                                                            }
                                                        }
                                                    }
                                                ]
                                            },
                                            "From": {
                                                "M": {
                                                    "LocationLevel1": {
                                                        "M": {
                                                            "LocationLevel1Id": {
                                                                "S": "LocationLevel1:c8d910d391a4314482aa4bfd61ede378"
                                                            },
                                                            "LocationLevel1Name": {
                                                                "S": "Kratie"
                                                            },
                                                            "LocationLevel2": {
                                                                "M": {
                                                                    "LocationLevel2Id": {
                                                                        "S": "LocationLevel2:b5fb20fadc9552021625383e30e44d88"
                                                                    },
                                                                    "LocationLevel2Name": {
                                                                        "S": "Kracheh"
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
                                                                "S": "LocationLevel1:c8d910d391a4314482aa4bfd61ede378"
                                                            },
                                                            "LocationLevel1Name": {
                                                                "S": "Kratie"
                                                            },
                                                            "LocationLevel2": {
                                                                "M": {
                                                                    "LocationLevel2Id": {
                                                                        "S": "LocationLevel2:e703ab5ab8328937e8b7a91d3c17d210"
                                                                    },
                                                                    "LocationLevel2Name": {
                                                                        "S": "Prek Prasab"
                                                                    }
                                                                }
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
                    },
                    "DepartureRoute": {
                        "M": {
                            "Date": {
                                "S": "2021-03-04 7:30"
                            },
                            "Route": {
                                "M": {
                                    "Shop": {
                                        "L": [
                                            {
                                                "M": {
                                                    "ShopId": {
                                                        "S": "59564083-7e2c-4c79-8345-0b7d178f0355"
                                                    },
                                                    "ShopName": {
                                                        "S": "Samsung LG"
                                                    }
                                                }
                                            },
                                            {
                                                "M": {
                                                    "ShopId": {
                                                        "S": "d5739d3d-0992-49fe-86c9-25d0015e735c"
                                                    },
                                                    "ShopName": {
                                                        "S": "Samsung Galaxy Store"
                                                    }
                                                }
                                            }
                                        ]
                                    },
                                    "From": {
                                        "M": {
                                            "LocationLevel1": {
                                                "M": {
                                                    "LocationLevel1Id": {
                                                        "S": "LocationLevel1:f142a3e8ca8f5df1462dd36ad22245e5"
                                                    },
                                                    "LocationLevel1Name": {
                                                        "S": "Kampong Speu"
                                                    },
                                                    "LocationLevel2": {
                                                        "M": {
                                                            "LocationLevel2Id": {
                                                                "S": "LocationLevel2:43415b8b6ab8b1c9e542f7da5eb136d5"
                                                            },
                                                            "LocationLevel2Name": {
                                                                "S": "Phnum Sruoch"
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
                                                        "S": "LocationLevel1:c8d910d391a4314482aa4bfd61ede378"
                                                    },
                                                    "LocationLevel1Name": {
                                                        "S": "Kratie"
                                                    },
                                                    "LocationLevel2": {
                                                        "M": {
                                                            "LocationLevel2Id": {
                                                                "S": "LocationLevel2:b5fb20fadc9552021625383e30e44d88"
                                                            },
                                                            "LocationLevel2Name": {
                                                                "S": "Kracheh"
                                                            }
                                                        }
                                                    }
                                                }
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
```

> The above HTTP request, if failure, will return Json structured like this:

```json
{
    "Resource": "aiml:dsa:trip-request/TripRequest:190fb791ce8eedee2c013d10796838b2",
    "Operation": "dsa:item-operation:Retrieves",
    "Message": "You're denied from performing the operation."
}
```

## Delete Info Of Trip Request
### HTTP Request
`DELETE dsa-svc/api/v1/trip-requests/{trip-request-id}`

### Query Paramaeters
Parameter       | Description
---------       | -----------
trip-request-id | Is the EntityItemId Of trip request

### HTTP Response
> The above HTTP request, if successful, will return Json structured like this:

```json
{
    "UnprocessedItems": [],
    "ConsumedCapacity": [
        {
            "TableName": "DsaDev",
            "CapacityUnits": 2
        }
    ],
    "@metadata": {
        "statusCode": 200,
        "effectiveUri": "https://dynamodb.ap-southeast-1.amazonaws.com",
        "headers": {
            "server": "Server",
            "date": "Wed, 17 Feb 2021 04:41:31 GMT",
            "content-type": "application/x-amz-json-1.0",
            "content-length": "87",
            "connection": "keep-alive",
            "x-amzn-requestid": "5RDEE8OQ7A5FTSJN3RND3N13NBVV4KQNSO5AEMVJF66Q9ASUAAJG",
            "x-amz-crc32": "1666787412"
        },
        "transferStats": {
            "http": [
                []
            ]
        }
    }
}
```

# Trip Expense

## Update the Trip Daily Expense

### HTTP Request
`PUT v1/trip-requests/{trip_request_id}`

### Query Paramaeters
Parameter                           | Description
---------                           | -----------
trip_request_id                     | The ID of the trip request to retrieve information

### Body Request

```json
{
    "TripRequest": {
        "Children": {
            "TripDailyExpense": [
                {
                    "TripDailyExpenseDate": "2021-03-04",
                    "TripDailyExpenseType": "Meal",
                    "TripDailyExpenseDescription": "Breakfast (2.00.$), Lunch (5.00.$), Diner (5.00.$)",
                    "TripDailyExpenseAmount": "12.00",
                    "TripDailyExpenseNotes": "Null"
                },
                {
                    "TripDailyExpenseDate": "2021-03-04",
                    "TripDailyExpenseType": "In-area Travel",
                    "TripDailyExpenseDescription": "In-area Travel",
                    "TripDailyExpenseAmount": "3.00",
                    "TripDailyExpenseNotes": "Null"
                },
                {
                    "TripDailyExpenseDate": "2021-03-04",
                    "TripDailyExpenseType": "Accommodation",
                    "TripDailyExpenseDescription": "Alone stay per night",
                    "TripDailyExpenseAmount": "15.00",
                    "TripDailyExpenseNotes": "Null"
                },
                {
                    "TripDailyExpenseDate": "2021-03-04",
                    "TripDailyExpenseType": "Travel Fee",
                    "TripDailyExpenseDescription": "From Phnum Sruoch to Kracheh",
                    "TripDailyExpenseAmount": "10.00",
                    "TripDailyExpenseNotes": "null"
                },
                {
                    "TripDailyExpenseDate": "2021-03-05",
                    "TripDailyExpenseType": "Meal",
                    "TripDailyExpenseDescription": "Breakfast (2.00.$), Lunch (5.00.$), Diner (5.00.$)",
                    "TripDailyExpenseAmount": "12.00",
                    "TripDailyExpenseNotes": "Null"
                },
                {
                    "TripDailyExpenseDate": "2021-03-05",
                    "TripDailyExpenseType": "In-area Travel",
                    "TripDailyExpenseDescription": "In-area Travel",
                    "TripDailyExpenseAmount": "3.00",
                    "TripDailyExpenseNotes": "Null"
                },
                {
                    "TripDailyExpenseDate": "2021-03-05",
                    "TripDailyExpenseType": "Accommodation",
                    "TripDailyExpenseDescription": "Alone stay per night",
                    "TripDailyExpenseAmount": "15.00",
                    "TripDailyExpenseNotes": "Null"
                },
                {
                    "TripDailyExpenseDate": "2021-03-05",
                    "TripDailyExpenseType": "Travel Fee",
                    "TripDailyExpenseDescription": "From Kracheh to Prek Prasab",
                    "TripDailyExpenseAmount": "3.00",
                    "TripDailyExpenseNotes": "null"
                },
                {
                    "TripDailyExpenseDate": "2021-03-06",
                    "TripDailyExpenseType": "Meal",
                    "TripDailyExpenseDescription": "Breakfast (2.00.$), Lunch (5.00.$), Diner (5.00.$)",
                    "TripDailyExpenseAmount": "12.00",
                    "TripDailyExpenseNotes": "Null"
                },
                {
                    "TripDailyExpenseDate": "2021-03-06",
                    "TripDailyExpenseType": "In-area Travel",
                    "TripDailyExpenseDescription": "In-area Travel",
                    "TripDailyExpenseAmount": "3.00",
                    "TripDailyExpenseNotes": "TEST LINE EXPENSE"
                },
                {
                    "TripDailyExpenseDate": "2021-03-06",
                    "TripDailyExpenseType": "Accommodation",
                    "TripDailyExpenseDescription": "Alone stay per night",
                    "TripDailyExpenseAmount": "15.00",
                    "TripDailyExpenseNotes": "Null"
                },
                {
                    "TripDailyExpenseDate": "2021-03-06",
                    "TripDailyExpenseType": "Travel Fee",
                    "TripDailyExpenseDescription": "From Kracheh to Prek Prasab",
                    "TripDailyExpenseAmount": "3.00",
                    "TripDailyExpenseNotes": "null"
                },
                {
                    "TripDailyExpenseDate": "2021-03-07",
                    "TripDailyExpenseType": "Meal",
                    "TripDailyExpenseDescription": "Breakfast (2.00.$), Lunch (5.00.$), Diner (5.00.$)",
                    "TripDailyExpenseAmount": "12.00",
                    "TripDailyExpenseNotes": "Null"
                },
                {
                    "TripDailyExpenseDate": "2021-03-07",
                    "TripDailyExpenseType": "In-area Travel",
                    "TripDailyExpenseDescription": "In-area Travel",
                    "TripDailyExpenseAmount": "3.00",
                    "TripDailyExpenseNotes": "Null"
                },
                {
                    "TripDailyExpenseDate": "2021-03-07",
                    "TripDailyExpenseType": "Accommodation",
                    "TripDailyExpenseDescription": "Alone stay per night",
                    "TripDailyExpenseAmount": "0.00",
                    "TripDailyExpenseNotes": "Null"
                },
                {
                    "TripDailyExpenseDate": "2021-03-07",
                    "TripDailyExpenseType": "Travel Fee",
                    "TripDailyExpenseDescription": "From Prek Prasab to Phnum Sruoch",
                    "TripDailyExpenseAmount": "3.00",
                    "TripDailyExpenseNotes": "TEST DATA UPDATED"
                }
            ]
        }
    }
}
```

### HTTP Response
> The above HTTP request, if successful, will return Json structured like this:

```json
{
    "CompositeAccessPatterns": {
        "S": "TripRequest#TripRequestLocalTrip:LocalTrip#TripRequestRequesterName:Jonh#TripRequestTravelMode:CompanyCar#TripRequestCoveredByOther:CoveredByOwnCompany"
    },
    "TripRequestLocalTrip": {
        "S": "LocalTrip"
    },
    "TripRequestRequesterName": {
        "S": "Jonh"
    },
    "TripRequestRequesterId": {
        "S": "93551f78-c2e2-4d47-bc5e-e2dad7ce5ba8"
    },
    "EntityItemId": {
        "S": "TripRequest:36aea7b372b7f0a7416e7af0f34e5146"
    },
    "TripRequestPurpose": {
        "S": "Test Shop On host server"
    },
    "TripRequestReturnDateTime": {
        "S": "2021-02-27 8:30"
    },
    "TripRequestTripDailyExpense": {
        "L": [
            {
                "M": {
                    "TripDailyExpenseDate": {
                        "S": "2021-02-22"
                    },
                    "TripDailyExpenseNotes": {
                        "S": "Test Update trip expense"
                    },
                    "TripDailyExpenseDescription": {
                        "S": "Breakfast (2.00.$), Lunch (5.00.$), Diner (5.00.$)"
                    },
                    "TripDailyExpenseType": {
                        "S": "Meal"
                    },
                    "TripDailyExpenseAmount": {
                        "S": "12.00"
                    }
                }
            },
            {
                "M": {
                    "TripDailyExpenseDate": {
                        "S": "2021-02-22"
                    },
                    "TripDailyExpenseNotes": {
                        "S": "test"
                    },
                    "TripDailyExpenseDescription": {
                        "S": "In-area Travel"
                    },
                    "TripDailyExpenseType": {
                        "S": "In-area Travel"
                    },
                    "TripDailyExpenseAmount": {
                        "S": "3.00"
                    }
                }
            },
            {
                "M": {
                    "TripDailyExpenseDate": {
                        "S": "2021-02-22"
                    },
                    "TripDailyExpenseNotes": {
                        "S": "Share Stay Per Night"
                    },
                    "TripDailyExpenseDescription": {
                        "S": "Alone stay per night"
                    },
                    "TripDailyExpenseType": {
                        "S": "Accommodation"
                    },
                    "TripDailyExpenseAmount": {
                        "S": "20.00"
                    }
                }
            },
            {
                "M": {
                    "TripDailyExpenseDate": {
                        "S": "2021-02-23"
                    },
                    "TripDailyExpenseNotes": {
                        "S": "Null"
                    },
                    "TripDailyExpenseDescription": {
                        "S": "Breakfast (2.00.$), Lunch (5.00.$), Diner (5.00.$)"
                    },
                    "TripDailyExpenseType": {
                        "S": "Meal"
                    },
                    "TripDailyExpenseAmount": {
                        "S": "12.00"
                    }
                }
            },
            {
                "M": {
                    "TripDailyExpenseDate": {
                        "S": "2021-02-23"
                    },
                    "TripDailyExpenseNotes": {
                        "S": "Null"
                    },
                    "TripDailyExpenseDescription": {
                        "S": "In-area Travel"
                    },
                    "TripDailyExpenseType": {
                        "S": "In-area Travel"
                    },
                    "TripDailyExpenseAmount": {
                        "S": "3.00"
                    }
                }
            },
            {
                "M": {
                    "TripDailyExpenseDate": {
                        "S": "2021-02-23"
                    },
                    "TripDailyExpenseNotes": {
                        "S": "Null"
                    },
                    "TripDailyExpenseDescription": {
                        "S": "Alone stay per night"
                    },
                    "TripDailyExpenseType": {
                        "S": "Accommodation"
                    },
                    "TripDailyExpenseAmount": {
                        "S": "0.00"
                    }
                }
            },
            {
                "M": {
                    "TripDailyExpenseDate": {
                        "S": "2021-02-22"
                    },
                    "TripDailyExpenseNotes": {
                        "S": "null"
                    },
                    "TripDailyExpenseDescription": {
                        "S": "From Kracheh to Phnum Sruoch"
                    },
                    "TripDailyExpenseType": {
                        "S": "Travel Fee"
                    },
                    "TripDailyExpenseAmount": {
                        "S": "10.00"
                    }
                }
            },
            {
                "M": {
                    "TripDailyExpenseDate": {
                        "S": "2021-02-22"
                    },
                    "TripDailyExpenseNotes": {
                        "S": "null"
                    },
                    "TripDailyExpenseDescription": {
                        "S": "From Kracheh to Prek Prasab"
                    },
                    "TripDailyExpenseType": {
                        "S": "Travel Fee"
                    },
                    "TripDailyExpenseAmount": {
                        "S": "3.00"
                    }
                }
            },
            {
                "M": {
                    "TripDailyExpenseDate": {
                        "S": "2021-02-23"
                    },
                    "TripDailyExpenseNotes": {
                        "S": "null"
                    },
                    "TripDailyExpenseDescription": {
                        "S": "From Phnum Sruoch to Prek Prasab"
                    },
                    "TripDailyExpenseType": {
                        "S": "Travel Fee"
                    },
                    "TripDailyExpenseAmount": {
                        "S": "8.00"
                    }
                }
            }
        ]
    },
    "TenantId": {
        "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
    },
    "TripRequestCoveredByOther": {
        "S": "CoveredByOwnCompany"
    },
    "TripRequestDepartureDateTime": {
        "S": "2021-02-26 7:30"
    },
    "TripRequestTravelMode": {
        "S": "CompanyCar"
    },
    "TripRequestTripRoute": {
        "L": [
            {
                "M": {
                    "ReturnRoute": {
                        "M": {
                            "Date": {
                                "S": "2021-02-27 8:30"
                            },
                            "Route": {
                                "M": {
                                    "From": {
                                        "M": {
                                            "LocationLevel1": {
                                                "M": {
                                                    "LocationLevel1Id": {
                                                        "S": "LocationLevel1:c8d910d391a4314482aa4bfd61ede378"
                                                    },
                                                    "LocationLevel1Name": {
                                                        "S": "Kratie"
                                                    },
                                                    "LocationLevel2": {
                                                        "M": {
                                                            "LocationLevel2Id": {
                                                                "S": "LocationLevel2:e703ab5ab8328937e8b7a91d3c17d210"
                                                            },
                                                            "LocationLevel2Name": {
                                                                "S": "Prek Prasab"
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
                                                        "S": "LocationLevel1:f142a3e8ca8f5df1462dd36ad22245e5"
                                                    },
                                                    "LocationLevel1Name": {
                                                        "S": "Kampong Speu"
                                                    },
                                                    "LocationLevel2": {
                                                        "M": {
                                                            "LocationLevel2Id": {
                                                                "S": "LocationLevel2:43415b8b6ab8b1c9e542f7da5eb136d5"
                                                            },
                                                            "LocationLevel2Name": {
                                                                "S": "Phnum Sruoch"
                                                            }
                                                        }
                                                    }
                                                }
                                            }
                                        }
                                    }
                                }
                            }
                        }
                    },
                    "OtherRoute": {
                        "L": [
                            {
                                "M": {
                                    "Date": {
                                        "S": "2021-02-26 8:30"
                                    },
                                    "Route": {
                                        "M": {
                                            "Shop": {
                                                "L": [
                                                    {
                                                        "M": {
                                                            "ShopId": {
                                                                "S": "59564083-7e2c-4c79-8345-0b7d178f0355"
                                                            },
                                                            "ShopName": {
                                                                "S": "Samsung LG"
                                                            }
                                                        }
                                                    }
                                                ]
                                            },
                                            "From": {
                                                "M": {
                                                    "LocationLevel1": {
                                                        "M": {
                                                            "LocationLevel1Id": {
                                                                "S": "LocationLevel1:c8d910d391a4314482aa4bfd61ede378"
                                                            },
                                                            "LocationLevel1Name": {
                                                                "S": "Kratie"
                                                            },
                                                            "LocationLevel2": {
                                                                "M": {
                                                                    "LocationLevel2Id": {
                                                                        "S": "LocationLevel2:b5fb20fadc9552021625383e30e44d88"
                                                                    },
                                                                    "LocationLevel2Name": {
                                                                        "S": "Kracheh"
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
                                                                "S": "LocationLevel1:c8d910d391a4314482aa4bfd61ede378"
                                                            },
                                                            "LocationLevel1Name": {
                                                                "S": "Kratie"
                                                            },
                                                            "LocationLevel2": {
                                                                "M": {
                                                                    "LocationLevel2Id": {
                                                                        "S": "LocationLevel2:e703ab5ab8328937e8b7a91d3c17d210"
                                                                    },
                                                                    "LocationLevel2Name": {
                                                                        "S": "Prek Prasab"
                                                                    }
                                                                }
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
                                    "Date": {
                                        "S": "2021-02-26 10:30"
                                    },
                                    "Route": {
                                        "M": {
                                            "Shop": {
                                                "L": [
                                                    {
                                                        "M": {
                                                            "ShopId": {
                                                                "S": "1088dd48-a325-4c32-95ea-7802dcca3c5c"
                                                            },
                                                            "ShopName": {
                                                                "S": "Samsung"
                                                            }
                                                        }
                                                    }
                                                ]
                                            },
                                            "From": {
                                                "M": {
                                                    "LocationLevel1": {
                                                        "M": {
                                                            "LocationLevel1Id": {
                                                                "S": "LocationLevel1:c8d910d391a4314482aa4bfd61ede378"
                                                            },
                                                            "LocationLevel1Name": {
                                                                "S": "Kratie"
                                                            },
                                                            "LocationLevel2": {
                                                                "M": {
                                                                    "LocationLevel2Id": {
                                                                        "S": "LocationLevel2:b5fb20fadc9552021625383e30e44d88"
                                                                    },
                                                                    "LocationLevel2Name": {
                                                                        "S": "Kracheh"
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
                                                                "S": "LocationLevel1:c8d910d391a4314482aa4bfd61ede378"
                                                            },
                                                            "LocationLevel1Name": {
                                                                "S": "Kratie"
                                                            },
                                                            "LocationLevel2": {
                                                                "M": {
                                                                    "LocationLevel2Id": {
                                                                        "S": "LocationLevel2:e703ab5ab8328937e8b7a91d3c17d210"
                                                                    },
                                                                    "LocationLevel2Name": {
                                                                        "S": "Prek Prasab"
                                                                    }
                                                                }
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
                    },
                    "DepartureRoute": {
                        "M": {
                            "Date": {
                                "S": "2021-02-26 7:30"
                            },
                            "Route": {
                                "M": {
                                    "Shop": {
                                        "L": [
                                            {
                                                "M": {
                                                    "ShopId": {
                                                        "S": "59564083-7e2c-4c79-8345-0b7d178f0355"
                                                    },
                                                    "ShopName": {
                                                        "S": "Samsung LG"
                                                    }
                                                }
                                            },
                                            {
                                                "M": {
                                                    "ShopId": {
                                                        "S": "d5739d3d-0992-49fe-86c9-25d0015e735c"
                                                    },
                                                    "ShopName": {
                                                        "S": "Samsung Galaxy Store"
                                                    }
                                                }
                                            }
                                        ]
                                    },
                                    "From": {
                                        "M": {
                                            "LocationLevel1": {
                                                "M": {
                                                    "LocationLevel1Id": {
                                                        "S": "LocationLevel1:f142a3e8ca8f5df1462dd36ad22245e5"
                                                    },
                                                    "LocationLevel1Name": {
                                                        "S": "Kampong Speu"
                                                    },
                                                    "LocationLevel2": {
                                                        "M": {
                                                            "LocationLevel2Id": {
                                                                "S": "LocationLevel2:43415b8b6ab8b1c9e542f7da5eb136d5"
                                                            },
                                                            "LocationLevel2Name": {
                                                                "S": "Phnum Sruoch"
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
                                                        "S": "LocationLevel1:c8d910d391a4314482aa4bfd61ede378"
                                                    },
                                                    "LocationLevel1Name": {
                                                        "S": "Kratie"
                                                    },
                                                    "LocationLevel2": {
                                                        "M": {
                                                            "LocationLevel2Id": {
                                                                "S": "LocationLevel2:b5fb20fadc9552021625383e30e44d88"
                                                            },
                                                            "LocationLevel2Name": {
                                                                "S": "Kracheh"
                                                            }
                                                        }
                                                    }
                                                }
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
```

# Travel Fee

## Create Trip Expense
### HTTP Request
`GET dsa-svc/api/locations/travelFee`

### Body Request
```json
{
    "TravelFee": {
        "TravelFeeFromLocationLevelId": "LocationLevel2:464b126eface9bb6782b93e6bc7f05f2",
        "TravelFeeFromLocationLevelName": "Kaoh Nheaek",
        "TravelFeeToLocationLevelId": "LocationLevel3:00c34b7db1603998e9d08e9a3dffa30c",
        "TravelFeeToLocationLevelName": "Yeang",
        "TravelFeeDistance": "457.00",
        "TravelFeeRate": "15.00"
    }
}
```
### HTTP Response
> The above HTTP request, if successful, will return Json structured like this:

```json
{
    "TravelFeeRate": {
        "S": "8.00"
    },
    "TravelFeeFromLocationId": {
        "S": "LocationLevel2:e703ab5ab8328937e8b7a91d3c17d210"
    },
    "TravelFeeFromLocationName": {
        "S": "Prek Prasab"
    },
    "EntityItemId": {
        "S": "TravelFee:e3be7592678c0f2ec54e9203751043b9"
    },
    "CompositeAccessPatterns": {
        "S": "TravelFee#TravelFeeFromLocationId:LocationLevel2:e703ab5ab8328937e8b7a91d3c17d210#TravelFeeFromLocationName:Prek Prasab#TravelFeeToLocationId:LocationLevel2:43415b8b6ab8b1c9e542f7da5eb136d5#TravelFeeToLocationName:Phnum Sruoch"
    },
    "TravelFeeToLocationId": {
        "S": "LocationLevel2:43415b8b6ab8b1c9e542f7da5eb136d5"
    },
    "TenantId": {
        "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
    },
    "TravelFeeToLocationName": {
        "S": "Phnum Sruoch"
    }
}
```

### HTTP Request Filter 
`GET dsa-svc/api/v1/trip-requests?contains=TripRequestRequesterName:Son`

### HTTP Response Filter
> The above HTTP request, if successful, will return Json structured like this:

```json
[
    {
        "CompositeAccessPatterns": {
            "S": "TripRequest#TripRequestLocalTrip:LocalTrip#TripRequestStatus:DRAFTED#TripRequestRequesterName:Dara#TripRequestTravelMode:RentalCar#TripRequestCoveredByOther:CoveredByOwnCompany"
        },
        "TripRequestLocalTrip": {
            "S": "LocalTrip"
        },
        "TripRequestJointTraveler": {
            "L": [
                {
                    "M": {
                        "JointTravelerEmployeePersonId": {
                            "S": "d8d6f92d-c683-4480-bc45-8324599f550d"
                        },
                        "JointTravelerPersonName": {
                            "S": "Lily"
                        }
                    }
                }
            ]
        },
        "TripRequestRequesterName": {
            "S": "Dara"
        },
        "TripRequestRequesterId": {
            "S": "93551f78-c2e2-4d47-bc5e-e2dad7ce5ba8"
        },
        "EntityItemId": {
            "S": "TripRequest:19ab3852ab49a0cb4dd408798ba7d670"
        },
        "TripRequestStatus": {
            "S": "DRAFTED"
        },
        "TripRequestPurpose": {
            "S": "Test Trip Expenses"
        },
        "TripRequestTripDailyExpense": {
            "L": [
                {
                    "M": {
                        "TripDailyExpenseDate": {
                            "S": "2021-02-12"
                        },
                        "TripDailyExpenseNotes": {
                            "S": "null"
                        },
                        "TripDailyExpenseDescription": {
                            "S": "From Phnom Penh at 8:03 AM to Battambong"
                        },
                        "TripDailyExpenseType": {
                            "S": "Travel Fee (Departure)"
                        },
                        "TripDailyExpenseAmount": {
                            "S": "8"
                        }
                    }
                },
                {
                    "M": {
                        "TripDailyExpenseDate": {
                            "S": "2021-02-12"
                        },
                        "TripDailyExpenseNotes": {
                            "S": "null"
                        },
                        "TripDailyExpenseDescription": {
                            "S": "Breakfast (2.00$), Lunch (5.00$), Diner (5.00$)"
                        },
                        "TripDailyExpenseType": {
                            "S": "Meal"
                        },
                        "TripDailyExpenseAmount": {
                            "S": "10"
                        }
                    }
                },
                {
                    "M": {
                        "TripDailyExpenseDate": {
                            "S": "2021-02-12"
                        },
                        "TripDailyExpenseNotes": {
                            "S": "null"
                        },
                        "TripDailyExpenseDescription": {
                            "S": "Travels in Battambong"
                        },
                        "TripDailyExpenseType": {
                            "S": "In-area Travel"
                        },
                        "TripDailyExpenseAmount": {
                            "S": "0"
                        }
                    }
                },
                {
                    "M": {
                        "TripDailyExpenseDate": {
                            "S": "2021-02-12"
                        },
                        "TripDailyExpenseNotes": {
                            "S": "null"
                        },
                        "TripDailyExpenseDescription": {
                            "S": "Alone stay per night"
                        },
                        "TripDailyExpenseType": {
                            "S": "Accommodation"
                        },
                        "TripDailyExpenseAmount": {
                            "S": "15"
                        }
                    }
                },
                {
                    "M": {
                        "TripDailyExpenseDate": {
                            "S": "2021-02-13"
                        },
                        "TripDailyExpenseNotes": {
                            "S": "null"
                        },
                        "TripDailyExpenseDescription": {
                            "S": "Breakfast (2.00$), Lunch (5.00$), Diner (5.00$)"
                        },
                        "TripDailyExpenseType": {
                            "S": "Meal"
                        },
                        "TripDailyExpenseAmount": {
                            "S": "7"
                        }
                    }
                },
                {
                    "M": {
                        "TripDailyExpenseDate": {
                            "S": "2021-02-13"
                        },
                        "TripDailyExpenseNotes": {
                            "S": "null"
                        },
                        "TripDailyExpenseDescription": {
                            "S": "Travels in Battambong"
                        },
                        "TripDailyExpenseType": {
                            "S": "In-area Travel"
                        },
                        "TripDailyExpenseAmount": {
                            "S": "0"
                        }
                    }
                },
                {
                    "M": {
                        "TripDailyExpenseDate": {
                            "S": "2021-02-13"
                        },
                        "TripDailyExpenseNotes": {
                            "S": "null"
                        },
                        "TripDailyExpenseDescription": {
                            "S": "Alone stay per night"
                        },
                        "TripDailyExpenseType": {
                            "S": "Accommodation"
                        },
                        "TripDailyExpenseAmount": {
                            "S": "0"
                        }
                    }
                },
                {
                    "M": {
                        "TripDailyExpenseDate": {
                            "S": "2021-02-13"
                        },
                        "TripDailyExpenseNotes": {
                            "S": "null"
                        },
                        "TripDailyExpenseDescription": {
                            "S": "From Battambong at 10:30 AM to Phnom Penh"
                        },
                        "TripDailyExpenseType": {
                            "S": "Travel Fee (Return)"
                        },
                        "TripDailyExpenseAmount": {
                            "S": "8.00"
                        }
                    }
                }
            ]
        },
        "TripRequestReturnDateTime": {
            "S": "2021-02-13 10:30:00"
        },
        "TripRequestCoveredByOther": {
            "S": "CoveredByOwnCompany"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "TripRequestDepartureDateTime": {
            "S": "2021-02-12 8:03:00"
        },
        "TripRequestTravelMode": {
            "S": "RentalCar"
        },
        "TripRequestShop": {
            "L": [
                {
                    "M": {
                        "ShopId": {
                            "S": "d8d6f92d-c683-4480-bc45-8324599f550d"
                        },
                        "ShopName": {
                            "S": "Sumsung"
                        }
                    }
                }
            ]
        },
        "TripRequestTripRoute": {
            "L": [
                {
                    "M": {
                        "Date": {
                            "S": "2021-02-15"
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
                                }
                            ]
                        }
                    }
                }
            ]
        }
    },
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
            "S": "TripRequest:2b64c9cb380bec9d5e506208de812ca3"
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
        "TripRequestShop": {
            "L": [
                {
                    "M": {
                        "ShopId": {
                            "S": "d8d6f92d-c683-4480-bc45-8324599f550d"
                        },
                        "ShopName": {
                            "S": "Sumsung"
                        }
                    }
                }
            ]
        },
        "TripRequestTripRoute": {
            "L": [
                {
                    "M": []
                }
            ]
        }
    }
]
```

## Get All Travel Fee
### HTTP Request
`GET dsa-svc/api/locations/travelFee`

### HTTP Response
> The above HTTP request, if successful, will return Json structured like this:

```json 
[
    {
        "TravelFeeRate": {
            "S": "8.00"
        },
        "TravelFeeFromLocationId": {
            "S": "LocationLevel2:e703ab5ab8328937e8b7a91d3c17d210"
        },
        "TravelFeeFromLocationName": {
            "S": "Prek Prasab"
        },
        "EntityItemId": {
            "S": "TravelFee:e3be7592678c0f2ec54e9203751043b9"
        },
        "CompositeAccessPatterns": {
            "S": "TravelFee#TravelFeeFromLocationId:LocationLevel2:e703ab5ab8328937e8b7a91d3c17d210#TravelFeeFromLocationName:Prek Prasab#TravelFeeToLocationId:LocationLevel2:43415b8b6ab8b1c9e542f7da5eb136d5#TravelFeeToLocationName:Phnum Sruoch"
        },
        "TravelFeeToLocationId": {
            "S": "LocationLevel2:43415b8b6ab8b1c9e542f7da5eb136d5"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "TravelFeeToLocationName": {
            "S": "Phnum Sruoch"
        }
    }
]
```

### HTTP Request Filter 
`GET dsa-svc/api/locations/travelFee?contains=TravelFeeFromLocationId:LocationLevel2:e703ab5ab8328937e8b7a91d3c17d210#TravelFeeToLocationId:LocationLevel2:43415b8b6ab8b1c9e542f7da5eb136d5`

### Query Paramaeters
Parameter                   | Description
---------                   | -----------
TravelFeeFromLocationId     | Is the location id of travel fee from
TravelFeeToLocationId       | Is the location id of travel fee to

### HTTP Response Filter
> The above HTTP request, if successful, will return Json structured like this:

```json 
[
    {
        "TravelFeeRate": {
            "S": "8.00"
        },
        "TravelFeeFromLocationId": {
            "S": "LocationLevel2:e703ab5ab8328937e8b7a91d3c17d210"
        },
        "TravelFeeFromLocationName": {
            "S": "Prek Prasab"
        },
        "EntityItemId": {
            "S": "TravelFee:e3be7592678c0f2ec54e9203751043b9"
        },
        "CompositeAccessPatterns": {
            "S": "TravelFee#TravelFeeFromLocationId:LocationLevel2:e703ab5ab8328937e8b7a91d3c17d210#TravelFeeFromLocationName:Prek Prasab#TravelFeeToLocationId:LocationLevel2:43415b8b6ab8b1c9e542f7da5eb136d5#TravelFeeToLocationName:Phnum Sruoch"
        },
        "TravelFeeToLocationId": {
            "S": "LocationLevel2:43415b8b6ab8b1c9e542f7da5eb136d5"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "TravelFeeToLocationName": {
            "S": "Phnum Sruoch"
        }
    }
]
```

# ContextData
## Get ContextData
### HTTP Request
`GET dsa-svc/api/initData`

### HTTP Response
> The above HTTP request, if successful, will return Json structured like this:

```json
[
    {
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "EntityItemId": {
            "S": "TripRequestContextData:df57896c7e3626c6e6c977e0dc3170e0"
        },
        "CompositeAccessPatterns": {
            "S": "TripRequestContextData"
        },
        "TripRequestContextDataData": {
            "L": [
                {
                    "M": {
                        "HomeCountry": {
                            "M": {
                                "Value": {
                                    "S": "Cambodia"
                                },
                                "MetaData": {
                                    "M": {
                                        "Label": {
                                            "S": "Home Country"
                                        },
                                        "Description": {
                                            "S": "Specify the country in which the main office is located."
                                        }
                                    }
                                }
                            }
                        },
                        "DepartureFrom": {
                            "L": [
                                {
                                    "M": {
                                        "Value": {
                                            "S": "BaseOffice"
                                        },
                                        "Label": {
                                            "S": "Base Office"
                                        }
                                    }
                                },
                                {
                                    "M": {
                                        "Value": {
                                            "S": "Destination"
                                        },
                                        "Label": {
                                            "S": "Destination"
                                        }
                                    }
                                }
                            ]
                        },
                        "CoveringAgent": {
                            "L": [
                                {
                                    "M": {
                                        "Value": {
                                            "S": "CoveredByOwnCompany"
                                        },
                                        "Label": {
                                            "S": "Covered by own company"
                                        },
                                        "Default": {
                                            "S": "YES"
                                        }
                                    }
                                },
                                {
                                    "M": {
                                        "Value": {
                                            "S": "CoveredByPartner"
                                        },
                                        "Label": {
                                            "S": "Covered by company's client or partner"
                                        },
                                        "Default": {
                                            "S": "NO"
                                        }
                                    }
                                }
                            ]
                        },
                        "ManagingOperation": {
                            "L": [
                                {
                                    "S": "dsa:item-operation:Retrieve"
                                },
                                {
                                    "S": "dsa:item-operation:Verify"
                                },
                                {
                                    "S": "dsa:item-operation:Return"
                                },
                                {
                                    "S": "dsa:item-operation:Reject"
                                },
                                {
                                    "S": "dsa:item-operation:Approve"
                                }
                            ]
                        },
                        "BasicOperation": {
                            "L": [
                                {
                                    "S": "dsa:item-operation:Create"
                                },
                                {
                                    "S": "dsa:item-operation:Retrieve"
                                },
                                {
                                    "S": "dsa:item-operation:Update"
                                },
                                {
                                    "S": "dsa:item-operation:Delete"
                                },
                                {
                                    "S": "dsa:item-operation:Submit"
                                }
                            ]
                        },
                        "TransportMode": {
                            "L": [
                                {
                                    "M": {
                                        "Value": {
                                            "S": "PublicTransport"
                                        },
                                        "Label": {
                                            "S": "PublicTransport"
                                        },
                                        "Default": {
                                            "S": "YES"
                                        }
                                    }
                                },
                                {
                                    "M": {
                                        "Value": {
                                            "S": "ComapnyCar"
                                        },
                                        "Label": {
                                            "S": "Company Car"
                                        },
                                        "Default": {
                                            "S": "NO"
                                        }
                                    }
                                },
                                {
                                    "M": {
                                        "Value": {
                                            "S": "RentalCar"
                                        },
                                        "Label": {
                                            "S": "Rental Car"
                                        },
                                        "Default": {
                                            "S": "NO"
                                        }
                                    }
                                }
                            ]
                        },
                        "OvernightStayMode": {
                            "L": [
                                {
                                    "M": {
                                        "Value": {
                                            "S": "AloneStayPerNight"
                                        },
                                        "Label": {
                                            "S": "Stay Alone"
                                        }
                                    }
                                },
                                {
                                    "M": {
                                        "Value": {
                                            "S": "ShareStayPerNight"
                                        },
                                        "Label": {
                                            "S": "Share with Another"
                                        }
                                    }
                                }
                            ]
                        },
                        "TripGeoScope": {
                            "L": [
                                {
                                    "M": {
                                        "Value": {
                                            "S": "LocalTrip"
                                        },
                                        "Label": {
                                            "S": "Local Trip"
                                        },
                                        "Default": {
                                            "S": "YES"
                                        }
                                    }
                                },
                                {
                                    "M": {
                                        "Value": {
                                            "S": "Oversea"
                                        },
                                        "Label": {
                                            "S": "Oversea Trip"
                                        },
                                        "Default": {
                                            "S": "NO"
                                        }
                                    }
                                }
                            ]
                        },
                        "HomeCity": {
                            "M": {
                                "Value": {
                                    "S": "Phnom Penh"
                                },
                                "MetaData": {
                                    "M": {
                                        "Label": {
                                            "S": "Home City"
                                        },
                                        "Description": {
                                            "S": "Specify the city in which the main office is located."
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
]
```

