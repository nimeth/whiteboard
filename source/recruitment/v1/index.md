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

# JobOrder
## Create JobOrder and JobVacancies

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

### HTTP Request

`POST https://dev.aimlapps.com/recruitment-svc/api/v1/job-orders`

## Get JobOrder
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

### HTTP Request

`GET https://dev.aimlapps.com/recruitment-svc/api/v1/job-orders`

<aside class="success">
Remember — a happy jobOrder is an authenticated Recruitment!
</aside>

## Get a Specific JobOrder

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

### HTTP Request

`GET https://dev.aimlapps.com/recruitment-svc/api/v1/job-orders/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the jobOrder to retrieve

## Delete a Specific JobOrder

```bash
curl "https://dev.aimlapps.com/recruitment-svc/api/v1/job-orders/JobOrder:7f584eaba7074d66d1e5e4863502e2fa"
  -H "Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw"
```

This endpoint delete a specific jobOrder.

<aside class="warning">If you're not using an administrator API key, note that some JobOrders will return 403 Forbidden if they are hidden for admins only.</aside>

### HTTP Request

`GET https://dev.aimlapps.com/recruitment-svc/api/v1/job-orders/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the jobOrder to delete

# JobVacacies

## Get JobVacancies don't specific JobOrder
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

### HTTP Request

`GET https://dev.aimlapps.com/recruitment-svc/api/v1/job-vacancies`

<aside class="success">
Remember — a happy jobOrder is an authenticated Recruitment!
</aside>

## Get JobVacancies specific JobOrder
```bash
curl "https://dev.aimlapps.com/recruitment-svc/api/v1/job-vacancies?contains=JobOrder:b74c6a8277b77079df061fc1da98f0cd"
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

### HTTP Request

`GET https://dev.aimlapps.com/recruitment-svc/api/v1/job-vacancies?contains=JobOrder:b74c6a8277b77079df061fc1da98f0cd`

<aside class="success">
Remember — a happy jobOrder is an authenticated Recruitment!
</aside>

# Init Data On Recruitment
## List Init data on Recruitment
```bash
curl "https://dev.aimlapps.com/recruitment-svc/api/v1/init"
  -H "Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw"
```

> The above command when submit JSON structured like this:

```json
{ 
    "Client":{
        "Iternal": {
            "Entity":[
                {
                    "EntityItemId": {
                        "S":"Client:931cc0bd784645abaa12df07bb6390c1"
                    },
                    "ClientEntityName":{
                        "S":"Van Dara"
                    },
                    "ClientEntityShortName":{
                        "S":"Dara"
                    }

                }, {
                    "EntityItemId": {
                        "S":"Client:931cc0bd784645abaa12df07bb6390c2"
                    },
                    "ClientEntityName":{
                        "S":"Nita Bunna"
                    },
                    "ClientEntityShortName":{
                        "S":"Nita"
                    }
                }, {
                    "EntityItemId": {
                        "S":"InternalClient:931cc0bd784645abaa12df07bb6390c3"
                    },
                    "ClientEntityName":{
                        "S":"Phorn Nary"
                    },
                    "ClientEntityShortName":{
                        "S":"Nary"
                    }
                }, {
                    "EntityItemId": {
                        "S":"InternalClient:931cc0bd784645abaa12df07bb6390c4"
                    },
                    "ClientEntityName":{
                        "S":"Kao Pisy"
                    },
                    "ClientEntityShortName":{
                        "S":"Pisy"
                    }
                }
            ],
            "JobProfile":[
                {
                    "EntityItemId": {
                        "S":"JobProfile:931cc0bd784645abaa12df07bb6390c1"
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
                    "PositionTitle":{
                        "S": "Web Developer"
                    }
                },{
                    "EntityItemId": {
                        "S":"JobProfile:931cc0bd784645abaa12df07bb6390c2"
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
                    "PositionTitle":{
                        "S": "HR"
                    }
                }

            ]
        },
        "External": [
            {
                "EntityItemId": {
                    "S":"Client:931cc0bd784645abaa12df07bb6390c5"
                },
                "ClientEntityName":{
                    "S":"Borumy Thida"
                },
                "ClientEntityShortName":{
                    "S":"Thida"
                },
                "JobProfile":[
                    {
                        "EntityItemId": {
                            "S":"JobProfile:931cc0bd784645abaa12df07bb6390c6"
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
                            "S":"Client:931cc0bd784645abaa12df07bb6390c5"
                        },
                        "PositionTitle":{
                            "S": "IT Officer"
                        }
                    },{
                        "EntityItemId": {
                            "S":"JobProfile:931cc0bd784645abaa12df07bb6390c7"
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
                            "S":"Client:931cc0bd784645abaa12df07bb6390c5"
                        },
                        "PositionTitle":{
                            "S": "Doctor"
                        }
                    }
                ]
            }, 
            {
                "EntityItemId": {
                    "S":"Client:931cc0bd784645abaa12df07bb6390c6"
                },
                "ClientEntityName":{
                    "S":"Dalin Many"
                },
                "ClientEntityShortName":{
                    "S":"Many"
                },
                "JobProfile":[
                    {
                        "EntityItemId": {
                            "S":"JobProfile:931cc0bd784645abaa12df07bb6390c8"
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
                            "S":"Client:931cc0bd784645abaa12df07bb6390c6"
                        },
                        "PositionTitle":{
                            "S": "Account"
                        }
                    },{
                        "EntityItemId": {
                            "S":"JobProfile:931cc0bd784645abaa12df07bb6390c9"
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
                            "S":"Client:931cc0bd784645abaa12df07bb6390c6"
                        },
                        "PositionTitle":{
                            "S": "Sale"
                        }
                    }
                ]
            },
            {
                "EntityItemId": {
                    "S":"Client:931cc0bd784645abaa12df07bb6390c7"
                },
                "ClientEntityName":{
                    "S":"Phech Dany"
                },
                "ClientEntityShortName":{
                    "S":"Dany"
                },
                "JobProfile":[
                    {
                        "EntityItemId": {
                            "S":"JobProfile:931cc0bd784645abaa12df07bb6390c10"
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
                            "S":"Client:931cc0bd784645abaa12df07bb6390c7"
                        },
                        "PositionTitle":{
                            "S": "Web Developer"
                        }
                    },{
                        "EntityItemId": {
                            "S":"JobProfile:931cc0bd784645abaa12df07bb6390c11"
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
                            "S":"Client:931cc0bd784645abaa12df07bb6390c7"
                        },
                        "PositionTitle":{
                            "S": "Mobile App Developer"
                        }
                    }
                ]
            }, 
            {
                "EntityItemId": {
                    "S":"Client:931cc0bd784645abaa12df07bb6390c8"
                },
                "ClientEntityName":{
                    "S":"Doung Chan"
                },
                "ClientEntityShortName":{
                    "S":"Chan"
                },
                "JobProfile":[
                    {
                        "EntityItemId": {
                            "S":"JobProfile:931cc0bd784645abaa12df07bb6390c12"
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
                            "S":"Client:931cc0bd784645abaa12df07bb6390c8"
                        },
                        "PositionTitle":{
                            "S": "Web Developer"
                        }
                    },{
                        "EntityItemId": {
                            "S":"JobProfile:931cc0bd784645abaa12df07bb6390c13"
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
                            "S":"Client:931cc0bd784645abaa12df07bb6390c8"
                        },
                        "PositionTitle":{
                            "S": "HR Manager"
                        }
                    }
                ]
            }
        ]
    }
    
}

```

This endpoint List init data on recruitment.

<aside class="warning">If you're not using an administrator API key, note that some JobOrders will return 403 Forbidden if they are hidden for admins only.</aside>

### HTTP Request

`GET https://dev.aimlapps.com/recruitment-svc/api/v1/init`

# Client Profile
## Create Client Profile

```bash
curl "https://dev.aimlapps.com/recruitment-svc/api/v1/client-profiles"
  -H "Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw"
```

> The above command when submit JSON structured like this:

```json

{
    "ClientProfile":{
        "ClientEntityName": "Phic Thida",
        "ClientEntityShortName": "Thida",
        "ClientType": "Internal", 
        "CompositeAccessPatterns": "Client#ClientEntityName:Phic Thida#ClientEntityShortName:Thida"
    }
}
```

This endpoint create a specific Client Profile.

<aside class="warning">If you're not using an administrator API key, note that some clientProfiles will return 403 Forbidden if they are hidden for admins only.</aside>

### HTTP Request

`POST https://dev.aimlapps.com/recruitment-svc/api/v1/client-profiles`

## Retrive Client Profile
```bash
curl "https://dev.aimlapps.com/recruitment-svc/api/v1/client-profiles"
  -H "Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw"
```

> The above command when submit JSON structured like this:

```json
[
    {
    
        "EntityItemId": "ClientProfile:931cc0bd784645abaa12df07bb6390c4",
        "ClientEntityName": "Phic Thida",
        "ClientEntityShortName": "Thida",
        "ClientType": "Internal", 
        "CompositeAccessPatterns": "ClientProfile#ClientEntityName:Phic Thida#ClientEntityShortName:Thida#ClientType:Internal"
    },
    {
        "EntityItemId": "ClientProfile:931cc0bd784645abaa12df07bb6390c5",
        "ClientEntityName": "Phen Davy",
        "ClientEntityShortName": "Thida",
        "ClientType": "External", 
        "CompositeAccessPatterns": "ClientProfile#ClientEntityName:Phen Davy#ClientEntityShortName:Davy#ClientType:Internal"
    }
]
```

This endpoint retrive a specific Client Profile.

<aside class="warning">If you're not using an administrator API key, note that some ClientProfiles will return 403 Forbidden if they are hidden for admins only.</aside>

### HTTP Request

`GET https://dev.aimlapps.com/recruitment-svc/api/v1/client-profiles`


## View Detaile Client Profile
```bash
curl "https://dev.aimlapps.com/recruitment-svc/api/v1/client-profiles/ClientProfile:931cc0bd784645abaa12df07bb6390c4"
  -H "Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw"
```

> The above command when submit JSON structured like this:

```json
{
    
    "EntityItemId": "ClientProfile:931cc0bd784645abaa12df07bb6390c4",
    "ClientEntityName": "Phic Thida",
    "ClientEntityShortName": "Thida",
    "ClientType": "Internal", 
    "CompositeAccessPatterns": "ClientProfile#ClientEntityName:Phic Thida#ClientEntityShortName:Thida#ClientType:Internal"
}
```

This endpoint view detail a specific Client.

<aside class="warning">If you're not using an administrator API key, note that some JobOrders will return 403 Forbidden if they are hidden for admins only.</aside>

### HTTP Request

`GET https://dev.aimlapps.com/recruitment-svc/api/v1/client-profiles/ClientProfile:931cc0bd784645abaa12df07bb6390c4`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the Client to View Detail each Client

## Update Client Profile
```bash
curl "https://dev.aimlapps.com/recruitment-svc/api/v1/client-profiles/ClientProfile:931cc0bd784645abaa12df07bb6390c4"
  -H "Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw"
```

> The above command when submit JSON structured like this:

```json
{
    "ClientProfile":{
        "EntityItemId": "ClientProfile:931cc0bd784645abaa12df07bb6390c4",
        "ClientEntityName": "Phic Thida",
        "ClientEntityShortName": "Thida",
        "ClientType": "Internal", 
        "CompositeAccessPatterns": "ClientProfile#ClientEntityName:Phic Thida#ClientEntityShortName:Thida#ClientType:Internal"
    }
}
```

This endpoint update a specific Client Profile.

<aside class="warning">If you're not using an administrator API key, note that some JobOrders will return 403 Forbidden if they are hidden for admins only.</aside>

### HTTP Request

`PUT https://dev.aimlapps.com/recruitment-svc/api/v1/client-profiles/ClientProfile:931cc0bd784645abaa12df07bb6390c4`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the Client to update Client Profile fild

## Delete Client Profile
```bash
curl "https://dev.aimlapps.com/recruitment-svc/api/v1/client-profiles/ClientProfile:931cc0bd784645abaa12df07bb6390c4"
  -H "Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw"
```


This endpoint Delete a specific Client Profile.

<aside class="warning">If you're not using an administrator API key, note that some JobOrders will return 403 Forbidden if they are hidden for admins only.</aside>

### HTTP Request

`DELETE https://dev.aimlapps.com/recruitment-svc/api/v1/client-profiles/ClientProfile:931cc0bd784645abaa12df07bb6390c4`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the Client to delete Client Profile

# CandidateBucket
## Create CandidateBucket

```bash
curl "https://dev.aimlapps.com/recruitment-svc/api/v1/candidate-buckets"
  -H "Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw"
```

> The above command when submit JSON structured like this:

```json

{
    "CandidateBucket": {
        "CandidateBucketPositionId": "Position:79526e35074d4799ab82cc37d4c79bf1",
        "Children":{
            "People":[
                {
                    "PeopleSex": "Male",
                    "PeopleName": "Chan Tha", 
                    "PeopleId": "People:4585454897fc431899dcdfc5b37ffad5" 
                },
                {
                    "PeopleSex": "Female",
                    "PeopleName": "Dara Mony",
                    "PeopleId": "People:4585454897fc431899dcdfc5b37fgdg5" 
                }
            ]
        }
    }
}
```

This endpoint create a specific CandidateBucket.

<aside class="warning">If you're not using an administrator API key, note that some Clients will return 403 Forbidden if they are hidden for admins only.</aside>

### HTTP Request

`POST https://dev.aimlapps.com/recruitment-svc/api/v1/CandidateBucket`

## Retrive CandidateBuckets
```bash
curl "https://dev.aimlapps.com/recruitment-svc/api/v1/candidate-buckets"
  -H "Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw"
```

> The above command when submit JSON structured like this:

```json
{
    "CandidateBucket": [
        {
            "CandidateBucketPositionId": {
                "S": "Position:79526e35074d4799ab82cc37d4c79bf1"
            },
            "TenantId": {
                "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
            },
            "CandidateBucketPeople": {
                "L": [
                    {
                        "M": {
                            "PeopleId": {
                                "S": "People:4585454897fc431899dcdfc5b37ffad5"
                            },
                            "PeopleName": {
                                "S": "Chan Tha"
                            },
                            "PeopleSex": {
                                "S": "Male"
                            }
                        }
                    },
                    {
                        "M": {
                            "PeopleId": {
                                "S": "People:4585454897fc431899dcdfc5b37fgdg5"
                            },
                            "PeopleName": {
                                "S": "Dara Mony"
                            },
                            "PeopleSex": {
                                "S": "Female"
                            }
                        }
                    }
                ]
            },
            "EntityItemId": {
                "S": "CandidateBucket:3ded93efc6ec6279ae1e6e973b215cea"
            },
            "CompositeAccessPatterns": {
                "S": "CandidateBucket"
            }
        }
    ],
    "FilterAttributes": [
        {
            "PositionTitle": "Position Title"
        }
    ]
}
```

This endpoint retrive CandidateBuckets.

<aside class="warning">If you're not using an administrator API key, note that some CandidateBuckets will return 403 Forbidden if they are hidden for admins only.</aside>

### HTTP Request

`GET https://dev.aimlapps.com/recruitment-svc/api/v1/candidate-buckets`


## View Detaile CandidateBucket
```bash
curl "https://dev.aimlapps.com/recruitment-svc/api/v1/candidate-buckets/CandidateBucket:3ded93efc6ec6279ae1e6e973b215cea"
  -H "Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw"
```

> The above command when submit JSON structured like this:

```json
{
    "CandidateBucket": [
        {
            "CandidateBucketPositionId": {
                "S": "Position:79526e35074d4799ab82cc37d4c79bf1"
            },
            "TenantId": {
                "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
            },
            "CandidateBucketPeople": {
                "L": [
                    {
                        "M": {
                            "PeopleId": {
                                "S": "People:4585454897fc431899dcdfc5b37ffad5"
                            },
                            "PeopleName": {
                                "S": "Chan Tha"
                            },
                            "PeopleSex": {
                                "S": "Male"
                            }
                        }
                    },
                    {
                        "M": {
                            "PeopleId": {
                                "S": "People:4585454897fc431899dcdfc5b37fgdg5"
                            },
                            "PeopleName": {
                                "S": "Dara Mony"
                            },
                            "PeopleSex": {
                                "S": "Female"
                            }
                        }
                    }
                ]
            },
            "EntityItemId": {
                "S": "CandidateBucket:3ded93efc6ec6279ae1e6e973b215cea"
            },
            "CompositeAccessPatterns": {
                "S": "CandidateBucket"
            }
        }
    ],
    "FilterAttributes": [
        {
            "PositionTitle": "Position Title"
        }
    ]
}
```

This endpoint view detail a specific CandidateBucket.

<aside class="warning">If you're not using an administrator API key, note that some JobOrders will return 403 Forbidden if they are hidden for admins only.</aside>

### HTTP Request

`GET https://dev.aimlapps.com/recruitment-svc/api/v1/candidate-buckets/CandidateBucket:3ded93efc6ec6279ae1e6e973b215cea`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the Client to View Detail each CandidateBucket

## Delete CandidateBucket
```bash
curl "https://dev.aimlapps.com/recruitment-svc/api/v1/candidate-buckets/CandidateBucket:3ded93efc6ec6279ae1e6e973b215cea"
  -H "Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw"
```


This endpoint Delete a specific Client Profile.

<aside class="warning">If you're not using an administrator API key, note that some CandidateBucket will return 403 Forbidden if they are hidden for admins only.</aside>

### HTTP Request

`DELETE https://dev.aimlapps.com/recruitment-svc/api/v1/candidate-buckets/CandidateBucket:3ded93efc6ec6279ae1e6e973b215cea`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the CandidateBucket to delete 