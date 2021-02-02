---
title: API Reference

language_tabs:
  - php
toc_footers:
  - <a href='#'>Sign Up for a Developer Key</a>
  - <a href='http://github.com/mpociot/whiteboard'>Documentation Powered by Whiteboard</a>

includes:
  - errors

search: true
---

# Introduction
Welcome to the Recruitment API! You can use our API access Recruitment API endpoints, which can get information on various candidate in our database.
# Authentication

> To authorize, use this code:

```php
# With shell, you can just pass the correct header with each request
curl "api_endpoint_here"
  -H "Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw"
```
>
Recruitment uses API keys to access to the API. You can get token after login.Recruitment expects for the API key to be included in all API requests to the server in a header that looks like the following:


`Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw`

<aside class="notice">
You must login to get token again after<code> expired token</code>.
</aside>

## JobOrder
### Create JobOrder and JobVacancies

```bash
curl "https://dev.aimlapps.com/recruitment-svc/api/v1/job-orders"
  -H "Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw"
```

> The above command when submit JSON structured like this:

```json
{
    "JobOrder": {
        "JobVacancyJobOrderId": "testing update",
        "JobOrderClientType": "internal",
        "JobOrderClientId": "Client:931cc0bd784645abaa12df07bb6390c8", 
        "JobOrderClientEntityName": "testing", 
        "JobOrderClientEntityShortName": "rrrrrrrrrrrrrrrrr", 
        "JobOrderDetail": "developer",
        "JobOrderReceiveDateTime": "2020-12-12 10:35:23", 
        "JobOrderCreatedDateTime": "2020-12-12 11:35:23", 
        "JobOrderCreatedById": "User:nauuua@aimlera.com", 
        "JobOrderCreatedByName": "Narggga", 
        "JobOrderSelectionProcessId": "SelectionProcess:025e103c1ac74e66aed9b7da0063609e",
        "CompositeAccessPatterns": "JobOrder#Client:931cc0bd784645abaa12df07bb6390c8#JobOrderCreatedByName:Nara#ReceiveDateTime:2020-11-30 16:25:33"
    },
    "Children":{
        "JobVacancy": [
            {
                "JobVacancyJobOrderId":"",
                "JobVacancyJobProfileId": "JobProfile:1b7d5c4fbaf64fb89433c7040866f446",
                "JobVacancyCountry": "Cambodiakkkk", 
                "JobVacancyHeadcount":"1", 
                "JobVacancyJobLevel": "Junior",
                "JobVacancyLocationLevel1": "Phnom Penh",
                "JobVacancyPositionTitle": "HR",
                "JobVacancyStatus": "Open",
                "JobVacancyTotalApplicant":"1", 
                "JobVacancyUrgencyLevel": "Medium"
            },{

                "JobVacancyJobOrderId":"",
                "JobVacancyJobProfileId": "JobProfile:1b7d5c4fbaf64fb89433c7040866f446",
                "JobVacancyCountry": "Cambodiammm", 
                "JobVacancyHeadcount":"1", 
                "JobVacancyJobLevel": "Junior",
                "JobVacancyLocationLevel1": "Phnom Penh",
                "JobVacancyPositionTitle": "HR Officer and Web developer",
                "JobVacancyStatus": "Open",
                "JobVacancyTotalApplicant":"1", 
                "JobVacancyUrgencyLevel": "Lage"
            }
        ]
    }
}
```

This endpoint create a specific jobOrder.

<aside class="warning">If you're not using an administrator API key, note that some JobOrders will return 403 Forbidden if they are hidden for admins only.</aside>

#### HTTP Request

`POST https://dev.aimlapps.com/recruitment-svc/api/v1/job-orders`

### Get JobOrder
```bash
curl "https://dev.aimlapps.com/recruitment-svc/api/v1/job-orders"
  -H "Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw"
```


> The above command returns JSON structured like this:

```json
[
    {
        "JobOrder":[
        {
            "JobOrderReceiveDateTime": {
                "S": "2021-01-08"
            },
            "CompositeAccessPatterns": {
                "S": "JobOrder#JobOrderClientEntityName:Van Dara#JobOrderClientEntityShortName:job#JobOrderReceiveDateTime:2021-01-08#JobOrderCreatedByName:Nagara"
            },
            "JobOrderJobTitle": [
                {
                    "S": "HR"
                },{
                    "S": "IT Officer"
                }
            ],
            "JobOrderClientEntityShortName": {
                "S": "job"
            },
            "JobOrderClientType": {
                "S": "InternalClient"
            },
            "JobOrderSelectionProcessId": {
                "S": "External client"
            },
            "JobOrderClientId": {
                "S": "Client:931cc0bd784645abaa12df07bb6390c8"
            },
            "JobOrderCreatedById": {
                "S": "User:nauuua@aimlera.com"
            },
            "JobOrderClientEntityName": {
                "S": "Van Dara"
            },
            "EntityItemId": {
                "S": "JobOrder:7f584eaba7074d66d1e5e4863502e2fa"
            },
            "JobOrderCreatedDateTime": {
                "S": "2021-01-28 09:56:23"
            },
            "JobOrderDetail": {
                "S": "test"
            },
            "TenantId": {
                "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
            },
            "JobOrderCreatedByName": {
                "S": "Nagara"
            }
        },
        {
            "JobOrderReceiveDateTime": {
                "S": "2021-01-20"
            },
            "CompositeAccessPatterns": {
                "S": "JobOrder#JobOrderClientEntityName:Sotheary#JobOrderClientEntityShortName:job#JobOrderReceiveDateTime:2021-01-20#JobOrderCreatedByName:NaKara"
            },
            "JobOrderClientEntityShortName": {
                "S": "job"
            },
            "JobOrderClientType": {
                "S": "Internal"
            },
            "JobOrderSelectionProcessId": {
                "S": "External client"
            },
            "JobOrderClientId": {
                "S": "Client:931cc0bd784645abaa12df07bb6390c8"
            },
            "JobOrderCreatedById": {
                "S": "User:nauuua@aimlera.com"
            },
            "JobOrderClientEntityName": {
                "S": "Sotheary"
            },
            "EntityItemId": {
                "S": "JobOrder:93ec5253eac1eeeb3927427149bc4de1"
            },
            "JobOrderCreatedDateTime": {
                "S": "2021-01-27 03:08:23"
            },
            "JobOrderDetail": {
                "S": "I am testing on this application"
            },
            "TenantId": {
                "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
            },
            "JobOrderCreatedByName": {
                "S": "NaKara"
            }
        } 
    ],
    "FilterAttributes":[
        {
        "JobOrderClientEntityName":"Client Name"
        },
        {
        "JobOrderClientEntityShortName":"Client Short Name"
        },
        {
        "JobOrderReceiveDateTime":"Receive Date Time"
        },
        {
        "JobOrderCreatedByName":"Created ByName"
        }

    ]
}
    
]

```

This endpoint retrieves all jobOrders.

#### HTTP Request

`GET https://dev.aimlapps.com/recruitment-svc/api/v1/job-orders`

<aside class="success">
Remember — a happy jobOrder is an authenticated Recruitment!
</aside>

### Get a Specific JobOrder

```bash
curl "https://dev.aimlapps.com/recruitment-svc/api/v1/job-orders/JobOrder:7f584eaba7074d66d1e5e4863502e2fa"
  -H "Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw"
```

> The above command returns JSON structured like this:

```json
[
    {
        "JobOrderReceiveDateTime": {
            "S": "2021-01-08"
        },
        "CompositeAccessPatterns": {
            "S": "JobOrder#JobOrderClientEntityName:Van Dara#JobOrderClientEntityShortName:job#JobOrderReceiveDateTime:2021-01-08#JobOrderCreatedByName:Nagara"
        },
        "JobOrderClientEntityShortName": {
            "S": "job"
        },
        "JobOrderClientType": {
            "S": "InternalClient"
        },
        "JobOrderSelectionProcessId": {
            "S": "External client"
        },
        "JobOrderClientId": {
            "S": "Client:931cc0bd784645abaa12df07bb6390c8"
        },
        "JobOrderCreatedById": {
            "S": "User:nauuua@aimlera.com"
        },
        "JobOrderClientEntityName": {
            "S": "Van Dara"
        },
        "EntityItemId": {
            "S": "JobOrder:7f584eaba7074d66d1e5e4863502e2fa"
        },
        "JobOrderCreatedDateTime": {
            "S": "2021-01-28 09:56:23"
        },
        "JobOrderDetail": {
            "S": "test"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "JobOrderCreatedByName": {
            "S": "Nagara"
        }
    }
]
```

This endpoint retrieves a specific jobOrder.

<aside class="warning">If you're not using an administrator API key, note that some JobOrders will return 403 Forbidden if they are hidden for admins only.</aside>

#### HTTP Request

`GET https://dev.aimlapps.com/recruitment-svc/api/v1/job-orders/<ID>`

#### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the jobOrder to retrieve

### Delete a Specific JobOrder

```bash
curl "https://dev.aimlapps.com/recruitment-svc/api/v1/job-orders/JobOrder:7f584eaba7074d66d1e5e4863502e2fa"
  -H "Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw"
```

This endpoint delete a specific jobOrder.

<aside class="warning">If you're not using an administrator API key, note that some JobOrders will return 403 Forbidden if they are hidden for admins only.</aside>

#### HTTP Request

`GET https://dev.aimlapps.com/recruitment-svc/api/v1/job-orders/<ID>`

#### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the jobOrder to delete

## JobVacacies

### Get JobVacancies don't specific JobOrder
```bash
curl "https://dev.aimlapps.com/recruitment-svc/api/v1/job-vacancies/"
  -H "Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw"
```


> The above command returns JSON structured like this:

```json
[
    {
        "JobVacancyJobOrderId": {
            "S": "JobOrder:b74c6a8277b77079df061fc1da98f0cd"
        },
        "JobVacancyHeadcount": {
            "N": "1"
        },
        "CompositeAccessPatterns": {
            "S": "JobOrder:b74c6a8277b77079df061fc1da98f0cd"
        },
        "JobVacancyStatus": {
            "S": "Open"
        },
        "JobVacancyUrgencyLevel": {
            "S": "Lage"
        },
        "JobVacancyPositionTitle": {
            "S": "HR Officer and Web developer"
        },
        "JobVacancyJobLevel": {
            "S": "Junior"
        },
        "EntityItemId": {
            "S": "JobVacancy:192752c8e1afad95c9e1fbff96b7bd23"
        },
        "JobVacancyLocationLevel1": {
            "S": "Phnom Penh"
        },
        "JobVacancyTotalApplicant": {
            "N": "1"
        },
        "JobVacancyCountry": {
            "S": "Cambodia"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "JobVacancyJobProfileId": {
            "S": "JobProfile:1b7d5c4fbaf64fb89433c7040866f446"
        }
    },
    {
        "JobVacancyJobOrderId": {
            "S": "JobOrder:b74c6a8277b77079df061fc1da98f0cd"
        },
        "JobVacancyHeadcount": {
            "N": "1"
        },
        "CompositeAccessPatterns": {
            "S": "JobOrder:b74c6a8277b77079df061fc1da98f0cd"
        },
        "JobVacancyStatus": {
            "S": "Open"
        },
        "JobVacancyUrgencyLevel": {
            "S": "Medium"
        },
        "JobVacancyPositionTitle": {
            "S": "HR"
        },
        "JobVacancyJobLevel": {
            "S": "Junior"
        },
        "EntityItemId": {
            "S": "JobVacancy:3acd5d1d144ea528d28a8d806a452a95"
        },
        "JobVacancyLocationLevel1": {
            "S": "Phnom Penh"
        },
        "JobVacancyTotalApplicant": {
            "N": "1"
        },
        "JobVacancyCountry": {
            "S": "Cambodia"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "JobVacancyJobProfileId": {
            "S": "JobProfile:1b7d5c4fbaf64fb89433c7040866f446"
        }
    },
    {
        "JobVacancyJobOrderId": {
            "S": "JobOrder:b74c6a8277b77079df061fc1da98f0cd"
        },
        "JobVacancyHeadcount": {
            "N": "1"
        },
        "CompositeAccessPatterns": {
            "S": "JobOrder:b74c6a8277b77079df061fc1da98f0cd"
        },
        "JobVacancyStatus": {
            "S": "Open"
        },
        "JobVacancyUrgencyLevel": {
            "S": "small"
        },
        "JobVacancyPositionTitle": {
            "S": "Accounting Manager"
        },
        "JobVacancyJobLevel": {
            "S": "Senoir"
        },
        "EntityItemId": {
            "S": "JobVacancy:99667f215d9017298aec6c95dd3ad1a2"
        },
        "JobVacancyLocationLevel1": {
            "S": "Phnom Penh"
        },
        "JobVacancyTotalApplicant": {
            "N": "1"
        },
        "JobVacancyCountry": {
            "S": "Cambodia"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "JobVacancyJobProfileId": {
            "S": "JobProfile:1b7d5c4fbaf64fb89433c7040866f446"
        }
    }
]
```

This endpoint retrieves all jobVacacies.

#### HTTP Request

`GET https://dev.aimlapps.com/recruitment-svc/api/v1/job-vacancies`

<aside class="success">
Remember — a happy jobOrder is an authenticated Recruitment!
</aside>

### Get JobVacancies specific JobOrder
```bash
curl "https://dev.aimlapps.com/recruitment-svc/api/v1/job-vacancies?contains/=JobOrder:b74c6a8277b77079df061fc1da98f0cd"
  -H "Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw"
```


> The above command returns JSON structured like this:

```json
[
    {
        "JobVacancyJobOrderId": {
            "S": "JobOrder:b74c6a8277b77079df061fc1da98f0cd"
        },
        "JobVacancyHeadcount": {
            "N": "1"
        },
        "CompositeAccessPatterns": {
            "S": "JobOrder:b74c6a8277b77079df061fc1da98f0cd"
        },
        "JobVacancyStatus": {
            "S": "Open"
        },
        "JobVacancyUrgencyLevel": {
            "S": "Lage"
        },
        "JobVacancyPositionTitle": {
            "S": "HR Officer and Web developer"
        },
        "JobVacancyJobLevel": {
            "S": "Junior"
        },
        "EntityItemId": {
            "S": "JobVacancy:192752c8e1afad95c9e1fbff96b7bd23"
        },
        "JobVacancyLocationLevel1": {
            "S": "Phnom Penh"
        },
        "JobVacancyTotalApplicant": {
            "N": "1"
        },
        "JobVacancyCountry": {
            "S": "Cambodia"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "JobVacancyJobProfileId": {
            "S": "JobProfile:1b7d5c4fbaf64fb89433c7040866f446"
        }
    },
    {
        "JobVacancyJobOrderId": {
            "S": "JobOrder:b74c6a8277b77079df061fc1da98f0cd"
        },
        "JobVacancyHeadcount": {
            "N": "1"
        },
        "CompositeAccessPatterns": {
            "S": "JobOrder:b74c6a8277b77079df061fc1da98f0cd"
        },
        "JobVacancyStatus": {
            "S": "Open"
        },
        "JobVacancyUrgencyLevel": {
            "S": "Medium"
        },
        "JobVacancyPositionTitle": {
            "S": "HR"
        },
        "JobVacancyJobLevel": {
            "S": "Junior"
        },
        "EntityItemId": {
            "S": "JobVacancy:3acd5d1d144ea528d28a8d806a452a95"
        },
        "JobVacancyLocationLevel1": {
            "S": "Phnom Penh"
        },
        "JobVacancyTotalApplicant": {
            "N": "1"
        },
        "JobVacancyCountry": {
            "S": "Cambodia"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "JobVacancyJobProfileId": {
            "S": "JobProfile:1b7d5c4fbaf64fb89433c7040866f446"
        }
    },
    {
        "JobVacancyJobOrderId": {
            "S": "JobOrder:b74c6a8277b77079df061fc1da98f0cd"
        },
        "JobVacancyHeadcount": {
            "N": "1"
        },
        "CompositeAccessPatterns": {
            "S": "JobOrder:b74c6a8277b77079df061fc1da98f0cd"
        },
        "JobVacancyStatus": {
            "S": "Open"
        },
        "JobVacancyUrgencyLevel": {
            "S": "small"
        },
        "JobVacancyPositionTitle": {
            "S": "Accounting Manager"
        },
        "JobVacancyJobLevel": {
            "S": "Senoir"
        },
        "EntityItemId": {
            "S": "JobVacancy:99667f215d9017298aec6c95dd3ad1a2"
        },
        "JobVacancyLocationLevel1": {
            "S": "Phnom Penh"
        },
        "JobVacancyTotalApplicant": {
            "N": "1"
        },
        "JobVacancyCountry": {
            "S": "Cambodia"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "JobVacancyJobProfileId": {
            "S": "JobProfile:1b7d5c4fbaf64fb89433c7040866f446"
        }
    }
]

```

This endpoint retrieves all jobVacancies under jobOrder.

#### HTTP Request

`GET https://dev.aimlapps.com/recruitment-svc/api/v1/job-vacancies?contains/=JobOrder:b74c6a8277b77079df061fc1da98f0cd`

<aside class="success">
Remember — a happy jobOrder is an authenticated Recruitment!
</aside>

## Init Data On Recruitment
### List Init data on Recruitment
```bash
curl "https://dev.aimlapps.com/recruitment-svc/api/v1/init"
  -H "Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw"
```

> The above command when submit JSON structured like this:

```json
{ 
    "clients":{
        "internal": {
            "entitlies":[
                {
                    "EntityItemId": {
                        "S":"InternalClient:931cc0bd784645abaa12df07bb6390c1"
                    },
                    "clientName":{
                        "S":"Van Dara"
                    },
                    "ClientEntityShortName":{
                        "S":"Dara"
                    }

                }, {
                    "EntityItemId": {
                        "S":"InternalClient:931cc0bd784645abaa12df07bb6390c2"
                    },
                    "clientName":{
                        "S":"Chan Rathana"
                    }
                }, {
                    "EntityItemId": {
                        "S":"InternalClient:931cc0bd784645abaa12df07bb6390c3"
                    },
                    "clientName":{
                        "S":"Phorn Nary"
                    },
                    "ClientEntityShortName":{
                        "S":"Nary"
                    }
                }, {
                    "EntityItemId": {
                        "S":"InternalClient:931cc0bd784645abaa12df07bb6390c4"
                    },
                    "clientName":{
                        "S":"Kao Pisy"
                    },
                    "ClientEntityShortName":{
                        "S":"Pisy"
                    }
                }
            ],
            "jobProfiles":[
                {
                    "EntityItemId": {
                        "S":"JobProfileInternalClient:931cc0bd784645abaa12df07bb6390c1"
                    },
                    "JobVacancyTotalApplicant": {
                        "N": "1"
                    },
                    "JobVacancyCountry": {
                        "S": "Cambodia"
                    },
                    "JobVacancyJobLevel": {
                        "S": "Senior"
                    },
                    "clientName":{
                        "S":"Van Dara"
                    },
                    "PositionTitle":{
                        "S": "Web Developer"
                    }
                },{
                    "EntityItemId": {
                        "S":"JobProfileInternalClient:931cc0bd784645abaa12df07bb6390c2"
                    },
                    "JobVacancyTotalApplicant": {
                        "N": "1"
                    },
                    "JobVacancyCountry": {
                        "S": "Cambodia"
                    },
                    "JobVacancyJobLevel": {
                        "S": "Senior"
                    },
                    "clientName":{
                        "S":"Van Dara"
                    },
                    "PositionTitle":{
                        "S": "Web Developer"
                    }
                }

            ]
        },
        "external": [
            {
                "EntityItemId": {
                    "S":"ExternalClient:931cc0bd784645abaa12df07bb6390c1"
                },
                "departmentName":{
                    "S":"Borumy Thida"
                },
                "ClientEntityShortName":{
                    "S":"Thida"
                }
            }, {
                "EntityItemId": {
                    "S":"ExternalClient:931cc0bd784645abaa12df07bb6390c2"
                },
                "departmentName":{
                    "S":"Dalin Many"
                },
                "ClientEntityShortName":{
                    "S":"Many"
                }
            }, {
                "EntityItemId": {
                    "S":"ExternalClient:931cc0bd784645abaa12df07bb6390c3"
                },
                "departmentName":{
                    "S":"Phech Dany"
                },
                "ClientEntityShortName":{
                    "S":"Dany"
                },
                "jobProfiles":[
                    {
                        "EntityItemId": {
                            "S":"JobProfileInternalClient:931cc0bd784645abaa12df07bb6390c1"
                        },
                        "JobVacancyTotalApplicant": {
                            "N": "1"
                        },
                        "JobVacancyCountry": {
                            "S": "Cambodia"
                        },
                        "JobVacancyJobLevel": {
                            "S": "Senior"
                        },
                        "ClientEntityItemId": {
                            "S":"ExternalClient:931cc0bd784645abaa12df07bb6390c3"
                        },
                        "PositionTitle":{
                            "S": "Web Developer"
                        }
                    },{
                        "EntityItemId": {
                            "S":"JobProfileInternalClient:931cc0bd784645abaa12df07bb6390c2"
                        },
                        "JobVacancyTotalApplicant": {
                            "N": "1"
                        },
                        "JobVacancyCountry": {
                            "S": "Cambodia"
                        },
                        "JobVacancyJobLevel": {
                            "S": "Senior"
                        },
                        "ClientEntityItemId": {
                            "S":"ExternalClient:931cc0bd784645abaa12df07bb6390c3"
                        },
                        "PositionTitle":{
                            "S": "Web Developer"
                        }
                    },
                ]
            }, {
                "EntityItemId": {
                    "S":"ExternalClient:931cc0bd784645abaa12df07bb6390c4"
                },
                "departmentName":{
                    "S":"Doung Chan"
                },
                "ClientEntityShortName":{
                    "S":"Chan"
                },
                "jobProfiles":[
                    {
                        "EntityItemId": {
                            "S":"JobProfileInternalClient:931cc0bd784645abaa12df07bb6390c1"
                        },
                        "JobVacancyTotalApplicant": {
                            "N": "1"
                        },
                        "JobVacancyCountry": {
                            "S": "Cambodia"
                        },
                        "JobVacancyJobLevel": {
                            "S": "Senior"
                        },
                        "ClientEntityItemId": {
                            "S":"ExternalClient:931cc0bd784645abaa12df07bb6390c4"
                        },
                        "PositionTitle":{
                            "S": "Web Developer"
                        }
                    },{
                        "EntityItemId": {
                            "S":"JobProfileInternalClient:931cc0bd784645abaa12df07bb6390c2"
                        },
                        "JobVacancyTotalApplicant": {
                            "N": "1"
                        },
                        "JobVacancyCountry": {
                            "S": "Cambodia"
                        },
                        "JobVacancyJobLevel": {
                            "S": "Senior"
                        },
                        "ClientEntityItemId": {
                            "S":"ExternalClient:931cc0bd784645abaa12df07bb6390c4"
                        },
                        "PositionTitle":{
                            "S": "Web Developer"
                        }
                    },
                ]
            }
        ]
    }
    
}

```

This endpoint List init data on recruitment.

<aside class="warning">If you're not using an administrator API key, note that some JobOrders will return 403 Forbidden if they are hidden for admins only.</aside>

#### HTTP Request

`GET https://dev.aimlapps.com/recruitment-svc/api/v1/init`

## Client Profile
### Create Client Profile

```bash
curl "https://dev.aimlapps.com/recruitment-svc/api/v1/clients"
  -H "Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw"
```

> The above command when submit JSON structured like this:

```json
{

    "clientName": "testing update",
    "ClientEntityShortName": "internal",
    "ClientType": "Internal", 
    "DepartmentName": "Rose Thida", 
    "CompositeAccessPatterns": "JobOrder#Client:931cc0bd784645abaa12df07bb6390c8#JobOrderCreatedByName:Nara#ReceiveDateTime:2020-11-30 16:25:33"
}
```

This endpoint create a specific jobOrder.

<aside class="warning">If you're not using an administrator API key, note that some JobOrders will return 403 Forbidden if they are hidden for admins only.</aside>

#### HTTP Request

`POST https://dev.aimlapps.com/recruitment-svc/api/v1/clients`

### Retrive Client Profile
#### Retrive Internal Clients
```bash
curl "https://dev.aimlapps.com/recruitment-svc/api/v1/clients?contains=internal"
  -H "Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw"
```

> The above command when submit JSON structured like this:

```json
{
    
    "EntityItemId": "Client:931cc0bd784645abaa12df07bb6390c4",
    "ClientName": "Rose Thida", 
    "ClientEntityShortName": "Nara",
    "ClientType": "Internal", 
    "CompositeAccessPatterns": ""
}
```

This endpoint retrive a specific Client Profile.

<aside class="warning">If you're not using an administrator API key, note that some JobOrders will return 403 Forbidden if they are hidden for admins only.</aside>

##### HTTP Request

`GET https://dev.aimlapps.com/recruitment-svc/api/v1/clients?contains=internal`

#### Retrive External Clients
```bash
curl "https://dev.aimlapps.com/recruitment-svc/api/v1/clients?contains=internal"
  -H "Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw"
```

> The above command when submit JSON structured like this:

```json
{
    
    "EntityItemId": "Client:931cc0bd784645abaa12df07bb6390c4",
    "ClientEntityShortName": "Nara",
    "ClientType": "Internal", 
    "DepartmentName": "Rose Thida", 
    "CompositeAccessPatterns": ""
}
```

This endpoint retrive a specific Internal Client.

<aside class="warning">If you're not using an administrator API key, note that some JobOrders will return 403 Forbidden if they are hidden for admins only.</aside>

##### HTTP Request

`GET https://dev.aimlapps.com/recruitment-svc/api/v1/clients?contains=external`

#### Retrive External Clients
```bash
curl "https://dev.aimlapps.com/recruitment-svc/api/v1/clients?contains=internal"
  -H "Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw"
```

> The above command when submit JSON structured like this:

```json
{
    
    "EntityItemId": "Client:931cc0bd784645abaa12df07bb6390c4",
    "ClientEntityShortName": "Nara",
    "ClientType": "Internal", 
    "DepartmentName": "Rose Thida", 
    "CompositeAccessPatterns": ""
}
```

This endpoint retrive a specific External Client.

<aside class="warning">If you're not using an administrator API key, note that some JobOrders will return 403 Forbidden if they are hidden for admins only.</aside>

##### HTTP Request

`GET https://dev.aimlapps.com/recruitment-svc/api/v1/clients?contains=external`

### View Detaile Client Profile
```bash
curl "https://dev.aimlapps.com/recruitment-svc/api/v1/clients/Client:931cc0bd784645abaa12df07bb6390c4"
  -H "Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw"
```

> The above command when submit JSON structured like this:

```json
{
    
    "EntityItemId": "Client:931cc0bd784645abaa12df07bb6390c4",
    "ClientEntityShortName": "Nara",
    "ClientType": "Internal", 
    "DepartmentName": "Rose Thida", 
    "CompositeAccessPatterns": ""
}
```

This endpoint view detail a specific Client.

<aside class="warning">If you're not using an administrator API key, note that some JobOrders will return 403 Forbidden if they are hidden for admins only.</aside>

#### HTTP Request

`GET https://dev.aimlapps.com/recruitment-svc/api/v1/clients/Client:931cc0bd784645abaa12df07bb6390c4`

#### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the Client to View Detail each Client

### Update Client Profile
```bash
curl "https://dev.aimlapps.com/recruitment-svc/api/v1/clients/Client:931cc0bd784645abaa12df07bb6390c4"
  -H "Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw"
```

> The above command when submit JSON structured like this:

```json
{
    "EntityItemId": "Client:931cc0bd784645abaa12df07bb6390c4",
    "ClientName": "Noun Nara",
    "ClientEntityShortName": "Nara",
    "ClientType": "Internal", 
    "DepartmentName": "Rose Thida", 
    "CompositeAccessPatterns": ""
}
```

This endpoint update a specific Client Profile.

<aside class="warning">If you're not using an administrator API key, note that some JobOrders will return 403 Forbidden if they are hidden for admins only.</aside>

#### HTTP Request

`PUT https://dev.aimlapps.com/recruitment-svc/api/v1/clients/Client:931cc0bd784645abaa12df07bb6390c4`

#### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the Client to update Client Profile fild

### Delete Client Profile
```bash
curl "https://dev.aimlapps.com/recruitment-svc/api/v1/clients/Client:931cc0bd784645abaa12df07bb6390c4"
  -H "Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw"
```


This endpoint Delete a specific Client Profile.

<aside class="warning">If you're not using an administrator API key, note that some JobOrders will return 403 Forbidden if they are hidden for admins only.</aside>

#### HTTP Request

`DELETE https://dev.aimlapps.com/recruitment-svc/api/v1/clients/Client:931cc0bd784645abaa12df07bb6390c4`

#### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the Client to delete Client Profile
