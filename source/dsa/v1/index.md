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
            "S": "TripRequest#TripRequestLocalTrip:LocalTrip#TripRequestStatus:DRAFTED#TripRequestRequesterName:Jonh#TripRequestTravelMode:PublicTransport#TripRequestCoveredByOther:CoveredByOwnCompany"
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
                            "S": "Zhinee"
                        }
                    }
                }
            ]
        },
        "TripRequestRequesterName": {
            "S": "Jonh"
        },
        "TripRequestRequesterId": {
            "S": "93551f78-c2e2-4d47-bc5e-e2dad7ce5ba8"
        },
        "EntityItemId": {
            "S": "TripRequest:befbdefb8dacf8da84cc9bb43f663157"
        },
        "TripRequestStatus": {
            "S": "DRAFTED"
        },
        "TripRequestPurpose": {
            "S": "Test Shop On host server"
        },
        "TripRequestTripDailyExpense": {
            "L": [
                {
                    "M": {
                        "TripDailyExpenseDate": {
                            "S": "2021-02-17"
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
                            "S": "12"
                        }
                    }
                },
                {
                    "M": {
                        "TripDailyExpenseDate": {
                            "S": "2021-02-17"
                        },
                        "TripDailyExpenseNotes": {
                            "S": "null"
                        },
                        "TripDailyExpenseDescription": {
                            "S": "Travels in Prek Prasab"
                        },
                        "TripDailyExpenseType": {
                            "S": "In-area Travel"
                        },
                        "TripDailyExpenseAmount": {
                            "S": "3"
                        }
                    }
                },
                {
                    "M": {
                        "TripDailyExpenseDate": {
                            "S": "2021-02-17"
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
                            "S": "2021-02-18"
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
                            "S": "12"
                        }
                    }
                },
                {
                    "M": {
                        "TripDailyExpenseDate": {
                            "S": "2021-02-18"
                        },
                        "TripDailyExpenseNotes": {
                            "S": "null"
                        },
                        "TripDailyExpenseDescription": {
                            "S": "Travels in Prek Prasab"
                        },
                        "TripDailyExpenseType": {
                            "S": "In-area Travel"
                        },
                        "TripDailyExpenseAmount": {
                            "S": "3"
                        }
                    }
                },
                {
                    "M": {
                        "TripDailyExpenseDate": {
                            "S": "2021-02-18"
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
                            "S": "2021-02-17"
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
                            "S": "2021-02-17"
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
                            "S": "2021-02-18"
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
                            "S": "8.00"
                        }
                    }
                }
            ]
        },
        "TripRequestReturnDateTime": {
            "S": "2021-02-18 8:30:00"
        },
        "TripRequestCoveredByOther": {
            "S": "CoveredByOwnCompany"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "TripRequestDepartureDateTime": {
            "S": "2021-02-17 7:30:00"
        },
        "TripRequestTravelMode": {
            "S": "PublicTransport"
        },
        "TripRequestTripRoute": {
            "L": [
                {
                    "M": {
                        "Date": {
                            "S": "2021-02-17"
                        },
                        "Route": {
                            "L": [
                                {
                                    "M": {
                                        "Shop": {
                                            "L": [
                                                {
                                                    "M": {
                                                        "ShopId": {
                                                            "S": "d8d6f92d-c683-4480-bc45-8324599f550d"
                                                        },
                                                        "ShopName": {
                                                            "S": "Sreymi Sumsung Shop branch 1"
                                                        }
                                                    }
                                                },
                                                {
                                                    "M": {
                                                        "ShopId": {
                                                            "S": "d8d6f92d-c683-4480-bc45-8324599f550d"
                                                        },
                                                        "ShopName": {
                                                            "S": "Sreymi Sumsung Shop branch 2"
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
                                },
                                {
                                    "M": {
                                        "Shop": {
                                            "L": [
                                                {
                                                    "M": {
                                                        "ShopId": {
                                                            "S": "d8d6f92d-c683-4480-bc45-8324599f550d"
                                                        },
                                                        "ShopName": {
                                                            "S": "Sophi Sumsung Shop branch 1"
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
                            ]
                        }
                    }
                },
                {
                    "M": {
                        "Date": {
                            "S": "2021-02-18"
                        },
                        "Route": {
                            "L": [
                                {
                                    "M": {
                                        "Shop": {
                                            "L": [
                                                {
                                                    "M": {
                                                        "ShopId": {
                                                            "S": "d8d6f92d-c683-4480-bc45-8324599f550d"
                                                        },
                                                        "ShopName": {
                                                            "S": "Ah mouy Sumsung Shop"
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
`GET dsa-svc/api/v1/trip-requests?contains=TripRequestRequesterName:Jonh`

### HTTP Response Filter
> The above HTTP request, if successful, will return Json structured like this:

```json
[
    {
        "CompositeAccessPatterns": {
            "S": "TripRequest#TripRequestLocalTrip:LocalTrip#TripRequestStatus:DRAFTED#TripRequestRequesterName:Jonh#TripRequestTravelMode:PublicTransport#TripRequestCoveredByOther:CoveredByOwnCompany"
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
                            "S": "Zhinee"
                        }
                    }
                }
            ]
        },
        "TripRequestRequesterName": {
            "S": "Jonh"
        },
        "TripRequestRequesterId": {
            "S": "93551f78-c2e2-4d47-bc5e-e2dad7ce5ba8"
        },
        "EntityItemId": {
            "S": "TripRequest:befbdefb8dacf8da84cc9bb43f663157"
        },
        "TripRequestStatus": {
            "S": "DRAFTED"
        },
        "TripRequestPurpose": {
            "S": "Test Shop On host server"
        },
        "TripRequestTripDailyExpense": {
            "L": [
                {
                    "M": {
                        "TripDailyExpenseDate": {
                            "S": "2021-02-17"
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
                            "S": "12"
                        }
                    }
                },
                {
                    "M": {
                        "TripDailyExpenseDate": {
                            "S": "2021-02-17"
                        },
                        "TripDailyExpenseNotes": {
                            "S": "null"
                        },
                        "TripDailyExpenseDescription": {
                            "S": "Travels in Prek Prasab"
                        },
                        "TripDailyExpenseType": {
                            "S": "In-area Travel"
                        },
                        "TripDailyExpenseAmount": {
                            "S": "3"
                        }
                    }
                },
                {
                    "M": {
                        "TripDailyExpenseDate": {
                            "S": "2021-02-17"
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
                            "S": "2021-02-18"
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
                            "S": "12"
                        }
                    }
                },
                {
                    "M": {
                        "TripDailyExpenseDate": {
                            "S": "2021-02-18"
                        },
                        "TripDailyExpenseNotes": {
                            "S": "null"
                        },
                        "TripDailyExpenseDescription": {
                            "S": "Travels in Prek Prasab"
                        },
                        "TripDailyExpenseType": {
                            "S": "In-area Travel"
                        },
                        "TripDailyExpenseAmount": {
                            "S": "3"
                        }
                    }
                },
                {
                    "M": {
                        "TripDailyExpenseDate": {
                            "S": "2021-02-18"
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
                            "S": "2021-02-17"
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
                            "S": "2021-02-17"
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
                            "S": "2021-02-18"
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
                            "S": "8.00"
                        }
                    }
                }
            ]
        },
        "TripRequestReturnDateTime": {
            "S": "2021-02-18 8:30:00"
        },
        "TripRequestCoveredByOther": {
            "S": "CoveredByOwnCompany"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "TripRequestDepartureDateTime": {
            "S": "2021-02-17 7:30:00"
        },
        "TripRequestTravelMode": {
            "S": "PublicTransport"
        },
        "TripRequestTripRoute": {
            "L": [
                {
                    "M": {
                        "Date": {
                            "S": "2021-02-17"
                        },
                        "Route": {
                            "L": [
                                {
                                    "M": {
                                        "Shop": {
                                            "L": [
                                                {
                                                    "M": {
                                                        "ShopId": {
                                                            "S": "d8d6f92d-c683-4480-bc45-8324599f550d"
                                                        },
                                                        "ShopName": {
                                                            "S": "Sreymi Sumsung Shop branch 1"
                                                        }
                                                    }
                                                },
                                                {
                                                    "M": {
                                                        "ShopId": {
                                                            "S": "d8d6f92d-c683-4480-bc45-8324599f550d"
                                                        },
                                                        "ShopName": {
                                                            "S": "Sreymi Sumsung Shop branch 2"
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
                                },
                                {
                                    "M": {
                                        "Shop": {
                                            "L": [
                                                {
                                                    "M": {
                                                        "ShopId": {
                                                            "S": "d8d6f92d-c683-4480-bc45-8324599f550d"
                                                        },
                                                        "ShopName": {
                                                            "S": "Sophi Sumsung Shop branch 1"
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
                            ]
                        }
                    }
                },
                {
                    "M": {
                        "Date": {
                            "S": "2021-02-18"
                        },
                        "Route": {
                            "L": [
                                {
                                    "M": {
                                        "Shop": {
                                            "L": [
                                                {
                                                    "M": {
                                                        "ShopId": {
                                                            "S": "d8d6f92d-c683-4480-bc45-8324599f550d"
                                                        },
                                                        "ShopName": {
                                                            "S": "Ah mouy Sumsung Shop"
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
                            ]
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
        "TripRequestDepartureDateTime": "2021-02-17 7:30:00",
        "TripRequestReturnDateTime": "2021-02-18 8:30:00",
        "TripRequestStatus": "DRAFTED",
        "TripRequestRequesterId": "93551f78-c2e2-4d47-bc5e-e2dad7ce5ba8",
        "TripRequestRequesterName": "Jonh",
        "TripRequestPurpose": "Test Shop On host server",
        "TripRequestTravelMode": "PublicTransport",
        "TripRequestCoveredByOther": "CoveredByOwnCompany",
        "Children": {
            "TripRoute": [
                {
                    "Date": "2021-02-17",
                    "Route": [
                        { 
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
                                    "ShopId": "d8d6f92d-c683-4480-bc45-8324599f550d",
                                    "ShopName": "Sreymi Sumsung Shop branch 1"
                                },
                                {
                                    "ShopId": "d8d6f92d-c683-4480-bc45-8324599f550d",
                                    "ShopName": "Sreymi Sumsung Shop branch 2"
                                }
                            ]
                        },
                        { 
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
                                    "ShopId": "d8d6f92d-c683-4480-bc45-8324599f550d",
                                    "ShopName": "Sophi Sumsung Shop branch 1"
                                }
                            ]
                        }
                    ]
                },
                {
                    "Date": "2021-02-18",
                    "Route": [
                        { 
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
                            },
                            "Shop": [
                                {
                                    "ShopId": "d8d6f92d-c683-4480-bc45-8324599f550d",
                                    "ShopName": "Ah mouy Sumsung Shop"
                                }
                            ]
                        }
                    ]
                }
            ],
            "JointTraveler": [
                {
                    "JointTravelerEmployeePersonId": "d8d6f92d-c683-4480-bc45-8324599f550d",
                    "JointTravelerPersonName": "Zhinee"
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
trip-request-id | Is the EntityItemId Of trip request

### Body Request

```json
{
    "TripRequest": {
        "TripRequestLocalTrip": "LocalTrip",
        "TripRequestDepartureDateTime": "2021-02-18 9:30:00",
        "TripRequestReturnDateTime": "2021-02-19 8:30:00",
        "TripRequestStatus": "DRAFTED",
        "TripRequestRequesterId": "93551f78-c2e2-4d47-bc5e-e2dad7ce5ba8",
        "TripRequestRequesterName": "Nuna",
        "TripRequestPurpose": "Test Update Data",
        "TripRequestTravelMode": "PublicTransport",
        "TripRequestCoveredByOther": "CoveredByOwnCompany",
        "Children": {
            "TripRoute": [
                {
                    "Date": "2021-02-17",
                    "Route": [
                        { 
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
                                    "LocationLevel1Id": "LocationLevel1:f142a3e8ca8f5df1462dd36ad22245e5",
                                    "LocationLevel1Name": "Kampong Speu",
                                    "LocationLevel2": {
                                        "LocationLevel2Id": "LocationLevel2:43415b8b6ab8b1c9e542f7da5eb136d5",
                                        "LocationLevel2Name": "Phnum Sruoch"
                                    }
                                }
                            },
                            "Shop": [
                                {
                                    "ShopId": "d8d6f92d-c683-4480-bc45-8324599f550d",
                                    "ShopName": "Mama Sumsung Shop branch 1"
                                },
                                {
                                    "ShopId": "d8d6f92d-c683-4480-bc45-8324599f550d",
                                    "ShopName": "Mama Sumsung Shop branch 2"
                                }
                            ]
                        },
                        { 
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
                                    "ShopId": "d8d6f92d-c683-4480-bc45-8324599f550d",
                                    "ShopName": "Same Sumsung Shop branch 1"
                                }
                            ]
                        }
                    ]
                },
                {
                    "Date": "2021-02-18",
                    "Route": [
                        { 
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
                                        "LocationLevel2Id": "LocationLevel2:e703ab5ab8328937e8b7a91d3c17d210",
                                        "LocationLevel2Name": "Prek Prasab"
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
                    "JointTravelerPersonName": "Zhinee"
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
        "S": "TripRequest#TripRequestLocalTrip:LocalTrip#TripRequestStatus:DRAFTED#TripRequestRequesterName:Nuna#TripRequestTravelMode:PublicTransport#TripRequestCoveredByOther:CoveredByOwnCompany"
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
                        "S": "Zhinee"
                    }
                }
            }
        ]
    },
    "TripRequestRequesterName": {
        "S": "Nuna"
    },
    "TripRequestRequesterId": {
        "S": "93551f78-c2e2-4d47-bc5e-e2dad7ce5ba8"
    },
    "EntityItemId": {
        "S": "TripRequest:0b02d7084eaf409130a85ff6f3e7d102"
    },
    "TripRequestStatus": {
        "S": "DRAFTED"
    },
    "TripRequestPurpose": {
        "S": "Test Update Data"
    },
    "TripRequestReturnDateTime": {
        "S": "2021-02-19 8:30:00"
    },
    "TripRequestTripDailyExpense": {
        "L": [
            {
                "M": {
                    "TripDailyExpenseDate": {
                        "S": "2021-02-18"
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
                        "S": "2021-02-18"
                    },
                    "TripDailyExpenseNotes": {
                        "S": "null"
                    },
                    "TripDailyExpenseDescription": {
                        "S": "null"
                    },
                    "TripDailyExpenseType": {
                        "S": "In-area Travel"
                    },
                    "TripDailyExpenseAmount": {
                        "S": "3"
                    }
                }
            },
            {
                "M": {
                    "TripDailyExpenseDate": {
                        "S": "2021-02-18"
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
                        "S": "2021-02-19"
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
                        "S": "12"
                    }
                }
            },
            {
                "M": {
                    "TripDailyExpenseDate": {
                        "S": "2021-02-19"
                    },
                    "TripDailyExpenseNotes": {
                        "S": "null"
                    },
                    "TripDailyExpenseDescription": {
                        "S": "null"
                    },
                    "TripDailyExpenseType": {
                        "S": "In-area Travel"
                    },
                    "TripDailyExpenseAmount": {
                        "S": "3"
                    }
                }
            },
            {
                "M": {
                    "TripDailyExpenseDate": {
                        "S": "2021-02-19"
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
                        "S": "2021-02-17"
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
                        "S": "2021-02-17"
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
                        "S": "2021-02-18"
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
        "S": "2021-02-18 9:30:00"
    },
    "TripRequestTravelMode": {
        "S": "PublicTransport"
    },
    "TripRequestTripRoute": {
        "L": [
            {
                "M": {
                    "Date": {
                        "S": "2021-02-17"
                    },
                    "Route": {
                        "L": [
                            {
                                "M": {
                                    "Shop": {
                                        "L": [
                                            {
                                                "M": {
                                                    "ShopId": {
                                                        "S": "d8d6f92d-c683-4480-bc45-8324599f550d"
                                                    },
                                                    "ShopName": {
                                                        "S": "Mama Sumsung Shop branch 1"
                                                    }
                                                }
                                            },
                                            {
                                                "M": {
                                                    "ShopId": {
                                                        "S": "d8d6f92d-c683-4480-bc45-8324599f550d"
                                                    },
                                                    "ShopName": {
                                                        "S": "Mama Sumsung Shop branch 2"
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
                            },
                            {
                                "M": {
                                    "Shop": {
                                        "L": [
                                            {
                                                "M": {
                                                    "ShopId": {
                                                        "S": "d8d6f92d-c683-4480-bc45-8324599f550d"
                                                    },
                                                    "ShopName": {
                                                        "S": "Same Sumsung Shop branch 1"
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
                        ]
                    }
                }
            },
            {
                "M": {
                    "Date": {
                        "S": "2021-02-18"
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
                        ]
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

### HTTP Response
> The above HTTP request, if successful, will return Json structured like this:

```json
[
    {
        "CompositeAccessPatterns": {
            "S": "TripRequest#TripRequestLocalTrip:LocalTrip#TripRequestStatus:DRAFTED#TripRequestRequesterName:SreyTa#TripRequestTravelMode:PublicTransport#TripRequestCoveredByOther:CoveredByOwnCompany"
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
                            "S": "MonySakor"
                        }
                    }
                }
            ]
        },
        "TripRequestRequesterName": {
            "S": "SreyTa"
        },
        "TripRequestRequesterId": {
            "S": "93551f78-c2e2-4d47-bc5e-e2dad7ce5ba8"
        },
        "EntityItemId": {
            "S": "TripRequest:3bad4ade93c24dcf9929934be4fe9495"
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
                            "S": "2021-02-17"
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
                            "S": "12"
                        }
                    }
                },
                {
                    "M": {
                        "TripDailyExpenseDate": {
                            "S": "2021-02-17"
                        },
                        "TripDailyExpenseNotes": {
                            "S": "null"
                        },
                        "TripDailyExpenseDescription": {
                            "S": "Travels in Thma Koul"
                        },
                        "TripDailyExpenseType": {
                            "S": "In-area Travel"
                        },
                        "TripDailyExpenseAmount": {
                            "S": "3"
                        }
                    }
                },
                {
                    "M": {
                        "TripDailyExpenseDate": {
                            "S": "2021-02-17"
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
                            "S": "2021-02-18"
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
                            "S": "12"
                        }
                    }
                },
                {
                    "M": {
                        "TripDailyExpenseDate": {
                            "S": "2021-02-18"
                        },
                        "TripDailyExpenseNotes": {
                            "S": "null"
                        },
                        "TripDailyExpenseDescription": {
                            "S": "Travels in Thma Koul"
                        },
                        "TripDailyExpenseType": {
                            "S": "In-area Travel"
                        },
                        "TripDailyExpenseAmount": {
                            "S": "3"
                        }
                    }
                },
                {
                    "M": {
                        "TripDailyExpenseDate": {
                            "S": "2021-02-18"
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
                            "S": "2021-02-17"
                        },
                        "TripDailyExpenseNotes": {
                            "S": "null"
                        },
                        "TripDailyExpenseDescription": {
                            "S": "From Prek Ruessey at 7:30 AM to Thma Koul"
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
        "TripRequestReturnDateTime": {
            "S": "2021-02-18 8:30:00"
        },
        "TripRequestCoveredByOther": {
            "S": "CoveredByOwnCompany"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "TripRequestDepartureDateTime": {
            "S": "2021-02-17 7:30:00"
        },
        "TripRequestTravelMode": {
            "S": "PublicTransport"
        },
        "TripRequestTripRoute": {
            "L": [
                {
                    "M": {
                        "Shop": {
                            "L": [
                                {
                                    "M": {
                                        "ShopId": {
                                            "S": "d8d6f92d-c683-4480-bc45-8324599f550d"
                                        },
                                        "ShopName": {
                                            "S": "Sumsung Shop"
                                        }
                                    }
                                }
                            ]
                        },
                        "Date": {
                            "S": "2021-02-17"
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
                                                            "S": "LocationLevel1:581c0d3e739fe0ada7e91962b4ec2d6d"
                                                        },
                                                        "LocationLevel1Name": {
                                                            "S": "Kandal"
                                                        },
                                                        "LocationLevel2": {
                                                            "M": {
                                                                "LocationLevel2Id": {
                                                                    "S": "LocationLevel2:0dabd9ae90f9b48220d6449d2bbfd85c"
                                                                },
                                                                "LocationLevel3": {
                                                                    "M": {
                                                                        "LocationLevel3Id": {
                                                                            "S": "LocationLevel3:3a6c640ec33f8e0545e702bd54ec38b5"
                                                                        },
                                                                        "LocationLevel3Name": {
                                                                            "S": "Prek Ruessey"
                                                                        }
                                                                    }
                                                                },
                                                                "LocationLevel2Name": {
                                                                    "S": "Ta Khmau"
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
                                                            "S": "LocationLevel1:7ed870110dc3d34491b73fe37f02f370"
                                                        },
                                                        "LocationLevel1Name": {
                                                            "S": "Battambang"
                                                        },
                                                        "LocationLevel2": {
                                                            "M": {
                                                                "LocationLevel2Id": {
                                                                    "S": "LocationLevel2:0bcb3dbe94797e903d600e3efb144ac1"
                                                                },
                                                                "LocationLevel2Name": {
                                                                    "S": "Thma Koul"
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
            "S": "15.00"
        },
        "EntityItemId": {
            "S": "TravelFee:da88760e78fa70abfd540f0ca027e201"
        },
        "TravelFeeDistance": {
            "S": "457.00"
        },
        "TravelFeeFromLocationLevelId": {
            "S": "LocationLevel2:464b126eface9bb6782b93e6bc7f05f2"
        },
        "CompositeAccessPatterns": {
            "S": "TravelFee#TravelFeeFromLocationLevelId:LocationLevel2:464b126eface9bb6782b93e6bc7f05f2#TravelFeeFromLocationLevelName:Kaoh Nheaek#TravelFeeToLocationLevelId:LocationLevel3:00c34b7db1603998e9d08e9a3dffa30c#TravelFeeToLocationLevelName:Yeang"
        },
        "TravelFeeFromLocationLevelName": {
            "S": "Kaoh Nheaek"
        },
        "TravelFeeToLocationLevelId": {
            "S": "LocationLevel3:00c34b7db1603998e9d08e9a3dffa30c"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "TravelFeeToLocationLevelName": {
            "S": "Yeang"
        }
    },
    {
        "TravelFeeRate": {
            "S": "10.00"
        },
        "TravelFeeFromLocationLevel2Name": {
            "S": "Tuek Chhou"
        },
        "EntityItemId": {
            "S": "TravelFee:f522cb093b2b643b1701095d4e03d3a3"
        },
        "CompositeAccessPatterns": {
            "S": "TravelFee#TravelFeeFromLocationLevel2Id:LocationLevel2:38c46419461651167a9d94da2eb470dd#TravelFeeFromLocationLevel2Name:Tuek Chhou#TravelFeeToLocationLevel2Id:LocationLevel2:37ea3ede9376c13dae975c7184e642a4#TravelFeeToLocationLevel2Name:Saensokh"
        },
        "TravelFeeToLocationLevel2Id": {
            "S": "LocationLevel2:37ea3ede9376c13dae975c7184e642a4"
        },
        "TravelFeeFromLocationLevel2Id": {
            "S": "LocationLevel2:38c46419461651167a9d94da2eb470dd"
        },
        "TravelFeeToLocationLevel2Name": {
            "S": "Saensokh"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        }
    }
]
```
### HTTP Request Filter 
`GET dsa-svc/api/locations/travelFee?contains=LocationLevel2:029d52772c42cf101560c4c52d929d5d#LocationLevel2:d02b7673b0046130511cde65091e5067`

### HTTP Response Filter
> The above HTTP request, if successful, will return Json structured like this:

```json
[
    {
        "TravelFeeRate": {
            "S": "5.00"
        },
        "TravelFeeFromLocationLevel2Name": {
            "S": "Srei Santhor"
        },
        "EntityItemId": {
            "S": "TravelFee:7b596cff8fab077872671c0046fe5b87"
        },
        "CompositeAccessPatterns": {
            "S": "TravelFee#TravelFeeFromLocationLevel2Id:LocationLevel2:029d52772c42cf101560c4c52d929d5d#TravelFeeFromLocationLevel2Name:Srei Santhor#TravelFeeToLocationLevel2Id:LocationLevel2:d02b7673b0046130511cde65091e5067#TravelFeeToLocationLevel2Name:Angkor Borei"
        },
        "TravelFeeToLocationLevel2Id": {
            "S": "LocationLevel2:d02b7673b0046130511cde65091e5067"
        },
        "TravelFeeFromLocationLevel2Id": {
            "S": "LocationLevel2:029d52772c42cf101560c4c52d929d5d"
        },
        "TravelFeeToLocationLevel2Name": {
            "S": "Angkor Borei"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        }
    }
]
```