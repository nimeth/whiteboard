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

# Job Order
## Create Job Order and Job Vacancies

```bash
curl "https://dev.aimlapps.com/recruitment-svc/api/v1/job-orders"
  -H "Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw"
```

> The above command when submit JSON structured like this:

```json
{
    "JobOrder": {
        "JobOrderClientType": "Internal",
        "JobOrderClientId": "Client:931cc0bd784645abaa12df07bb6390c8", 
        "JobOrderClientEntityName": "testing", 
        "JobOrderClientEntityShortName": "rrrrrrrrrrrrrrrrr", 
        "JobOrderDetail": "developer",
        "JobOrderReceiveDateTime": "2020-12-12 10:35:23", 
        "JobOrderCreatedDateTime": "2020-12-12 11:35:23", 
        "JobOrderCreatedById": "User:nauuua@aimlera.com", 
        "JobOrderCreatedByName": "Narggga", 
        "JobOrderSelectionProcessId": "SelectionProcess:025e103c1ac74e66aed9b7da0063609e",
        "CompositeAccessPatterns": "JobOrder#Client:931cc0bd784645abaa12df07bb6390c8#JobOrderCreatedByName:Nara#ReceiveDateTime:2020-11-30 16:25:33",
        "Children":{
            "JobVacancy": [
                {
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
    
}
```

This endpoint create a specific jobOrder.

<aside class="warning">If you're not using an administrator API key, note that some JobOrders will return 403 Forbidden if they are hidden for admins only.</aside>

### HTTP Request

`POST https://dev.aimlapps.com/recruitment-svc/api/v1/job-orders`

## Get Job Order
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
                "S": "SelectionProcessId:931cc0bd784645abaa12df07bb6390c8"
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

## Get a Specific Job Order

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
            "S": ""
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

## Delete a Specific Job Order

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

## Get Job Vacancies don't specific Job Order
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

## Get Job Vacancies specific Job Order
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
        "Internal": {
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


## View Detail Client Profile
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

# Candidate Bucket
## Create Candidate Bucket

```bash
curl "https://dev.aimlapps.com/recruitment-svc/api/v1/candidate-buckets"
  -H "Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw"
```

> The above command when submit JSON structured like this:

```json

{
    "CandidateBucket": {
        "CandidateBucketPositionTitle": "Mobile Developer",
        "CandidateBucketPositionId": "Position:79526e35074d4799ab82cc37d4c79bf2",
        "CompositeAccessPatterns":"CandidateBucket#PositionTitle:HR Manager#Position:79526e35074d4799ab82cc37d4c79bf1",
        "Children":{
            "People":[
                {
                    "PeopleSex": "Male",
                    "PeopleName": "Theara sun", 
                    "PeopleId": "People:4585454897fc431899dcdfc5b37ffad5" 
                },
                {
                    "PeopleSex": "Female",
                    "PeopleName": "Vina chung",
                    "PeopleId": "People:4585454897fc431899dcdfc5b37fgdg5" 
                },
                {
                    "PeopleSex": "Female",
                    "PeopleName": "Kun Thida",
                    "PeopleId": "People:4585454897fc431899dcdfc5b37fgdg5" 
                },
                {
                    "PeopleSex": "Female",
                    "PeopleName": "Nita Kao",
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

## Retrive Candidate Buckets
```bash
curl "https://dev.aimlapps.com/recruitment-svc/api/v1/candidate-buckets"
  -H "Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw"
```

> The above command when submit JSON structured like this:

```json
{
    "CandidateBucket": [
        {
            "CandidateBucketPositionTitle": {
                "S": "IT Network System"
            },
            "CandidateBucketPositionId": {
                "S": "Position:79526e35074d4799ab82cc37d4c79bf2"
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
                                "S": "Dara Chan"
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
                                "S": "Kim Vuty"
                            },
                            "PeopleSex": {
                                "S": "Female"
                            }
                        }
                    },
                    {
                        "M": {
                            "PeopleId": {
                                "S": "People:4585454897fc431899dcdfc5b37fgdg5"
                            },
                            "PeopleName": {
                                "S": "Kun Thida"
                            },
                            "PeopleSex": {
                                "S": "Female"
                            }
                        }
                    },
                    {
                        "M": {
                            "PeopleId": {
                                "S": "People:4585454897fc431899dcdfc5b37fgdg5"
                            },
                            "PeopleName": {
                                "S": "Theavy Sut"
                            },
                            "PeopleSex": {
                                "S": "Female"
                            }
                        }
                    }
                ]
            },
            "EntityItemId": {
                "S": "CandidateBucket:ba521ce76bddbe924e7ee030bde3e6a8"
            },
            "CompositeAccessPatterns": {
                "S": "CandidateBucket#CandidateBucketPositionId:Position:79526e35074d4799ab82cc37d4c79bf2#CandidateBucketPositionTitle:IT Network System"
            }
        },
        {
            "CandidateBucketPositionTitle": {
                "S": "Mobile Developer"
            },
            "CandidateBucketPositionId": {
                "S": "Position:79526e35074d4799ab82cc37d4c79bf2"
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
                                "S": "Theara sun"
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
                                "S": "Vina chung"
                            },
                            "PeopleSex": {
                                "S": "Female"
                            }
                        }
                    },
                    {
                        "M": {
                            "PeopleId": {
                                "S": "People:4585454897fc431899dcdfc5b37fgdg5"
                            },
                            "PeopleName": {
                                "S": "Kun Thida"
                            },
                            "PeopleSex": {
                                "S": "Female"
                            }
                        }
                    },
                    {
                        "M": {
                            "PeopleId": {
                                "S": "People:4585454897fc431899dcdfc5b37fgdg5"
                            },
                            "PeopleName": {
                                "S": "Nita Kao"
                            },
                            "PeopleSex": {
                                "S": "Female"
                            }
                        }
                    }
                ]
            },
            "EntityItemId": {
                "S": "CandidateBucket:be9edf11b0b22a6d1ad3786a4bb47893"
            },
            "CompositeAccessPatterns": {
                "S": "CandidateBucket#CandidateBucketPositionId:Position:79526e35074d4799ab82cc37d4c79bf2#CandidateBucketPositionTitle:Mobile Developer"
            }
        }
    ],
    "FilterAttributes": [
        {
            "CandidateBucketPositionTitle": "Position Title"
        },
        {
            "CandidateBucketPositionId": "Position Id"
        }
    ]
}
```

This endpoint retrive CandidateBuckets.

<aside class="warning">If you're not using an administrator API key, note that some CandidateBuckets will return 403 Forbidden if they are hidden for admins only.</aside>

### HTTP Request

`GET https://dev.aimlapps.com/recruitment-svc/api/v1/candidate-buckets`


## View Detail Candidate Bucket
```bash
curl "https://dev.aimlapps.com/recruitment-svc/api/v1/candidate-buckets/CandidateBucket:be9edf11b0b22a6d1ad3786a4bb47893"
  -H "Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw"
```

> The above command when submit JSON structured like this:

```json
[
    {
        "CandidateBucketPositionTitle": {
            "S": "Mobile Developer"
        },
        "CandidateBucketPositionId": {
            "S": "Position:79526e35074d4799ab82cc37d4c79bf2"
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
                            "S": "Theara sun"
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
                            "S": "Vina chung"
                        },
                        "PeopleSex": {
                            "S": "Female"
                        }
                    }
                },
                {
                    "M": {
                        "PeopleId": {
                            "S": "People:4585454897fc431899dcdfc5b37fgdg5"
                        },
                        "PeopleName": {
                            "S": "Kun Thida"
                        },
                        "PeopleSex": {
                            "S": "Female"
                        }
                    }
                },
                {
                    "M": {
                        "PeopleId": {
                            "S": "People:4585454897fc431899dcdfc5b37fgdg5"
                        },
                        "PeopleName": {
                            "S": "Nita Kao"
                        },
                        "PeopleSex": {
                            "S": "Female"
                        }
                    }
                }
            ]
        },
        "EntityItemId": {
            "S": "CandidateBucket:be9edf11b0b22a6d1ad3786a4bb47893"
        },
        "CompositeAccessPatterns": {
            "S": "CandidateBucket#CandidateBucketPositionId:Position:79526e35074d4799ab82cc37d4c79bf2#CandidateBucketPositionTitle:Mobile Developer"
        }
    }
]
```

This endpoint view detail a specific CandidateBucket.

<aside class="warning">If you're not using an administrator API key, note that some JobOrders will return 403 Forbidden if they are hidden for admins only.</aside>

### HTTP Request

`GET https://dev.aimlapps.com/recruitment-svc/api/v1/candidate-buckets/CandidateBucket:be9edf11b0b22a6d1ad3786a4bb47893`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the Client to View Detail each CandidateBucket

## Delete Candidate Bucket
```bash
curl "https://dev.aimlapps.com/recruitment-svc/api/v1/candidate-buckets/CandidateBucket:be9edf11b0b22a6d1ad3786a4bb47893"
  -H "Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw"
```


This endpoint Delete a specific CandidateBucket.

<aside class="warning">If you're not using an administrator API key, note that some CandidateBucket will return 403 Forbidden if they are hidden for admins only.</aside>

### HTTP Request

`DELETE https://dev.aimlapps.com/recruitment-svc/api/v1/candidate-buckets/CandidateBucket:be9edf11b0b22a6d1ad3786a4bb47893`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the CandidateBucket to delete 

# Job Vacancy Applicant
## Create Job Vacancy Applicant

```bash
curl "https://dev.aimlapps.com/recruitment-svc/api/v1/job-vacancies/JobVacancy:1e9cf083a2c3b07f0078b1b82d7ed274/applicants"
  -H "Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw"
```

> The above command when submit JSON structured like this:

```json

[
    {
        "JobVacancyApplicant":{
            "JobVacancyApplicantJobVacancyId": "JobVacancy:e303c774cd6aaf492950011bf7e6b50f",
            "JobVacancyApplicantPeopleName": "tttt",
            "JobVacancyApplicantPeopleSex": "F",
            "JobVacancyApplicantCurrentStepId": "Step:ac3d4ee48c4c5e272d74ebd762ceaa41", 
            "JobVacancyApplicantCurrentStepTitle": "Arrang assessment/interview", 
            "JobVacancyApplicantProcessResult": "IN_PROGRESS",
            "CompositeAccessPatterns": "JobVacancyApplicant#JobVacancyApplicantPeopleName:SoTheara#JobVacancyApplicantCurrentStepTitle:ApplyJob#JobVacancyApplicantProcessResult:Pass"
        }
    },
      {
        "JobVacancyApplicant":{
            "JobVacancyApplicantJobVacancyId": "JobVacancy:e303c774cd6aaf492950011bf7e6b50f",
            "JobVacancyApplicantPeopleName": "tttt",
            "JobVacancyApplicantPeopleSex": "F",
            "JobVacancyApplicantCurrentStepId": "Step:ac3d4ee48c4c5e272d74ebd762ceaa41", 
            "JobVacancyApplicantCurrentStepTitle": "Arrang assessment/interview", 
            "JobVacancyApplicantProcessResult": "IN_PROGRESS",
            "CompositeAccessPatterns": "JobVacancyApplicant#JobVacancyApplicantPeopleName:SoTheara#JobVacancyApplicantCurrentStepTitle:ApplyJob#JobVacancyApplicantProcessResult:Pass"
        }
    }
           
]

```

This endpoint create a specific JobVacancy Applicant.

<aside class="warning">If you're not using an administrator API key, note that some JobVacancy Applicant will return 403 Forbidden if they are hidden for admins only.</aside>

### HTTP Request

`POST https://dev.aimlapps.com/recruitment-svc/api/v1/job-vacancies/JobVacancy:1e9cf083a2c3b07f0078b1b82d7ed274/applicants`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the JobVacancy 

## View Detail Job Vacancy Applicant
```bash
curl "https://dev.aimlapps.com/recruitment-svc/api/v1/job-vacancies/JobVacancy:412af8742b5a465db54cd5648b80bd72/applicants/JobVacancyApplicant:1fb61bd50be4434aa28a609f1d54e022"
  -H "Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw"
```

> The above command when submit JSON structured like this:

```json
{
    "PersonalData": {
        "JobVacancyApplicantCurrentStepId": {
            "S": "Step:ac3d4ee48c4c5e272d74ebd762ceaa41"
        },
        "JobVacancyApplicantPeopleName": {
            "S": "SamaiDUCH"
        },
        "JobVacancyApplicantPeopleId": {
            "S": "People:e303c774cd6aaf492950011bf7e6b50f"
        },
        "JobVacancyApplicantJobVacancyId": {
            "S": "JobVacancy:e303c774cd6aaf492950011bf7e6b50f"
        },
        "EntityItemId": {
            "S": "JobVacancyApplicant:aea453883098e9bccf5ca022a819a2b9"
        },
        "JobVacancyApplicantCurrentStepTitle": {
            "S": "Testing/Assessment"
        },
        "CompositeAccessPatterns": {
            "S": "JobVacancyApplicant#JobVacancyApplicantJobVacancyId:JobVacancy:e303c774cd6aaf492950011bf7e6b50f#JobVacancyApplicantPeopleName:SamaiDUCH#JobVacancyApplicantCurrentStepTitle:Testing/Assessment#JobVacancyApplicantProcessResult:IN_PROGRESS"
        },
        "JobVacancyApplicantPeopleSex": {
            "S": "F"
        },
        "JobVacancyApplicantProcessResult": {
            "S": "IN_PROGRESS"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        }
    },
    "CurrentStep": [
        {
            "ApplicantProcessingStepCompletedByName": {
                "S": "Not avalable"
            },
            "ApplicantProcessingStepTitle": {
                "S": "Testing/Assessment"
            },
            "CompositeAccessPatterns": {
                "S": "ApplicantProcessingStep#ApplicantProcessingStepTitle:Testing/Assessment#ApplicantProcessingStepStatus:IN_PROGRESS#ApplicantProcessingStepAddedByPeopleName:SamaiDUCH#ApplicantProcessingStepCompletedByName:Not avalable"
            },
            "ApplicantProcessingStepResult": {
                "S": "Not avalable"
            },
            "ApplicantProcessingStepStatus": {
                "S": "IN_PROGRESS"
            },
            "ApplicantProcessingJobVacancyApplicantId": {
                "S": "JobVacancyApplicant:aea453883098e9bccf5ca022a819a2b9"
            },
            "EntityItemId": {
                "S": "ApplicantProcessingStep:882bb66c864cdf4f3b0c1d242be39115"
            },
            "ApplicantProcessingStepActualCompleteDate": {
                "S": "Not avalable"
            },
            "ApplicantProcessingStepNote": {
                "S": "mmmmmmmmmmmmmmmmmm"
            },
            "ApplicantProcessingStepId": {
                "S": "Step:ac3d4ee48c4c5e272d74ebd762ceaa41"
            },
            "TenantId": {
                "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
            },
            "ApplicantProcessingStepAddedByPeopleName": {
                "S": "SamaiDUCH"
            },
            "ApplicantProcessingStepCompletedById": {
                "S": "Not avalable"
            },
            "ApplicantProcessingStepAddedByPeopleId": {
                "S": "People:e303c774cd6daafffR492950011bf7e6b50f"
            },
            "ApplicantProcessingStepPlannedCompleteDate": {
                "S": "08-02-2021"
            }
        }
    ],
    "CompleteStep": [
        {
            "ApplicantProcessingStepCompletedByName": {
                "S": "samaiduch"
            },
            "ApplicantProcessingStepTitle": {
                "S": "Conduct interview"
            },
            "CompositeAccessPatterns": {
                "S": "ApplicantProcessingStep#ApplicantProcessingStepTitle:Conduct interview#ApplicantProcessingStepStatus:DONE#ApplicantProcessingStepAddedByPeopleName:SamaiDUCH#ApplicantProcessingStepCompletedByName:samaiduch"
            },
            "ApplicantProcessingStepResult": {
                "S": "Accept offer?"
            },
            "ApplicantProcessingStepStatus": {
                "S": "DONE"
            },
            "ApplicantProcessingJobVacancyApplicantId": {
                "S": "JobVacancyApplicant:aea453883098e9bccf5ca022a819a2b9"
            },
            "EntityItemId": {
                "S": "ApplicantProcessingStep:0d90a5bb4a56c3bea9e6cb26b8d2b722"
            },
            "ApplicantProcessingStepActualCompleteDate": {
                "S": "2021-01-31"
            },
            "ApplicantProcessingStepNote": {
                "S": "testing"
            },
            "ApplicantProcessingStepId": {
                "S": "Step:ac3d4ee48c4c5e272d74ebd762ceaa41"
            },
            "ApplicantProcessingStepAddedByPeopleName": {
                "S": "SamaiDUCH"
            },
            "TenantId": {
                "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
            },
            "ApplicantProcessingStepAddedByPeopleId": {
                "S": "People:e303c774cd6daafffR492950011bf7e6b50f"
            },
            "ApplicantProcessingStepCompletedById": {
                "S": "user:1ab83367a398b6c66d04924d348abc06"
            },
            "ApplicantProcessingStepPlannedCompleteDate": {
                "S": "08-02-2021"
            }
        },
        {
            "ApplicantProcessingStepCompletedByName": {
                "S": "samaiduch"
            },
            "ApplicantProcessingStepTitle": {
                "S": "Send job offer note"
            },
            "CompositeAccessPatterns": {
                "S": "ApplicantProcessingStep#ApplicantProcessingStepTitle:Send job offer note#ApplicantProcessingStepStatus:DONE#ApplicantProcessingStepAddedByPeopleName:SamaiDUCH#ApplicantProcessingStepCompletedByName:samaiduch"
            },
            "ApplicantProcessingStepResult": {
                "S": "Accept offer?"
            },
            "ApplicantProcessingStepStatus": {
                "S": "DONE"
            },
            "ApplicantProcessingJobVacancyApplicantId": {
                "S": "JobVacancyApplicant:aea453883098e9bccf5ca022a819a2b9"
            },
            "EntityItemId": {
                "S": "ApplicantProcessingStep:2e76a54681fad66c613976cdff12c04a"
            },
            "ApplicantProcessingStepActualCompleteDate": {
                "S": "2021-02-02"
            },
            "ApplicantProcessingStepNote": {
                "S": "testing"
            },
            "ApplicantProcessingStepId": {
                "S": "Step:ac3d4ee48c4c5e272d74ebd762ceaa41"
            },
            "ApplicantProcessingStepAddedByPeopleName": {
                "S": "SamaiDUCH"
            },
            "TenantId": {
                "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
            },
            "ApplicantProcessingStepAddedByPeopleId": {
                "S": "People:e303c774cd6daafffR492950011bf7e6b50f"
            },
            "ApplicantProcessingStepCompletedById": {
                "S": "user:1ab83367a398b6c66d04924d348abc06"
            },
            "ApplicantProcessingStepPlannedCompleteDate": {
                "S": "08-02-2021"
            }
        },
        {
            "ApplicantProcessingStepCompletedByName": {
                "S": "samaiduch"
            },
            "ApplicantProcessingStepTitle": {
                "S": "Testing/Assessment"
            },
            "CompositeAccessPatterns": {
                "S": "ApplicantProcessingStep#ApplicantProcessingStepTitle:Testing/Assessment#ApplicantProcessingStepStatus:DONE#ApplicantProcessingStepAddedByPeopleName:SamaiDUCH#ApplicantProcessingStepCompletedByName:samaiduch"
            },
            "ApplicantProcessingStepResult": {
                "S": "Agree to processed?"
            },
            "ApplicantProcessingStepStatus": {
                "S": "DONE"
            },
            "ApplicantProcessingJobVacancyApplicantId": {
                "S": "JobVacancyApplicant:aea453883098e9bccf5ca022a819a2b9"
            },
            "EntityItemId": {
                "S": "ApplicantProcessingStep:4ca859000f0277de8040f074c4b7a2b5"
            },
            "ApplicantProcessingStepActualCompleteDate": {
                "S": "2021-02-23"
            },
            "ApplicantProcessingStepNote": {
                "S": "testing"
            },
            "ApplicantProcessingStepId": {
                "S": "Step:ac3d4ee48c4c5e272d74ebd762ceaa41"
            },
            "ApplicantProcessingStepAddedByPeopleName": {
                "S": "SamaiDUCH"
            },
            "TenantId": {
                "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
            },
            "ApplicantProcessingStepAddedByPeopleId": {
                "S": "People:e303c774cd6daafffR492950011bf7e6b50f"
            },
            "ApplicantProcessingStepCompletedById": {
                "S": "user:1ab83367a398b6c66d04924d348abc06"
            },
            "ApplicantProcessingStepPlannedCompleteDate": {
                "S": "08-02-2021"
            }
        },
        {
            "ApplicantProcessingStepCompletedByName": {
                "S": "samaiduch"
            },
            "ApplicantProcessingStepTitle": {
                "S": "Send job offer note"
            },
            "CompositeAccessPatterns": {
                "S": "ApplicantProcessingStep#ApplicantProcessingStepTitle:Send job offer note#ApplicantProcessingStepStatus:DONE#ApplicantProcessingStepAddedByPeopleName:SamaiDUCH#ApplicantProcessingStepCompletedByName:samaiduch"
            },
            "ApplicantProcessingStepResult": {
                "S": "Agree to processed?"
            },
            "ApplicantProcessingStepStatus": {
                "S": "DONE"
            },
            "ApplicantProcessingJobVacancyApplicantId": {
                "S": "JobVacancyApplicant:aea453883098e9bccf5ca022a819a2b9"
            },
            "EntityItemId": {
                "S": "ApplicantProcessingStep:605f561c05a84772dec9ada1674e3c2e"
            },
            "ApplicantProcessingStepActualCompleteDate": {
                "S": "2021-02-23"
            },
            "ApplicantProcessingStepNote": {
                "S": "Tesigngdskoankldvfiue"
            },
            "ApplicantProcessingStepId": {
                "S": "Step:ac3d4ee48c4c5e272d74ebd762ceaa41"
            },
            "ApplicantProcessingStepAddedByPeopleName": {
                "S": "SamaiDUCH"
            },
            "TenantId": {
                "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
            },
            "ApplicantProcessingStepAddedByPeopleId": {
                "S": "People:e303c774cd6daafffR492950011bf7e6b50f"
            },
            "ApplicantProcessingStepCompletedById": {
                "S": "user:1ab83367a398b6c66d04924d348abc06"
            },
            "ApplicantProcessingStepPlannedCompleteDate": {
                "S": "08-02-2021"
            }
        },
        {
            "ApplicantProcessingStepCompletedByName": {
                "S": "samaiduch"
            },
            "ApplicantProcessingStepTitle": {
                "S": "Recommend to client"
            },
            "CompositeAccessPatterns": {
                "S": "ApplicantProcessingStep#ApplicantProcessingStepTitle:Recommend to client#ApplicantProcessingStepStatus:DONE#ApplicantProcessingStepAddedByPeopleName:SamaiDUCH#ApplicantProcessingStepCompletedByName:samaiduch"
            },
            "ApplicantProcessingStepResult": {
                "S": "Shortlisted?"
            },
            "ApplicantProcessingStepStatus": {
                "S": "DONE"
            },
            "ApplicantProcessingJobVacancyApplicantId": {
                "S": "JobVacancyApplicant:aea453883098e9bccf5ca022a819a2b9"
            },
            "EntityItemId": {
                "S": "ApplicantProcessingStep:7ac9de85ce0e4305446303a419c9d019"
            },
            "ApplicantProcessingStepActualCompleteDate": {
                "S": "2021-02-25"
            },
            "ApplicantProcessingStepNote": {
                "S": "aaaaaaaaaaaaaa"
            },
            "ApplicantProcessingStepId": {
                "S": "Step:ac3d4ee48c4c5e272d74ebd762ceaa41"
            },
            "ApplicantProcessingStepAddedByPeopleName": {
                "S": "SamaiDUCH"
            },
            "TenantId": {
                "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
            },
            "ApplicantProcessingStepAddedByPeopleId": {
                "S": "People:e303c774cd6daafffR492950011bf7e6b50f"
            },
            "ApplicantProcessingStepCompletedById": {
                "S": "user:1ab83367a398b6c66d04924d348abc06"
            },
            "ApplicantProcessingStepPlannedCompleteDate": {
                "S": "08-02-2021"
            }
        },
        {
            "ApplicantProcessingStepCompletedByName": {
                "S": "samaiduch"
            },
            "ApplicantProcessingStepTitle": {
                "S": "Send job offer note"
            },
            "CompositeAccessPatterns": {
                "S": "ApplicantProcessingStep#ApplicantProcessingStepTitle:Send job offer note#ApplicantProcessingStepStatus:DONE#ApplicantProcessingStepAddedByPeopleName:SamaiDUCH#ApplicantProcessingStepCompletedByName:samaiduch"
            },
            "ApplicantProcessingStepResult": {
                "S": "Accept offer?"
            },
            "ApplicantProcessingStepStatus": {
                "S": "DONE"
            },
            "ApplicantProcessingJobVacancyApplicantId": {
                "S": "JobVacancyApplicant:aea453883098e9bccf5ca022a819a2b9"
            },
            "EntityItemId": {
                "S": "ApplicantProcessingStep:818e49f376b7fdd96c374125670fc0a1"
            },
            "ApplicantProcessingStepActualCompleteDate": {
                "S": "2021-02-09"
            },
            "ApplicantProcessingStepNote": {
                "S": "testing"
            },
            "ApplicantProcessingStepId": {
                "S": "Step:ac3d4ee48c4c5e272d74ebd762ceaa41"
            },
            "ApplicantProcessingStepAddedByPeopleName": {
                "S": "SamaiDUCH"
            },
            "TenantId": {
                "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
            },
            "ApplicantProcessingStepAddedByPeopleId": {
                "S": "People:e303c774cd6daafffR492950011bf7e6b50f"
            },
            "ApplicantProcessingStepCompletedById": {
                "S": "user:1ab83367a398b6c66d04924d348abc06"
            },
            "ApplicantProcessingStepPlannedCompleteDate": {
                "S": "08-02-2021"
            }
        },
        {
            "ApplicantProcessingStepCompletedByName": {
                "S": "samaiduch"
            },
            "ApplicantProcessingStepTitle": {
                "S": "Conduct interview"
            },
            "CompositeAccessPatterns": {
                "S": "ApplicantProcessingStep#ApplicantProcessingStepTitle:Conduct interview#ApplicantProcessingStepStatus:DONE#ApplicantProcessingStepAddedByPeopleName:SamaiDUCH#ApplicantProcessingStepCompletedByName:samaiduch"
            },
            "ApplicantProcessingStepResult": {
                "S": "Shortlisted?"
            },
            "ApplicantProcessingStepStatus": {
                "S": "DONE"
            },
            "ApplicantProcessingJobVacancyApplicantId": {
                "S": "JobVacancyApplicant:aea453883098e9bccf5ca022a819a2b9"
            },
            "EntityItemId": {
                "S": "ApplicantProcessingStep:84e0f6742a1d93f77026519c456e206b"
            },
            "ApplicantProcessingStepActualCompleteDate": {
                "S": "2021-02-25"
            },
            "ApplicantProcessingStepNote": {
                "S": "dcfvtgbyhnujmik"
            },
            "ApplicantProcessingStepId": {
                "S": "Step:ac3d4ee48c4c5e272d74ebd762ceaa41"
            },
            "ApplicantProcessingStepAddedByPeopleName": {
                "S": "SamaiDUCH"
            },
            "TenantId": {
                "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
            },
            "ApplicantProcessingStepAddedByPeopleId": {
                "S": "People:e303c774cd6daafffR492950011bf7e6b50f"
            },
            "ApplicantProcessingStepCompletedById": {
                "S": "user:1ab83367a398b6c66d04924d348abc06"
            },
            "ApplicantProcessingStepPlannedCompleteDate": {
                "S": "08-02-2021"
            }
        },
        {
            "ApplicantProcessingStepCompletedByName": {
                "S": "samaiduch"
            },
            "ApplicantProcessingStepTitle": {
                "S": "Send job offer note"
            },
            "CompositeAccessPatterns": {
                "S": "ApplicantProcessingStep#ApplicantProcessingStepTitle:Send job offer note#ApplicantProcessingStepStatus:DONE#ApplicantProcessingStepAddedByPeopleName:SamaiDUCH#ApplicantProcessingStepCompletedByName:samaiduch"
            },
            "ApplicantProcessingStepResult": {
                "S": "Shortlisted?"
            },
            "ApplicantProcessingStepStatus": {
                "S": "DONE"
            },
            "ApplicantProcessingJobVacancyApplicantId": {
                "S": "JobVacancyApplicant:aea453883098e9bccf5ca022a819a2b9"
            },
            "EntityItemId": {
                "S": "ApplicantProcessingStep:89b2410e3a6fc6f02c54172798152e94"
            },
            "ApplicantProcessingStepActualCompleteDate": {
                "S": "2021-02-25"
            },
            "ApplicantProcessingStepNote": {
                "S": "DATA TEST"
            },
            "ApplicantProcessingStepId": {
                "S": "Step:ac3d4ee48c4c5e272d74ebd762ceaa41"
            },
            "ApplicantProcessingStepAddedByPeopleName": {
                "S": "SamaiDUCH"
            },
            "TenantId": {
                "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
            },
            "ApplicantProcessingStepAddedByPeopleId": {
                "S": "People:e303c774cd6daafffR492950011bf7e6b50f"
            },
            "ApplicantProcessingStepCompletedById": {
                "S": "user:1ab83367a398b6c66d04924d348abc06"
            },
            "ApplicantProcessingStepPlannedCompleteDate": {
                "S": "08-02-2021"
            }
        },
        {
            "ApplicantProcessingStepCompletedByName": {
                "S": "samaiduch"
            },
            "ApplicantProcessingStepTitle": {
                "S": "Testing/Assessment"
            },
            "CompositeAccessPatterns": {
                "S": "ApplicantProcessingStep#ApplicantProcessingStepTitle:Testing/Assessment#ApplicantProcessingStepStatus:DONE#ApplicantProcessingStepAddedByPeopleName:SamaiDUCH#ApplicantProcessingStepCompletedByName:samaiduch"
            },
            "ApplicantProcessingStepResult": {
                "S": "Agree to processed?"
            },
            "ApplicantProcessingStepStatus": {
                "S": "DONE"
            },
            "ApplicantProcessingJobVacancyApplicantId": {
                "S": "JobVacancyApplicant:aea453883098e9bccf5ca022a819a2b9"
            },
            "EntityItemId": {
                "S": "ApplicantProcessingStep:8ce47fa212b98e83c6d849b17d908a97"
            },
            "ApplicantProcessingStepActualCompleteDate": {
                "S": "2021-02-01"
            },
            "ApplicantProcessingStepNote": {
                "S": "testing"
            },
            "ApplicantProcessingStepId": {
                "S": "Step:ac3d4ee48c4c5e272d74ebd762ceaa41"
            },
            "ApplicantProcessingStepAddedByPeopleName": {
                "S": "SamaiDUCH"
            },
            "TenantId": {
                "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
            },
            "ApplicantProcessingStepAddedByPeopleId": {
                "S": "People:e303c774cd6daafffR492950011bf7e6b50f"
            },
            "ApplicantProcessingStepCompletedById": {
                "S": "user:1ab83367a398b6c66d04924d348abc06"
            },
            "ApplicantProcessingStepPlannedCompleteDate": {
                "S": "08-02-2021"
            }
        },
        {
            "ApplicantProcessingStepCompletedByName": {
                "S": "samaiduch"
            },
            "ApplicantProcessingStepTitle": {
                "S": "Arrange accessment/interview/shortisting(ODI/Client)"
            },
            "CompositeAccessPatterns": {
                "S": "ApplicantProcessingStep#ApplicantProcessingStepTitle:Arrange accessment/interview/shortisting(ODI/Client)#ApplicantProcessingStepStatus:DONE#ApplicantProcessingStepAddedByPeopleName:SamaiDUCH#ApplicantProcessingStepCompletedByName:samaiduch"
            },
            "ApplicantProcessingStepResult": {
                "S": "Shortlisted?"
            },
            "ApplicantProcessingStepStatus": {
                "S": "DONE"
            },
            "ApplicantProcessingJobVacancyApplicantId": {
                "S": "JobVacancyApplicant:aea453883098e9bccf5ca022a819a2b9"
            },
            "EntityItemId": {
                "S": "ApplicantProcessingStep:8f0b318d8c3cda988d6363a3df736af9"
            },
            "ApplicantProcessingStepActualCompleteDate": {
                "S": "2021-02-25"
            },
            "ApplicantProcessingStepNote": {
                "S": "TEST UPDATE"
            },
            "ApplicantProcessingStepId": {
                "S": "Step:ac3d4ee48c4c5e272d74ebd762ceaa41"
            },
            "ApplicantProcessingStepAddedByPeopleName": {
                "S": "SamaiDUCH"
            },
            "TenantId": {
                "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
            },
            "ApplicantProcessingStepAddedByPeopleId": {
                "S": "People:e303c774cd6daafffR492950011bf7e6b50f"
            },
            "ApplicantProcessingStepCompletedById": {
                "S": "user:1ab83367a398b6c66d04924d348abc06"
            },
            "ApplicantProcessingStepPlannedCompleteDate": {
                "S": "08-02-2021"
            }
        },
        {
            "ApplicantProcessingStepCompletedByName": {
                "S": "samaiduch"
            },
            "ApplicantProcessingStepTitle": {
                "S": "Arrange accessment/interview/shortisting(ODI/Client)"
            },
            "CompositeAccessPatterns": {
                "S": "ApplicantProcessingStep#ApplicantProcessingStepTitle:Arrange accessment/interview/shortisting(ODI/Client)#ApplicantProcessingStepStatus:DONE#ApplicantProcessingStepAddedByPeopleName:SamaiDUCH#ApplicantProcessingStepCompletedByName:samaiduch"
            },
            "ApplicantProcessingStepResult": {
                "S": "Accept offer?"
            },
            "ApplicantProcessingStepStatus": {
                "S": "DONE"
            },
            "ApplicantProcessingJobVacancyApplicantId": {
                "S": "JobVacancyApplicant:aea453883098e9bccf5ca022a819a2b9"
            },
            "EntityItemId": {
                "S": "ApplicantProcessingStep:9c9b280938858c969edcca0196a003b8"
            },
            "ApplicantProcessingStepActualCompleteDate": {
                "S": "2021-02-23"
            },
            "ApplicantProcessingStepNote": {
                "S": "testing"
            },
            "ApplicantProcessingStepId": {
                "S": "Step:ac3d4ee48c4c5e272d74ebd762ceaa41"
            },
            "ApplicantProcessingStepAddedByPeopleName": {
                "S": "SamaiDUCH"
            },
            "TenantId": {
                "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
            },
            "ApplicantProcessingStepAddedByPeopleId": {
                "S": "People:e303c774cd6daafffR492950011bf7e6b50f"
            },
            "ApplicantProcessingStepCompletedById": {
                "S": "user:1ab83367a398b6c66d04924d348abc06"
            },
            "ApplicantProcessingStepPlannedCompleteDate": {
                "S": "08-02-2021"
            }
        },
        {
            "ApplicantProcessingStepCompletedByName": {
                "S": "samaiduch"
            },
            "ApplicantProcessingStepTitle": {
                "S": "Arrange accessment/interview/shortisting(ODI/Client)"
            },
            "CompositeAccessPatterns": {
                "S": "ApplicantProcessingStep#ApplicantProcessingStepTitle:Arrange accessment/interview/shortisting(ODI/Client)#ApplicantProcessingStepStatus:DONE#ApplicantProcessingStepAddedByPeopleName:SamaiDUCH#ApplicantProcessingStepCompletedByName:samaiduch"
            },
            "ApplicantProcessingStepResult": {
                "S": "Agree to processed?"
            },
            "ApplicantProcessingStepStatus": {
                "S": "DONE"
            },
            "ApplicantProcessingJobVacancyApplicantId": {
                "S": "JobVacancyApplicant:aea453883098e9bccf5ca022a819a2b9"
            },
            "EntityItemId": {
                "S": "ApplicantProcessingStep:9d7a6f6f43958bb906f2e6502bf01fb0"
            },
            "ApplicantProcessingStepActualCompleteDate": {
                "S": "2021-02-25"
            },
            "ApplicantProcessingStepNote": {
                "S": "UPDATE"
            },
            "ApplicantProcessingStepId": {
                "S": "Step:ac3d4ee48c4c5e272d74ebd762ceaa41"
            },
            "ApplicantProcessingStepAddedByPeopleName": {
                "S": "SamaiDUCH"
            },
            "TenantId": {
                "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
            },
            "ApplicantProcessingStepAddedByPeopleId": {
                "S": "People:e303c774cd6daafffR492950011bf7e6b50f"
            },
            "ApplicantProcessingStepCompletedById": {
                "S": "user:1ab83367a398b6c66d04924d348abc06"
            },
            "ApplicantProcessingStepPlannedCompleteDate": {
                "S": "08-02-2021"
            }
        },
        {
            "ApplicantProcessingStepCompletedByName": {
                "S": "samaiduch"
            },
            "ApplicantProcessingStepTitle": {
                "S": "Arrange accessment/interview/shortisting(ODI/Client)"
            },
            "CompositeAccessPatterns": {
                "S": "ApplicantProcessingStep#ApplicantProcessingStepTitle:Arrange accessment/interview/shortisting(ODI/Client)#ApplicantProcessingStepStatus:DONE#ApplicantProcessingStepAddedByPeopleName:SamaiDUCH#ApplicantProcessingStepCompletedByName:samaiduch"
            },
            "ApplicantProcessingStepResult": {
                "S": "Agree to processed?"
            },
            "ApplicantProcessingStepStatus": {
                "S": "DONE"
            },
            "ApplicantProcessingJobVacancyApplicantId": {
                "S": "JobVacancyApplicant:aea453883098e9bccf5ca022a819a2b9"
            },
            "EntityItemId": {
                "S": "ApplicantProcessingStep:bd4458ec25ea28b8de54be895813feca"
            },
            "ApplicantProcessingStepActualCompleteDate": {
                "S": "2021-02-01"
            },
            "ApplicantProcessingStepNote": {
                "S": "zzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzz"
            },
            "ApplicantProcessingStepId": {
                "S": "Step:ac3d4ee48c4c5e272d74ebd762ceaa41"
            },
            "ApplicantProcessingStepAddedByPeopleName": {
                "S": "SamaiDUCH"
            },
            "TenantId": {
                "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
            },
            "ApplicantProcessingStepAddedByPeopleId": {
                "S": "People:e303c774cd6daafffR492950011bf7e6b50f"
            },
            "ApplicantProcessingStepCompletedById": {
                "S": "user:1ab83367a398b6c66d04924d348abc06"
            },
            "ApplicantProcessingStepPlannedCompleteDate": {
                "S": "08-02-2021"
            }
        },
        {
            "ApplicantProcessingStepCompletedByName": {
                "S": "samaiduch"
            },
            "ApplicantProcessingStepTitle": {
                "S": "Send job offer note"
            },
            "CompositeAccessPatterns": {
                "S": "ApplicantProcessingStep#ApplicantProcessingStepTitle:Send job offer note#ApplicantProcessingStepStatus:DONE#ApplicantProcessingStepAddedByPeopleName:SamaiDUCH#ApplicantProcessingStepCompletedByName:samaiduch"
            },
            "ApplicantProcessingStepResult": {
                "S": "Accept offer?"
            },
            "ApplicantProcessingStepStatus": {
                "S": "DONE"
            },
            "ApplicantProcessingJobVacancyApplicantId": {
                "S": "JobVacancyApplicant:aea453883098e9bccf5ca022a819a2b9"
            },
            "EntityItemId": {
                "S": "ApplicantProcessingStep:d6d737fc53865fe33cd02a005d4fdbeb"
            },
            "ApplicantProcessingStepActualCompleteDate": {
                "S": "2021-02-23"
            },
            "ApplicantProcessingStepNote": {
                "S": "Updating Step Status"
            },
            "ApplicantProcessingStepId": {
                "S": "Step:ac3d4ee48c4c5e272d74ebd762ceaa41"
            },
            "ApplicantProcessingStepAddedByPeopleName": {
                "S": "SamaiDUCH"
            },
            "TenantId": {
                "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
            },
            "ApplicantProcessingStepAddedByPeopleId": {
                "S": "People:e303c774cd6daafffR492950011bf7e6b50f"
            },
            "ApplicantProcessingStepCompletedById": {
                "S": "user:1ab83367a398b6c66d04924d348abc06"
            },
            "ApplicantProcessingStepPlannedCompleteDate": {
                "S": "08-02-2021"
            }
        },
        {
            "ApplicantProcessingStepCompletedByName": {
                "S": "samaiduch"
            },
            "ApplicantProcessingStepTitle": {
                "S": "Send job offer note"
            },
            "CompositeAccessPatterns": {
                "S": "ApplicantProcessingStep#ApplicantProcessingStepTitle:Send job offer note#ApplicantProcessingStepStatus:DONE#ApplicantProcessingStepAddedByPeopleName:SamaiDUCH#ApplicantProcessingStepCompletedByName:samaiduch"
            },
            "ApplicantProcessingStepResult": {
                "S": "Agree to processed?"
            },
            "ApplicantProcessingStepStatus": {
                "S": "DONE"
            },
            "ApplicantProcessingJobVacancyApplicantId": {
                "S": "JobVacancyApplicant:aea453883098e9bccf5ca022a819a2b9"
            },
            "EntityItemId": {
                "S": "ApplicantProcessingStep:d8334ab30ad99fbabfa0d18fb3b864ee"
            },
            "ApplicantProcessingStepActualCompleteDate": {
                "S": "2021-02-22"
            },
            "ApplicantProcessingStepNote": {
                "S": "testing"
            },
            "ApplicantProcessingStepId": {
                "S": "Step:ac3d4ee48c4c5e272d74ebd762ceaa41"
            },
            "ApplicantProcessingStepAddedByPeopleName": {
                "S": "SamaiDUCH"
            },
            "TenantId": {
                "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
            },
            "ApplicantProcessingStepAddedByPeopleId": {
                "S": "People:e303c774cd6daafffR492950011bf7e6b50f"
            },
            "ApplicantProcessingStepCompletedById": {
                "S": "user:1ab83367a398b6c66d04924d348abc06"
            },
            "ApplicantProcessingStepPlannedCompleteDate": {
                "S": "08-02-2021"
            }
        },
        {
            "ApplicantProcessingStepCompletedByName": {
                "S": "samaiduch"
            },
            "ApplicantProcessingStepTitle": {
                "S": "Arrange accessment/interview/shortisting(ODI/Client)"
            },
            "CompositeAccessPatterns": {
                "S": "ApplicantProcessingStep#ApplicantProcessingStepTitle:Arrange accessment/interview/shortisting(ODI/Client)#ApplicantProcessingStepStatus:DONE#ApplicantProcessingStepAddedByPeopleName:SamaiDUCH#ApplicantProcessingStepCompletedByName:samaiduch"
            },
            "ApplicantProcessingStepResult": {
                "S": "Agree to processed?"
            },
            "ApplicantProcessingStepStatus": {
                "S": "DONE"
            },
            "ApplicantProcessingJobVacancyApplicantId": {
                "S": "JobVacancyApplicant:aea453883098e9bccf5ca022a819a2b9"
            },
            "EntityItemId": {
                "S": "ApplicantProcessingStep:d96fdda7ebf469104ff5d080de2d5e58"
            },
            "ApplicantProcessingStepActualCompleteDate": {
                "S": "2021-02-25"
            },
            "ApplicantProcessingStepNote": {
                "S": "kkkkkkkkkk"
            },
            "ApplicantProcessingStepId": {
                "S": "Step:ac3d4ee48c4c5e272d74ebd762ceaa41"
            },
            "ApplicantProcessingStepAddedByPeopleName": {
                "S": "SamaiDUCH"
            },
            "TenantId": {
                "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
            },
            "ApplicantProcessingStepAddedByPeopleId": {
                "S": "People:e303c774cd6daafffR492950011bf7e6b50f"
            },
            "ApplicantProcessingStepCompletedById": {
                "S": "user:1ab83367a398b6c66d04924d348abc06"
            },
            "ApplicantProcessingStepPlannedCompleteDate": {
                "S": "08-02-2021"
            }
        },
        {
            "ApplicantProcessingStepCompletedByName": {
                "S": "samaiduch"
            },
            "ApplicantProcessingStepTitle": {
                "S": "Screen candidate profile"
            },
            "CompositeAccessPatterns": {
                "S": "ApplicantProcessingStep#ApplicantProcessingStepTitle:Screen candidate profile#ApplicantProcessingStepStatus:DONE#ApplicantProcessingStepAddedByPeopleName:SamaiDUCH#ApplicantProcessingStepCompletedByName:samaiduch"
            },
            "ApplicantProcessingStepResult": {
                "S": "Shortlisted?"
            },
            "ApplicantProcessingStepStatus": {
                "S": "DONE"
            },
            "ApplicantProcessingJobVacancyApplicantId": {
                "S": "JobVacancyApplicant:aea453883098e9bccf5ca022a819a2b9"
            },
            "EntityItemId": {
                "S": "ApplicantProcessingStep:df4cd5c6a8a3b9302dfafea7f425e75e"
            },
            "ApplicantProcessingStepActualCompleteDate": {
                "S": "18-02-2021"
            },
            "ApplicantProcessingStepNote": {
                "S": "testing"
            },
            "ApplicantProcessingStepId": {
                "S": "Step:83257e73ea5ca99e19ff75992c24c634"
            },
            "ApplicantProcessingStepAddedByPeopleName": {
                "S": "SamaiDUCH"
            },
            "TenantId": {
                "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
            },
            "ApplicantProcessingStepAddedByPeopleId": {
                "S": "People:e303c774cd6daafffR492950011bf7e6b50f"
            },
            "ApplicantProcessingStepCompletedById": {
                "S": "user:1ab83367a398b6c66d04924d348abc06"
            },
            "ApplicantProcessingStepPlannedCompleteDate": {
                "S": "08-02-2021"
            }
        },
        {
            "ApplicantProcessingStepCompletedByName": {
                "S": "samaiduch"
            },
            "ApplicantProcessingStepTitle": {
                "S": "Conduct interview"
            },
            "CompositeAccessPatterns": {
                "S": "ApplicantProcessingStep#ApplicantProcessingStepTitle:Conduct interview#ApplicantProcessingStepStatus:DONE#ApplicantProcessingStepAddedByPeopleName:SamaiDUCH#ApplicantProcessingStepCompletedByName:samaiduch"
            },
            "ApplicantProcessingStepResult": {
                "S": "Accept offer?"
            },
            "ApplicantProcessingStepStatus": {
                "S": "DONE"
            },
            "ApplicantProcessingJobVacancyApplicantId": {
                "S": "JobVacancyApplicant:aea453883098e9bccf5ca022a819a2b9"
            },
            "EntityItemId": {
                "S": "ApplicantProcessingStep:f6be517e14606f845e24b0fac85e8937"
            },
            "ApplicantProcessingStepActualCompleteDate": {
                "S": "2021-02-23"
            },
            "ApplicantProcessingStepNote": {
                "S": "testing"
            },
            "ApplicantProcessingStepId": {
                "S": "Step:ac3d4ee48c4c5e272d74ebd762ceaa41"
            },
            "ApplicantProcessingStepAddedByPeopleName": {
                "S": "SamaiDUCH"
            },
            "TenantId": {
                "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
            },
            "ApplicantProcessingStepAddedByPeopleId": {
                "S": "People:e303c774cd6daafffR492950011bf7e6b50f"
            },
            "ApplicantProcessingStepCompletedById": {
                "S": "user:1ab83367a398b6c66d04924d348abc06"
            },
            "ApplicantProcessingStepPlannedCompleteDate": {
                "S": "08-02-2021"
            }
        },
        {
            "ApplicantProcessingStepCompletedByName": {
                "S": "samaiduch"
            },
            "ApplicantProcessingStepTitle": {
                "S": "Arrange accessment/interview/shortisting(ODI/Client)"
            },
            "CompositeAccessPatterns": {
                "S": "ApplicantProcessingStep#ApplicantProcessingStepTitle:Arrange accessment/interview/shortisting(ODI/Client)#ApplicantProcessingStepStatus:DONE#ApplicantProcessingStepAddedByPeopleName:SamaiDUCH#ApplicantProcessingStepCompletedByName:samaiduch"
            },
            "ApplicantProcessingStepResult": {
                "S": "Shortlisted?"
            },
            "ApplicantProcessingStepStatus": {
                "S": "DONE"
            },
            "ApplicantProcessingJobVacancyApplicantId": {
                "S": "JobVacancyApplicant:aea453883098e9bccf5ca022a819a2b9"
            },
            "EntityItemId": {
                "S": "ApplicantProcessingStep:fca9cb2cd3adf765204d6db134a3e117"
            },
            "ApplicantProcessingStepActualCompleteDate": {
                "S": "2021-02-25"
            },
            "ApplicantProcessingStepNote": {
                "S": "tttttttttttttttttttttttttttttttttttttttttttttttt"
            },
            "ApplicantProcessingStepId": {
                "S": "Step:ac3d4ee48c4c5e272d74ebd762ceaa41"
            },
            "ApplicantProcessingStepAddedByPeopleName": {
                "S": "SamaiDUCH"
            },
            "TenantId": {
                "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
            },
            "ApplicantProcessingStepAddedByPeopleId": {
                "S": "People:e303c774cd6daafffR492950011bf7e6b50f"
            },
            "ApplicantProcessingStepCompletedById": {
                "S": "user:1ab83367a398b6c66d04924d348abc06"
            },
            "ApplicantProcessingStepPlannedCompleteDate": {
                "S": "08-02-2021"
            }
        }
    ]
}

```

This endpoint view detail a specific JobVacancyApplicant.

<aside class="warning">If you're not using an administrator API key, note that some JobVacancyApplicant will return 403 Forbidden if they are hidden for admins only.</aside>

### HTTP Request

`GET https://dev.aimlapps.com/recruitment-svc/api/v1/job-vacancies/JobVacancy:412af8742b5a465db54cd5648b80bd72/applicants/JobVacancyApplicant:1fb61bd50be4434aa28a609f1d54e022`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the JobVacancy
ID | The ID of JobVacancyApplicant

## Retrive Job Vacancy Applicant
```bash
curl "https://dev.aimlapps.com/recruitment-svc/api/v1/job-vacancies/JobVacancy:412af8742b5a465db54cd5648b80bd72/applicants"
  -H "Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw"
```

> The above command when submit JSON structured like this:

```json
{
    "JobVacancyApplicant": [
        {
            "JobVacancyApplicantProcessResult": {
                "S": "Pass"
            },
            "EntityItemId": {
                "S": "JobVacancyApplicant:396b0e3887a8e24d7a0f4d89854aee8c"
            },
            "JobVacancyApplicantPeopleSex": {
                "S": "Male"
            },
            "CompositeAccessPatterns": {
                "S": "JobVacancyApplicant#JobVacancyApplicantPeopleName:SoTheara#JobVacancyApplicantCurrentStepTitle:ApplyJob#JobVacancyApplicantProcessResult:Pass"
            },
            "JobVacancyApplicantPeopleId": {
                "S": "People:1e9cf083a2c3b07f0078b1b82d7ed274"
            },
            "JobVacancyApplicantJobVacancyId": {
                "S": "JobVacancy:1e9cf083a2c3b07f0078b1b82d7ed274"
            },
            "JobVacancyApplicantPeopleName": {
                "S": "SoTheara"
            },
            "TenantId": {
                "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
            },
            "JobVacancyApplicantCurrentStepId": {
                "S": "Step:1e9cf083a2c3b07f0078b1b82d7ed274"
            },
            "JobVacancyApplicantCurrentStepTitle": {
                "S": "ApplyJob"
            }
        },
        {
            "JobVacancyApplicantProcessResult": {
                "S": "Pass"
            },
            "EntityItemId": {
                "S": "JobVacancyApplicant:41477c8763f7ad0fd8d5079b24d276d0"
            },
            "JobVacancyApplicantPeopleSex": {
                "S": "Female"
            },
            "CompositeAccessPatterns": {
                "S": "JobVacancyApplicant#JobVacancyApplicantPeopleName:SoTheara#JobVacancyApplicantCurrentStepTitle:ApplyJob#JobVacancyApplicantProcessResult:Pass"
            },
            "JobVacancyApplicantPeopleId": {
                "S": "People:1e9cf083a2c3b07f0078b1b82d7ed274"
            },
            "JobVacancyApplicantJobVacancyId": {
                "S": "JobVacancy:1e9cf083a2c3b07f0078b1b82d7ed274"
            },
            "JobVacancyApplicantPeopleName": {
                "S": "SoTheara"
            },
            "TenantId": {
                "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
            },
            "JobVacancyApplicantCurrentStepId": {
                "S": "Step:1e9cf083a2c3b07f0078b1b82d7ed274"
            },
            "JobVacancyApplicantCurrentStepTitle": {
                "S": "ApplyJob"
            }
        },
        {
            "JobVacancyApplicantProcessResult": {
                "S": "PROCESSING"
            },
            "EntityItemId": {
                "S": "JobVacancyApplicant:453c51ef252985f7b4eb942c63129a0f"
            },
             "JobVacancyApplicantPeopleSex": {
            "S": "F"
            },
            "CompositeAccessPatterns": {
                "S": "JobVacancyApplicant#JobVacancyApplicantPeopleName:Dyna#JobVacancyApplicantCurrentStepTitle:Apply Job#JobVacancyApplicantProcessResult:PROCESSING"
            },
            "JobVacancyApplicantPeopleId": {
                "S": "People:1e9cf083a2c3b07f0078b1b82d7ed274"
            },
            "JobVacancyApplicantJobVacancyId": {
                "S": "People:1e9cf083a2c3b07f0078b1b82d7ed274"
            },
            "JobVacancyApplicantPeopleName": {
                "S": "Dyna"
            },
            "TenantId": {
                "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
            },
            "JobVacancyApplicantCurrentStepId": {
                "S": "Step:1e9cf083a2c3b07f0078b1b82d7ed274"
            },
            "JobVacancyApplicantCurrentStepTitle": {
                "S": "Apply Job"
            }
        },
        {
            "JobVacancyApplicantProcessResult": {
                "S": "PROCESSING"
            },
            "EntityItemId": {
                "S": "JobVacancyApplicant:bf8a7e80f6978e9a2d2ee54b9c6494d8"
            },
            "JobVacancyApplicantPeopleSex": {
                "S": "F"
            },
            "CompositeAccessPatterns": {
                "S": "JobVacancyApplicant#JobVacancyApplicantPeopleName:Dyna#JobVacancyApplicantCurrentStepTitle:Apply Job#JobVacancyApplicantProcessResult:PROCESSING"
            },
            "JobVacancyApplicantPeopleId": {
                "S": "People:1e9cf083a2c3b07f0078b1b82d7ed274"
            },
            "JobVacancyApplicantJobVacancyId": {
                "S": "People:1e9cf083a2c3b07f0078b1b82d7ed274"
            },
            "JobVacancyApplicantPeopleName": {
                "S": "Dyna"
            },
            "TenantId": {
                "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
            },
            "JobVacancyApplicantCurrentStepId": {
                "S": "Step:1e9cf083a2c3b07f0078b1b82d7ed274"
            },
            "JobVacancyApplicantCurrentStepTitle": {
                "S": "Apply Job"
            }
        }
    ],
    "FilterAttributes": [
        {
            "JobVacancyApplicantPeopleName": "People Name"
        },
        {
            "JobVacancyApplicantCurrentStepTitle": "Current Step Title"
        },
        {
            "JobVacancyApplicantProcessResult": "Process Result"
        }
    ]
}
```

This endpoint retrive JobVacancyApplicant.

<aside class="warning">If you're not using an administrator API key, note that some JobVacancyApplicant will return 403 Forbidden if they are hidden for admins only.</aside>

### HTTP Request

`GET https://dev.aimlapps.com/recruitment-svc/api/v1/job-vacancies/JobVacancy:412af8742b5a465db54cd5648b80bd72/applicants`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of JobVacancy

## Delete Job Vacancy Applicant
```bash
curl "https://dev.aimlapps.com/recruitment-svc/api/v1/job-vacancies/JobVacancy:412af8742b5a465db54cd5648b80bd72/applicants/JobVacancyApplicant:1fb61bd50be4434aa28a609f1d54e022"
  -H "Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw"
```


This endpoint Delete a specific JobVacancy Applicant.

<aside class="warning">If you're not using an administrator API key, note that some JobOrders will return 403 Forbidden if they are hidden for admins only.</aside>

### HTTP Request

`DELETE https://dev.aimlapps.com/recruitment-svc/api/v1/job-vacancies/JobVacancy:412af8742b5a465db54cd5648b80bd72/applicants/JobVacancyApplicant:1fb61bd50be4434aa28a609f1d54e022`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of JobVacancy
ID | The ID of JobVacancy Applicant


# Applicant Processing Step
## Create Applicant Processing Step

```bash
curl "https://dev.aimlapps.com/recruitment-svc/api/v1/applicants/JobVacancyApplicant:1ab83367a398b6c66d04924348abc06b/steps"
  -H "Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw"
```

> The above command when submit JSON structured like this:

```json

{
    "ApplicantProcessingStep":{
        "ApplicantProcessingJobVacancyApplicantId": "JobVacancyApplicant:1ab83367a398b6c66d04924348abc06b",
        "ApplicantProcessingStepId": "Step:1ab83367a398b6c66d04924348abc06b",
        "ApplicantProcessingStepStatus": "IN_PROGRESS",
        "ApplicantProcessingStepPlannedCompleteDate": "08-02-2021", 
        "ApplicantProcessingStepAddedByPeopleId": "People:1ab83367a398b6c66d04924348abc06b", 
        "ApplicantProcessingStepAddedByPeopleName": "Nary Doung",
        "ApplicantProcessingStepResult": "",
        "ApplicantProcessingStepActualCompleteDate": "",
        "ApplicantProcessingStepCompletedById": "",
        "ApplicantProcessingStepCompletedByName": "",
        "CompositeAccessPatterns": "",
        "ApplicantProcessingStepNote": "testing",

    }
}
```

This endpoint create a Applicant Processing Step.

<aside class="warning">If you're not using an administrator API key, note that some Applicant Processing Step will return 403 Forbidden if they are hidden for admins only.</aside>

### HTTP Request

`POST https://dev.aimlapps.com/recruitment-svc/api/v1/applicants/JobVacancyApplicant:1ab83367a398b6c66d04924348abc06b/steps`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of Applicant

## Get Applicant Processing Step
```bash
curl "https://dev.aimlapps.com/recruitment-svc/api/v1/applicants/JobVacancyApplicant:1ab83367a398b6c66d04924348abc06b/steps"
  -H "Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw"
```


> The above command returns JSON structured like this:

```json
{
    "ApplicantProcessingStep": [
        {
            "ApplicantProcessingStepCompletedByName": {
                "S": ""
            },
            "ApplicantProcessingStepResult": {
                "S": ""
            },
            "CompositeAccessPatterns": {
                "S": "ApplicantProcessingStep#ApplicantProcessingStepStatus:IN_PROGRESS#ApplicantProcessingStepAddedByPeopleName:Nary Doung#ApplicantProcessingStepCompletedByName:Mony Chan"
            },
            "ApplicantProcessingStepStatus": {
                "S": "IN_PROGRESS"
            },
            "ApplicantProcessingJobVacancyApplicantId": {
                "S": "JobVacancyApplicant:1ab83367a398b6c66d04924348abc06b"
            },
            "EntityItemId": {
                "S": "ApplicantProcessingStep:3fa403b1977f72dc73fdc65e62b79ebe"
            },
            "ApplicantProcessingStepActualCompleteDate": {
                "S": ""
            },
            "ApplicantProcessingStepId": {
                "S": "Step:1ab83367a398b6c66d04924348abc06b"
            },
            "ApplicantProcessingStepAddedByPeopleName": {
                "S": "Nary Doung"
            },
            "ApplicantProcessingStepCompletedById": {
                "S": ""
            },
            "ApplicantProcessingStepAddedByPeopleId": {
                "S": "People:1ab83367a398b6c66d04924348abc06b"
            },
            "ApplicantProcessingStepPlannedCompleteDate": {
                "S": "08-02-2021"
            },
            "ApplicantProcessingStepNote": "testing",
        },
        {
            "ApplicantProcessingStepCompletedByName": {
                "S": "Mony Chan"
            },
            "ApplicantProcessingStepResult": {
                "S": "SHORTLISTED"
            },
            "ApplicantProcessingStepTitle": {
                "S": "ScreenCandidate"
            },
            "CompositeAccessPatterns": {
                "S": "ApplicantProcessingStep#ApplicantProcessingStepTitle:ScreenCandidate#ApplicantProcessingStepStatus:IN_PROGRESS#ApplicantProcessingStepAddedByPeopleName:Sopha NyTa#ApplicantProcessingStepCompletedByName:Mony Chan"
            },
            "ApplicantProcessingStepStatus": {
                "S": "IN_PROGRESS"
            },
            "ApplicantProcessingJobVacancyApplicantId": {
                "S": "JobVacancyApplicant:1ab83367a398b6c66d04924348abc06b"
            },
            "EntityItemId": {
                "S": "ApplicantProcessingStep:4cb185d04887d0e206e3c2e9b1e552d8"
            },
            "ApplicantProcessingStepActualCompleteDate": {
                "S": "08-02-2021"
            },
            "ApplicantProcessingStepId": {
                "S": "Step:1ab83367a398b6c66d04924348abc06b"
            },
            "ApplicantProcessingStepAddedByPeopleName": {
                "S": "Sopha NyTa"
            },
            "TenantId": {
                "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
            },
            "ApplicantProcessingStepAddedByPeopleId": {
                "S": "People:1ab83367a398b6c66d04924348abc06b"
            },
            "ApplicantProcessingStepCompletedById": {
                "S": "CompletedBy:1ab83367a398b6c66d04924348abc06b"
            },
            "ApplicantProcessingStepPlannedCompleteDate": {
                "S": "08-02-2021"
            },
            "ApplicantProcessingStepNote": "testing",
        },
        {
            "ApplicantProcessingStepCompletedByName": {
                "S": "Mony Chan"
            },
            "ApplicantProcessingStepResult": {
                "S": "SHORTLISTED"
            },
            "ApplicantProcessingStepTitle": {
                "S": "ScreenCandidate"
            },
            "CompositeAccessPatterns": {
                "S": "ApplicantProcessingStep#ApplicantProcessingStepTitle:ScreenCandidate#ApplicantProcessingStepStatus:IN_PROGRESS#ApplicantProcessingStepAddedByPeopleName:Sopha Ny#ApplicantProcessingStepCompletedByName:Mony Chan"
            },
            "ApplicantProcessingStepStatus": {
                "S": "IN_PROGRESS"
            },
            "ApplicantProcessingJobVacancyApplicantId": {
                "S": "JobVacancyApplicant:1ab83367a398b6c66d04924348abc06b"
            },
            "EntityItemId": {
                "S": "ApplicantProcessingStep:a1945d018b57da121d47d602ade6a6d4"
            },
            "ApplicantProcessingStepActualCompleteDate": {
                "S": "08-02-2021"
            },
            "ApplicantProcessingStepId": {
                "S": "Step:1ab83367a398b6c66d04924348abc06b"
            },
            "TenantId": {
                "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
            },
            "ApplicantProcessingStepAddedByPeopleName": {
                "S": "Sopha Ny"
            },
            "ApplicantProcessingStepCompletedById": {
                "S": "CompletedBy:1ab83367a398b6c66d04924348abc06b"
            },
            "ApplicantProcessingStepAddedByPeopleId": {
                "S": "People:1ab83367a398b6c66d04924348abc06b"
            },
            "ApplicantProcessingStepPlannedCompleteDate": {
                "S": "08-02-2021"
            },
            "ApplicantProcessingStepNote": "testing",
        }
    ],
    "FilterAttributes": [
        {
            "ApplicantProcessingStepTitle": "Selection Step"
        },
        {
            "ApplicantProcessingStepStatus": "Step Status"
        },
        {
            "ApplicantProcessingStepAddedByPeopleName": "Added by"
        },
        {
            "ApplicantProcessingStepCompletedByName": "Completed by"
        }
    ]
}

```

This endpoint retrieves all Applicant Processing Step.

### HTTP Request

`GET https://dev.aimlapps.com/recruitment-svc/api/v1/applicants/JobVacancyApplicant:1ab83367a398b6c66d04924348abc06b/steps`

<aside class="success">
Remember — a happy Applicant Processing Step is an authenticated Recruitment!
</aside>

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of Applicant

## Delete Applicant Processing Step
```bash
curl "http://127.0.0.1:8000/recruitment-svc/api/v1/applicants/JobVacancyApplicant:1ab83367a398b6c66d04924348abc06b/steps/ApplicantProcessingStep:3fa403b1977f72dc73fdc65e62b79ebe"
  -H "Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw"
```


This endpoint Delete a specific Applicant Processing Step.

<aside class="warning">If you're not using an administrator API key, note that some JobOrders will return 403 Forbidden if they are hidden for admins only.</aside>

### HTTP Request

`DELETE http://127.0.0.1:8000/recruitment-svc/api/v1/applicants/JobVacancyApplicant:1ab83367a398b6c66d04924348abc06b/steps/ApplicantProcessingStep:3fa403b1977f72dc73fdc65e62b79ebe`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of Applicant
ID | The ID of Processing Step

## View Detail Applicant Processing Step
```bash
curl "http://127.0.0.1:8000/recruitment-svc/api/v1/applicants/JobVacancyApplicant:1ab83367a398b6c66d04924348abc06b/steps/ApplicantProcessingStep:3fa403b1977f72dc73fdc65e62b79ebe"
  -H "Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw"
```

> The above command when submit JSON structured like this:

```json
[
    {
        "ApplicantProcessingStepCompletedByName": {
            "S": "Mony Chan"
        },
        "ApplicantProcessingStepResult": {
            "S": "SHORTLISTED"
        },
        "CompositeAccessPatterns": {
            "S": "ApplicantProcessingStep#ApplicantProcessingStepStatus:IN_PROGRESS#ApplicantProcessingStepAddedByPeopleName:Nary Doung#ApplicantProcessingStepCompletedByName:Mony Chan"
        },
        "ApplicantProcessingStepStatus": {
            "S": "IN_PROGRESS"
        },
        "ApplicantProcessingJobVacancyApplicantId": {
            "S": "JobVacancyApplicant:1ab83367a398b6c66d04924348abc06b"
        },
        "EntityItemId": {
            "S": "ApplicantProcessingStep:3fa403b1977f72dc73fdc65e62b79ebe"
        },
        "ApplicantProcessingStepActualCompleteDate": {
            "S": "08-02-2021"
        },
        "ApplicantProcessingStepId": {
            "S": "Step:1ab83367a398b6c66d04924348abc06b"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "ApplicantProcessingStepAddedByPeopleName": {
            "S": "Nary Doung"
        },
        "ApplicantProcessingStepCompletedById": {
            "S": "CompletedBy:1ab83367a398b6c66d04924348abc06b"
        },
        "ApplicantProcessingStepAddedByPeopleId": {
            "S": "People:1ab83367a398b6c66d04924348abc06b"
        },
        "ApplicantProcessingStepPlannedCompleteDate": {
            "S": "08-02-2021"
        },
        "ApplicantProcessingStepNote": "testing",
    }
]
```

This endpoint view detail a specific Applicant Processing Step.

<aside class="warning">If you're not using an administrator API key, note that some Applicant Processing Step will return 403 Forbidden if they are hidden for admins only.</aside>

### HTTP Request

`GET http://127.0.0.1:8000/recruitment-svc/api/v1/applicants/JobVacancyApplicant:1ab83367a398b6c66d04924348abc06b/steps/ApplicantProcessingStep:3fa403b1977f72dc73fdc65e62b79ebe`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of Applicant
ID | The ID of Processing Step

## Update Applicant Processing Step
```bash
curl "http://127.0.0.1:8000/recruitment-svc/api/v1/applicants/JobVacancyApplicant:1ab83367a398b6c66d04924348abc06b/steps/ApplicantProcessingStep:3fa403b1977f72dc73fdc65e62b79ebe"
  -H "Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw"
```

> The above command when submit JSON structured like this:

```json
{
    "ApplicantProcessingStep":{
        "ApplicantProcessingJobVacancyApplicantId":"JobVacancyApplicant:8b254209482f8e12bddf093b4fa85222",
        "ApplicantProcessingStepTitle":"Ratha Testing",
        "ApplicantProcessingStepId": "Step:741a08e9bde2708b59fee705d09f4cd9",
        "ApplicantProcessingStepStatus": "DONE",
        "ApplicantProcessingStepPlannedCompleteDate": "08-02-2021", 
        "ApplicantProcessingStepAddedByPeopleId": "People:e303c774cd6daafffR49295t0011bf7e6b50f", 
        "ApplicantProcessingStepAddedByPeopleName": "SamaiDUCH",
        "ApplicantProcessingStepResult": "Shortlisted?",
        "ApplicantProcessingStepActualCompleteDate": "18-02-2021",
        "ApplicantProcessingStepCompletedById": "user:1ab83367a398b6c66d04924d348abc06",
        "ApplicantProcessingStepCompletedByName": "samaiduch",
        "CompositeAccessPatterns": "ApplicantProcessingStep#ApplicantProcessingStepTitle:ScreenCandidate#ApplicantProcessingStepStatus:IN_PROGRESS#ApplicantProcessingStepAddedByPeopleName:Sopha Ny#ApplicantProcessingStepCompletedByName:Mony Chan",
        "ApplicantProcessingOldStepNote": "Step Arrange accessment/interview/shortisting(ODI/Client)",
        "ApplicantProcessingNextStepNote": "Step Arrange accessment/interview/shortisting(ODI/Client)"
    }
}
```

This endpoint update a specific Applicant Processing Step

<aside class="warning">If you're not using an administrator API key, note that some Applicant Processing Step will return 403 FForbidden if they are hidden for admins only.</aside>

### HTTP Request

`PUT http://127.0.0.1:8000/recruitment-svc/api/v1/applicants/JobVacancyApplicant:1ab83367a398b6c66d04924348abc06b/steps/ApplicantProcessingStep:3fa403b1977f72dc73fdc65e62b79ebe`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of Applicant
ID | The ID of Processing Step


# Urgency Level
## Create Urgency Level

```bash
curl "https://dev.aimlapps.com/recruitment-svc/api/v1/urgency-levels"
  -H "Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw"
```

> The above command when submit JSON structured like this:

```json

{
    "UrgencyLevel":{
        "UrgencyLevel": "Urgent"
    }
}
```

This endpoint create a specific UrgencyLevel.

<aside class="warning">If you're not using an administrator API key, note that some UrgencyLevel will return 403 Forbidden if they are hidden for admins only.</aside>

### HTTP Request

`POST https://dev.aimlapps.com/recruitment-svc/api/v1/urgency-levels`

## Retrive Urgency Level
```bash
curl "https://dev.aimlapps.com/recruitment-svc/api/v1/urgency-levels"
  -H "Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw"
```

> The above command when submit JSON structured like this:

```json
{
    "UrgencyLevel": [
        {
            "EntityItemId": {
                "S": "UrgencyLevel:bf8a7e80f6978e9a2d2ee54b9c6494d8"
            },
            "UrgencyLevel": {
                "S": "Urgent"
            }
        },
        {
            "EntityItemId": {
                "S": "UrgencyLevel:bf8a7e80f6978e9a2d2ee54b9c6494d9"
            },
            "UrgencyLevel": {
                "S": "Urgent"
            }
        }
    ],
    "FilterAttributes": [
        {
            "UrgencyLevel": "Urgency Level"
        }
    ]
}
```

This endpoint retrive UrgencyLevels.

<aside class="warning">If you're not using an administrator API key, note that some UrgencyLevels will return 403 Forbidden if they are hidden for admins only.</aside>

### HTTP Request

`GET https://dev.aimlapps.com/recruitment-svc/api/v1/urgency-levels`

## Update Urgency Level
```bash
curl "https://dev.aimlapps.com/recruitment-svc/api/v1/urgency-levels/UrgencyLevel:bf8a7e80f6978e9a2d2ee54b9c6494d9"
  -H "Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw"
```

> The above command when submit JSON structured like this:

```json
{
    "UrgencyLevel":{
        "UrgencyLevel": "Urgent"
    }
}
```

This endpoint update a specific UrgencyLevel

<aside class="warning">If you're not using an administrator API key, note that some UrgencyLevel will return 403 Forbidden if they are hidden for admins only.</aside>

### HTTP Request

`PUT https://dev.aimlapps.com/recruitment-svc/api/v1/urgency-levels/UrgencyLevel:bf8a7e80f6978e9a2d2ee54b9c6494d9`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of UrgencyLevel

## View Detail Urgency Level
```bash
curl "https://dev.aimlapps.com/recruitment-svc/api/v1/urgency-levels/UrgencyLevel:bf8a7e80f6978e9a2d2ee54b9c6494d9"
  -H "Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw"
```

> The above command when submit JSON structured like this:

```json
[
   {
            "EntityItemId": {
                "S": "UrgencyLevel:bf8a7e80f6978e9a2d2ee54b9c6494d9"
            },
            "UrgencyLevel": {
                "S": "Urgent"
            }
        }
]
```

This endpoint view detail a specific UrgencyLevel.

<aside class="warning">If you're not using an administrator API key, note that some UrgencyLevel will return 403 Forbidden if they are hidden for admins only.</aside>

### HTTP Request

`get https://dev.aimlapps.com/recruitment-svc/api/v1/urgency-levels/UrgencyLevel:bf8a7e80f6978e9a2d2ee54b9c6494d9`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of UrgencyLevel

## Delete a Urgency Level

```bash
curl "https://dev.aimlapps.com/recruitment-svc/api/v1/urgency-levels/UrgencyLevel:bf8a7e80f6978e9a2d2ee54b9c6494d9"
  -H "Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw"
```

This endpoint delete a UrgencyLevel.

<aside class="warning">If you're not using an administrator API key, note that some UrgencyLevel will return 403 Forbidden if they are hidden for admins only.</aside>

### HTTP Request

`DELETE https://dev.aimlapps.com/recruitment-svc/api/v1/urgency-levels/UrgencyLevel:bf8a7e80f6978e9a2d2ee54b9c6494d9`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of UrgencyLevel

# Fee Rate
## Create Fee Rate

```bash
curl "https://dev.aimlapps.com/recruitment-svc/api/v1/fee-rates"
  -H "Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw"
```

> The above command when submit JSON structured like this:

```json

{
    "FeeRate":{
        "FeeRate": "5.5"
    }
}
```

This endpoint create a specific FeeRate.

<aside class="warning">If you're not using an administrator API key, note that some FeeRate will return 403 Forbidden if they are hidden for admins only.</aside>

### HTTP Request

`POST https://dev.aimlapps.com/recruitment-svc/api/v1/fee-rates`

## Retrive Fee Rate
```bash
curl "https://dev.aimlapps.com/recruitment-svc/api/v1/fee-rates"
  -H "Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw"
```

> The above command when submit JSON structured like this:

```json
{
    "FeeRate": [
        {
            "EntityItemId": {
                "S": "FeeRate:bf8a7e80f6978e9a2d2ee54b9c6494d8"
            },
            "FeeRate": {
                "S": "5.5"
            }
        },
        {
            "EntityItemId": {
                "S": "FeeRate:bf8a7e80f6978e9a2d2ee54b9c6494d9"
            },
            "FeeRate": {
                "S": "5.6"
            }
        }
    ],
    "FilterAttributes": [
        {
            "FeeRate": "Fee Rate"
        }
    ]
}
```

This endpoint retrive FeeRates.

<aside class="warning">If you're not using an administrator API key, note that some FeeRates will return 403 Forbidden if they are hidden for admins only.</aside>

### HTTP Request

`GET https://dev.aimlapps.com/recruitment-svc/api/v1/fee-rates`

## Update Fee Rate
```bash
curl "https://dev.aimlapps.com/recruitment-svc/api/v1/fee-rates/FeeRate:bf8a7e80f6978e9a2d2ee54b9c6494d9"
  -H "Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw"
```

> The above command when submit JSON structured like this:

```json
{
    "FeeRate":{
        "FeeRate": "6.6"
    }
}
```

This endpoint update a specific FeeRate

<aside class="warning">If you're not using an administrator API key, note that some FeeRate will return 403 Forbidden if they are hidden for admins only.</aside>

### HTTP Request

`PUT https://dev.aimlapps.com/recruitment-svc/api/v1/fee-rates/FeeRate:bf8a7e80f6978e9a2d2ee54b9c6494d9`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of FeeRate

## View Detail Fee Rate
```bash
curl "https://dev.aimlapps.com/recruitment-svc/api/v1/fee-rates/FeeRate:bf8a7e80f6978e9a2d2ee54b9c6494d9"
  -H "Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw"
```

> The above command when submit JSON structured like this:

```json
[
   {
            "EntityItemId": {
                "S": "FeeRate:bf8a7e80f6978e9a2d2ee54b9c6494d9"
            },
            "FeeRate": {
                "S": "5.7"
            }
        }
]
```

This endpoint view detail a specific FeeRate.

<aside class="warning">If you're not using an administrator API key, note that some FeeRate will return 403 Forbidden if they are hidden for admins only.</aside>

### HTTP Request

`get https://dev.aimlapps.com/recruitment-svc/api/v1/fee-rates/FeeRate:bf8a7e80f6978e9a2d2ee54b9c6494d9`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of FeeRate

## Delete a Fee Rate

```bash
curl "https://dev.aimlapps.com/recruitment-svc/api/v1/fee-rates/FeeRate:bf8a7e80f6978e9a2d2ee54b9c6494d9"
  -H "Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw"
```

This endpoint delete a FeeRate.

<aside class="warning">If you're not using an administrator API key, note that some FeeRate will return 403 Forbidden if they are hidden for admins only.</aside>

### HTTP Request

`DELETE https://dev.aimlapps.com/recruitment-svc/api/v1/fee-rates/FeeRate:bf8a7e80f6978e9a2d2ee54b9c6494d9`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of FeeRate
# Job Channel
## Create Job Channel

```bash
curl "https://dev.aimlapps.com/recruitment-svc/api/v1/job-channels"
  -H "Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw"
```

> The above command when submit JSON structured like this:

```json

{
    "JobChannel":{
        "JobChannelName": "HR",
        "JobChannelWebsite": "www.HR.com",
        "JobChannelAddress": "Phnom Phenh",
        "JobChannelEmail": "HR@gmail.com",
        "JobChannelPhoneNumber": "0987654321",
        "JobChannelNote": "Recruitment Office",
        "CompositeAccessPatterns": "JobChannel#JobChannelName:ODI"

    }
}
```

This endpoint create a specific JobChannel.

<aside class="warning">If you're not using an administrator API key, note that some JobChannel will return 403 Forbidden if they are hidden for admins only.</aside>

### HTTP Request

`POST https://dev.aimlapps.com/recruitment-svc/api/v1/job-channels`

## Retrive Job Channel
```bash
curl "https://dev.aimlapps.com/recruitment-svc/api/v1/job-channels"
  -H "Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw"
```

> The above command when submit JSON structured like this:

```json
{
    "JobChannel": [
        {
            "JobChannelEmail": {
                "S": "HR@gmail.com"
            },
            "JobChannelWebsite": {
                "S": "www.HR.com"
            },
            "EntityItemId": {
                "S": "JobChannel:2b03fb005f0d75e46924c1448b3e033c"
            },
            "CompositeAccessPatterns": {
                "S": "JobChannel#JobChannelName:HR"
            },
            "JobChannelName": {
                "S": "HR"
            },
            "TenantId": {
                "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
            },
            "JobChannelPhoneNumber": {
                "S": "0987654321"
            },
            "JobChannelNote": {
                "S": "Recruitment Office"
            },
            "JobChannelAddress": {
                "S": "Phnom Phenh"
            }
        },
        {
            "JobChannelEmail": {
                "S": "odi@gmail.com"
            },
            "JobChannelWebsite": {
                "S": "www.ODI.com"
            },
            "EntityItemId": {
                "S": "JobChannel:6ee8925d50c058dbf55fb568afc71f54"
            },
            "CompositeAccessPatterns": {
                "S": "JobChannel#JobChannelName:ODI"
            },
            "JobChannelName": {
                "S": "ODI"
            },
            "TenantId": {
                "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
            },
            "JobChannelPhoneNumber": {
                "S": "0987654321"
            },
            "JobChannelNote": {
                "S": "Recruitment Office"
            },
            "JobChannelAddress": {
                "S": "Phnom Phenh"
            }
        }
    ],
    "FilterAttributes": [
        {
            "JobChannelName": "JobChannel Name"
        }
    ]
}
```

This endpoint retrive JobChannels.

<aside class="warning">If you're not using an administrator API key, note that some JobChannels will return 403 Forbidden if they are hidden for admins only.</aside>

### HTTP Request

`GET https://dev.aimlapps.com/recruitment-svc/api/v1/job-channels`

## Update Job Channel
```bash
curl "https://dev.aimlapps.com/recruitment-svc/api/v1/job-channels/JobChannel:bf8a7e80f6978e9a2d2ee54b9c6494d9"
  -H "Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw"
```

> The above command when submit JSON structured like this:

```json
{
    "JobChannel":{
        "JobChannelName": "ODI",
        "JobChannelWebsite": "www.ODI.com",
        "JobChannelAddress": "Phnom Phenh",
        "JobChannelEmail": "odi@gmail.com",
        "JobChannelPhoneNumber": "0987654321",
        "JobChannelNote": "Recruitment Office"
    }
}
```

This endpoint update a specific JobChannel

<aside class="warning">If you're not using an administrator API key, note that some JobChannel will return 403 Forbidden if they are hidden for admins only.</aside>

### HTTP Request

`PUT https://dev.aimlapps.com/recruitment-svc/api/v1/job-channels/JobChannel:bf8a7e80f6978e9a2d2ee54b9c6494d9`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of JobChannel

## View Detail Job Channal
```bash
curl "https://dev.aimlapps.com/recruitment-svc/api/v1/job-channels/JobChannel:bf8a7e80f6978e9a2d2ee54b9c6494d9"
  -H "Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw"
```

> The above command when submit JSON structured like this:

```json
[
    {
        "EntityItemId": {
            "S": "JobChannel:bf8a7e80f6978e9a2d2ee54b9c6494d8"
        },
        "JobChannelName": {
            "S": "ODI"
        },
        "JobChannelWebsite": {
            "S": "www.ODI.com"
        },
        "JobChannelAddress": {
            "S": "Phnom Phenh"
        },
        "JobChannelPhoneNumber": {
            "S": "0987654321"
        },
        "JobChannelNote": {
            "S": "Recruitment Office"
        }
    }
]
```

This endpoint view detail a specific JobChannel.

<aside class="warning">If you're not using an administrator API key, note that some JobChannel will return 403 Forbidden if they are hidden for admins only.</aside>

### HTTP Request

`get https://dev.aimlapps.com/recruitment-svc/api/v1/job-channels/JobChannel:bf8a7e80f6978e9a2d2ee54b9c6494d9`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of JobChannel

## Delete a Job Channel

```bash
curl "https://dev.aimlapps.com/recruitment-svc/api/v1/job-channels/JobChannel:bf8a7e80f6978e9a2d2ee54b9c6494d9"
  -H "Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw"
```

This endpoint delete a JobChannel.

<aside class="warning">If you're not using an administrator API key, note that some JobChannel will return 403 Forbidden if they are hidden for admins only.</aside>

### HTTP Request

`DELETE https://dev.aimlapps.com/recruitment-svc/api/v1/job-channels/JobChannel:bf8a7e80f6978e9a2d2ee54b9c6494d9`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of JobChannel

# Decision Option
## Create Decision Option

```bash
curl "https://dev.aimlapps.com/recruitment-svc/api/v1/decision-options"
  -H "Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw"
```

> The above command when submit JSON structured like this:

```json

{
    "DecisionOption":{
        "DecisionOption": "PASS"
    }
}
```

This endpoint create a specific DecisionOption.

<aside class="warning">If you're not using an administrator API key, note that some DecisionOption will return 403 Forbidden if they are hidden for admins only.</aside>

### HTTP Request

`POST https://dev.aimlapps.com/recruitment-svc/api/v1/decision-options`

## Retrive Decision Option
```bash
curl "https://dev.aimlapps.com/recruitment-svc/api/v1/decision-options"
  -H "Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw"
```

> The above command when submit JSON structured like this:

```json
{
    "DecisionOption": [
        {
            "EntityItemId": {
                "S": "DecisionOption:bf8a7e80f6978e9a2d2ee54b9c6494d8"
            },
            "DecisionOption": {
                "S": "PASS"
            }
        },
        {
            "EntityItemId": {
                "S": "DecisionOption:bf8a7e80f6978e9a2d2ee54b9c6494d9"
            },
            "DecisionOption": {
                "S": "PASS"
            }
        }
    ],
    "FilterAttributes": [
        {
            "DecisionOption": "Decision"
        }
    ]
}
```

This endpoint retrive DecisionOptions.

<aside class="warning">If you're not using an administrator API key, note that some DecisionOptions will return 403 Forbidden if they are hidden for admins only.</aside>

### HTTP Request

`GET https://dev.aimlapps.com/recruitment-svc/api/v1/decision-options`

## Update Decision Option
```bash
curl "https://dev.aimlapps.com/recruitment-svc/api/v1/decision-options/DecisionOption:bf8a7e80f6978e9a2d2ee54b9c6494d9"
  -H "Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw"
```

> The above command when submit JSON structured like this:

```json
{
    "DecisionOption":{
        "DecisionOption": "PASS"
    }
}
```

This endpoint update a specific DecisionOption

<aside class="warning">If you're not using an administrator API key, note that some DecisionOption will return 403 Forbidden if they are hidden for admins only.</aside>

### HTTP Request

`PUT https://dev.aimlapps.com/recruitment-svc/api/v1/decision-options/DecisionOption:bf8a7e80f6978e9a2d2ee54b9c6494d9`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of DecisionOption

## View Detail Decision Option
```bash
curl "https://dev.aimlapps.com/recruitment-svc/api/v1/decision-options/DecisionOption:bf8a7e80f6978e9a2d2ee54b9c6494d9"
  -H "Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw"
```

> The above command when submit JSON structured like this:

```json
[
   {
            "EntityItemId": {
                "S": "DecisionOption:bf8a7e80f6978e9a2d2ee54b9c6494d9"
            },
            "DecisionOption": {
                "S": "PASS"
            }
        }
]
```

This endpoint view detail a specific DecisionOption.

<aside class="warning">If you're not using an administrator API key, note that some DecisionOption will return 403 Forbidden if they are hidden for admins only.</aside>

### HTTP Request

`get https://dev.aimlapps.com/recruitment-svc/api/v1/decision-options/DecisionOption:bf8a7e80f6978e9a2d2ee54b9c6494d9`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of DecisionOption

## Delete a Decision Option

```bash
curl "https://dev.aimlapps.com/recruitment-svc/api/v1/decision-options/DecisionOption:bf8a7e80f6978e9a2d2ee54b9c6494d9"
  -H "Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw"
```

This endpoint delete a DecisionOption.

<aside class="warning">If you're not using an administrator API key, note that some DecisionOption will return 403 Forbidden if they are hidden for admins only.</aside>

### HTTP Request

`DELETE https://dev.aimlapps.com/recruitment-svc/api/v1/decision-options/DecisionOption:bf8a7e80f6978e9a2d2ee54b9c6494d9`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of DecisionOption

# Step
## Create Step

```bash
curl "https://dev.aimlapps.com/recruitment-svc/api/v1/selection-processes/SelectionProcess:bf8a7e80f6978e9a2d2ee54b9c6494d9/steps"
  -H "Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw"
```

> The above command when submit JSON structured like this:

```json

{
    "Step":{
        "StepSelectionProcessId": "Step:bf8a7e80f6978e9a2d2ee54b9c6494d9",
        "StepTitle": "Screen Candidate",
        "StepCouldStart": "YES",
        "StepNeedDecision": "YES",
        "StepOfferJob": "NO",
        "StepLinkSystemResource": "Screen Candidate",
        "StepLinkPurpose": "Screen Candidate",

    }
}
```

This endpoint create a specific Step.

<aside class="warning">If you're not using an administrator API key, note that some Step will return 403 Forbidden if they are hidden for admins only.</aside>

### HTTP Request

`POST https://dev.aimlapps.com/recruitment-svc/api/v1/selection-processes/SelectionProcess:bf8a7e80f6978e9a2d2ee54b9c6494d9/steps`

## Retrive Step
```bash
curl "https://dev.aimlapps.com/recruitment-svc/api/v1/selection-processes/SelectionProcess:bf8a7e80f6978e9a2d2ee54b9c6494d9/steps"
  -H "Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw"
```

> The above command when submit JSON structured like this:

```json
{
    "Step": [
        {
            "EntityItemId": {
                "S": "Step:bf8a7e80f6978e9a2d2ee54b9c6494d9"
            },
            "StepSelectionProcessId": {
                "S": "SelectionProcess:bf8a7e80f6978e9a2d2ee54b9c6494d9"
            },
            "StepTitle": {
                "S": "Screen Candidate"
            },
            "StepCouldStart": {
                "S": "YES"
            },
            "StepNeedDecision": {
                "S": "YES"
            },
            "StepOfferJob": {
                "S": "NO"
            },
            "StepLinkSystemResource": {
                "S": "Screen Candidate"
            },
            "StepLinkPurpose": {
                "S": "Screen Candidate"
            }
        },
        {
             "EntityItemId": {
                "S": "Step:bf8a7e80f6978e9a2d2ee54b9c6494d8"
            },
            "StepSelectionProcessId": {
                "S": "SelectionProcess:bf8a7e80f6978e9a2d2ee54b9c6494d9"
            },
            "StepTitle": {
                "S": "Apply Job"
            },
            "StepCouldStart": {
                "S": "YES"
            },
            "StepNeedDecision": {
                "S": "YES"
            },
            "StepOfferJob": {
                "S": "NO"
            },
            "StepLinkSystemResource": {
                "S": "Apply Job"
            },
            "StepLinkPurpose": {
                "S": "Apply Job"
            }
        }
    ],
    "FilterAttributes": [
        {
            "Step": "Decision",
        }
    ]
}
```

This endpoint retrive Steps.

<aside class="warning">If you're not using an administrator API key, note that some Steps will return 403 Forbidden if they are hidden for admins only.</aside>

### HTTP Request

`GET https://dev.aimlapps.com/recruitment-svc/api/v1/selection-processes/SelectionProcess:bf8a7e80f6978e9a2d2ee54b9c6494d9/steps`

## Update Step
```bash
curl "https://dev.aimlapps.com/recruitment-svc/api/v1/selection-processes/SelectionProcess:bf8a7e80f6978e9a2d2ee54b9c6494d9/steps/Step:bf8a7e80f6978e9a2d2ee54b9c6494d8"
  -H "Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw"
```

> The above command when submit JSON structured like this:

```json
{
     "Step":{
        "StepSelectionProcessId": "Step:bf8a7e80f6978e9a2d2ee54b9c6494d9",
        "StepTitle": "Screen Candidate",
        "StepCouldStart": "YES",
        "StepNeedDecision": "YES",
        "StepOfferJob": "NO",
        "StepLinkSystemResource": "Screen Candidate",
        "StepLinkPurpose": "Screen Candidate",

    }
}
```

This endpoint update a specific Step

<aside class="warning">If you're not using an administrator API key, note that some Step will return 403 Forbidden if they are hidden for admins only.</aside>

### HTTP Request

`PUT https://dev.aimlapps.com/recruitment-svc/api/v1/selection-processes/SelectionProcess:bf8a7e80f6978e9a2d2ee54b9c6494d9/steps/Step:bf8a7e80f6978e9a2d2ee54b9c6494d8`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of Step

## View Detail Step
```bash
curl "https://dev.aimlapps.com/recruitment-svc/api/v1/selection-processes/SelectionProcess:bf8a7e80f6978e9a2d2ee54b9c6494d9/steps/Step:bf8a7e80f6978e9a2d2ee54b9c6494d9"
  -H "Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw"
```

> The above command when submit JSON structured like this:

```json
[
{        "EntityItemId": {
            "S": "Step:bf8a7e80f6978e9a2d2ee54b9c6494d9"
        },
        "StepSelectionProcessId": {
            "S": "SelectionProcess:bf8a7e80f6978e9a2d2ee54b9c6494d9"
        },
        "StepTitle": {
            "S": "Screen Candidate"
        },
        "StepCouldStart": {
            "S": "YES"
        },
        "StepNeedDecision": {
            "S": "YES"
        },
        "StepOfferJob": {
            "S": "NO"
        },
        "StepLinkSystemResource": {
            "S": "Screen Candidate"
        },
        "StepLinkPurpose": {
            "S": "Screen Candidate"
        }
    }
]
```

This endpoint view detail a specific Step.

<aside class="warning">If you're not using an administrator API key, note that some Step will return 403 Forbidden if they are hidden for admins only.</aside>

### HTTP Request

`get https://dev.aimlapps.com/recruitment-svc/api/v1/selection-processes/SelectionProcess:bf8a7e80f6978e9a2d2ee54b9c6494d9/steps/Step:bf8a7e80f6978e9a2d2ee54b9c6494d9`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of Step

## Delete a Step

```bash
curl "https://dev.aimlapps.com/recruitment-svc/api/v1/selection-processes/SelectionProcess:bf8a7e80f6978e9a2d2ee54b9c6494d9/steps/Step:bf8a7e80f6978e9a2d2ee54b9c6494d9"
  -H "Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw"
```

This endpoint delete a Step.

<aside class="warning">If you're not using an administrator API key, note that some Step will return 403 Forbidden if they are hidden for admins only.</aside>

### HTTP Request

`DELETE https://dev.aimlapps.com/recruitment-svc/api/v1/selection-processes/SelectionProcess:bf8a7e80f6978e9a2d2ee54b9c6494d9/steps/Step:bf8a7e80f6978e9a2d2ee54b9c6494d9`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of Step

# Step Flow Config
## Create Step Flow Config

```bash
curl "https://dev.aimlapps.com/recruitment-svc/api/v1/selectios-processes/SelectionProcess:bf8a7e80f6978e9a2d2ee54b9c6494d9/step-flow-configs"
  -H "Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw"
```

> The above command when submit JSON structured like this:

```json
{
    "StepFlowConfig":{
        "StepFlowConfigSelectionProcessId": "SelectionProcess:078ce8c7c1d75b663c602c08a8700c3f",
        "StepFlowConfigFromStepTitle":"Arrange accessment/interview/shortisting(ODI/Client)",
        "StepFlowConfigFromStepId": "Step:ac3d4ee48c4c5e272d74ebd762ceaa41",
        "StepFlowConfigDecisionOptionId": "DecisionOption:fcb1bba5b859b78aff0e16b94a0931b9",
        "StepFlowConfigEndProcess": "NO",
        "StepFlowConfigToStepTitle":"Testing/Assessment",
        "StepFlowConfigToStepId": "Step:1625994eb1c32a0306e391f8b26e767e",
        "CompositeAccessPatterns": "StepFlowConfig#Step:bf8a7e80f6978e9a2d2ee54b9c6494d9#DecisionOption:bf8a7e80f6978e9a2d2ee54b9c6494d9#StepFlowConfigSelectionProcessId"
    }
}
```

This endpoint create a specific StepFlowConfig.

<aside class="warning">If you're not using an administrator API key, note that some StepFlowConfig will return 403 Forbidden if they are hidden for admins only.</aside>

### HTTP Request

`POST https://dev.aimlapps.com/recruitment-svc/api/v1/selectios-processes/SelectionProcess:bf8a7e80f6978e9a2d2ee54b9c6494d9/step-flow-configs`

## Retrive Step Flow Config
```bash
curl "https://dev.aimlapps.com/recruitment-svc/api/v1/selectios-processes/SelectionProcess:bf8a7e80f6978e9a2d2ee54b9c6494d9/step-flow-configs"
  -H "Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw"
```

> The above command when submit JSON structured like this:

```json
{
    "StepFlowConfig": [
        {
            "EntityItemId": {
                "S": "StepFlowConfig:bf8a7e80f6978e9a2d2ee54b9c6494d8"
            },
            "StepFlowConfigSelectionProcessId": {
                "S":"SelectionProcess:bf8a7e80f6978e9a2d2ee54b9c6494d9"
            },
            "StepFlowConfigFromStepId": {
                "S":"Step:bf8a7e80f6978e9a2d2ee54b9c6494d9"
            },
            "StepFlowConfigDecisionOptionId": {
                "S":"DecisionOption:bf8a7e80f6978e9a2d2ee54b9c6494d9"
            },
            "StepFlowConfigEndProcess": {
                "S":"NO"
            },
            "StepFlowConfigToStepId":{
                "S": "Step:bf8a7e80f6978e9a2d2ee54b9c6494d10"
            }
        },
        {
            "EntityItemId": {
                "S": "StepFlowConfig:bf8a7e80f6978e9a2d2ee54b9c6494d8"
            },
            "StepFlowConfigSelectionProcessId": {
                "S":"SelectionProcess:bf8a7e80f6978e9a2d2ee54b9c6494d9"
            },
            "StepFlowConfigFromStepId": {
                "S":"Step:bf8a7e80f6978e9a2d2ee54b9c6494d9"
            },
            "StepFlowConfigDecisionOptionId": {
                "S":"DecisionOption:bf8a7e80f6978e9a2d2ee54b9c6494d9"
            },
            "StepFlowConfigEndProcess": {
                "S":"NO"
            },
            "StepFlowConfigToStepId":{
                "S": "Step:bf8a7e80f6978e9a2d2ee54b9c6494d10"
            }
        }
    ]
}
```

This endpoint retrive StepFlowConfigs.

<aside class="warning">If you're not using an administrator API key, note that some StepFlowConfigs will return 403 Forbidden if they are hidden for admins only.</aside>

### HTTP Request

`GET https://dev.aimlapps.com/recruitment-svc/api/v1/selectios-processes/SelectionProcess:bf8a7e80f6978e9a2d2ee54b9c6494d9/step-flow-configs`

## Update Step Flow Config
```bash
curl "https://dev.aimlapps.com/recruitment-svc/api/v1/selectios-processes/SelectionProcess:bf8a7e80f6978e9a2d2ee54b9c6494d9/step-flow-configs/StepFlowConfig:bf8a7e80f6978e9a2d2ee54b9c6494d8"
  -H "Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw"
```

> The above command when submit JSON structured like this:

```json
{
    "StepFlowConfig":{
        "StepFlowConfigSelectionProcessId": "SelectionProcess:078ce8c7c1d75b663c602c08a8700c3f",
        "StepFlowConfigFromStepTitle":"Arrange accessment/interview/shortisting(ODI/Client)",
        "StepFlowConfigFromStepId": "Step:ac3d4ee48c4c5e272d74ebd762ceaa41",
        "StepFlowConfigDecisionOptionId": "DecisionOption:fcb1bba5b859b78aff0e16b94a0931b9",
        "StepFlowConfigEndProcess": "NO",
        "StepFlowConfigToStepTitle":"Testing/Assessment",
        "StepFlowConfigToStepId": "Step:1625994eb1c32a0306e391f8b26e767e",
        "CompositeAccessPatterns": "StepFlowConfig#Step:bf8a7e80f6978e9a2d2ee54b9c6494d9#DecisionOption:bf8a7e80f6978e9a2d2ee54b9c6494d9#StepFlowConfigSelectionProcessId"
    }
}
```

This endpoint update a specific StepFlowConfig

<aside class="warning">If you're not using an administrator API key, note that some StepFlowConfig will return 403 Forbidden if they are hidden for admins only.</aside>

### HTTP Request

`PUT https://dev.aimlapps.com/recruitment-svc/api/v1/selectios-processes/SelectionProcess:bf8a7e80f6978e9a2d2ee54b9c6494d9/step-flow-configs/StepFlowConfig:bf8a7e80f6978e9a2d2ee54b9c6494d8`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of StepFlowConfig

## View Detail Step Flow Config
```bash
curl "https://dev.aimlapps.com/recruitment-svc/api/v1/selectios-processes/SelectionProcess:bf8a7e80f6978e9a2d2ee54b9c6494d9/step-flow-configs/StepFlowConfig:bf8a7e80f6978e9a2d2ee54b9c6494d8"
  -H "Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw"
```

> The above command when submit JSON structured like this:

```json
[
    {
            "EntityItemId": {
                "S": "StepFlowConfig:bf8a7e80f6978e9a2d2ee54b9c6494d8"
            },
            "StepFlowConfigSelectionProcessId": {
                "S":"SelectionProcess:bf8a7e80f6978e9a2d2ee54b9c6494d9"
            },
            "StepFlowConfigFromStepId": {
                "S":"Step:bf8a7e80f6978e9a2d2ee54b9c6494d9"
            },
            "StepFlowConfigDecisionOptionId": {
                "S":"DecisionOption:bf8a7e80f6978e9a2d2ee54b9c6494d9"
            },
            "StepFlowConfigEndProcess": {
                "S":"NO"
            },
            "StepFlowConfigToStepId":{
                "S": "Step:bf8a7e80f6978e9a2d2ee54b9c6494d10"
            }
        }
]
```

This endpoint view detail a specific StepFlowConfig.

<aside class="warning">If you're not using an administrator API key, note that some StepFlowConfig will return 403 Forbidden if they are hidden for admins only.</aside>

### HTTP Request

`get https://dev.aimlapps.com/recruitment-svc/api/v1/selectios-processes/SelectionProcess:bf8a7e80f6978e9a2d2ee54b9c6494d9/step-flow-configs/StepFlowConfig:bf8a7e80f6978e9a2d2ee54b9c6494d8`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of StepFlowConfig

## Delete a Step Flow Config

```bash
curl "https://dev.aimlapps.com/recruitment-svc/api/v1/selectios-processes/SelectionProcess:bf8a7e80f6978e9a2d2ee54b9c6494d9/step-flow-configs/StepFlowConfig:bf8a7e80f6978e9a2d2ee54b9c6494d8"
  -H "Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw"
```

This endpoint delete a StepFlowConfig.

<aside class="warning">If you're not using an administrator API key, note that some StepFlowConfig will return 403 Forbidden if they are hidden for admins only.</aside>

### HTTP Request

`DELETE https://dev.aimlapps.com/recruitment-svc/api/v1/selectios-processes/SelectionProcess:bf8a7e80f6978e9a2d2ee54b9c6494d9/step-flow-configs/StepFlowConfig:bf8a7e80f6978e9a2d2ee54b9c6494d8`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of StepFlowConfig

# Retrieve Next Processing Step
```bash
curl "https://dev.aimlapps.com/recruitment-svc/api/v1/selection-processes/SelectionProcess:bf8a7e80f6978e9a2d2ee54b9c6494d9/step-flow-configs?contains=Step:ac3d4ee48c4c5e272d74ebd762ceaa41&contains=DecisionOption:fcb1bba5b859b78aff0e16b94a0931b9"
  -H "Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw"
```

> The above command when submit JSON structured like this:

```json
[
    {
        "StepFlowConfigSelectionProcessId": {
            "S": "SelectionProcess:078ce8c7c1d75b663c602c08a8700c3f"
        },
        "StepFlowConfigToStepId": {
            "S": "Step:f065aaaade0d12740ce720e27692bb9b"
        },
        "StepFlowConfigToStepTitle": {
            "S": "Conduct interview"
        },
        "EntityItemId": {
            "S": "StepFlowConfig:ca72411978ad2c0848d2fdd3ea671046"
        },
        "StepFlowConfigEndProcess": {
            "B": "NO"
        },
        "CompositeAccessPatterns": {
            "S": "StepFlowConfig#StepFlowConfigSelectionProcessId:SelectionProcess:078ce8c7c1d75b663c602c08a8700c3f#StepFlowConfigDecisionOptionId:DecisionOption:fcb1bba5b859b78aff0e16b94a0931b9"
        },
        "StepFlowConfigDecisionOptionId": {
            "S": "DecisionOption:fcb1bba5b859b78aff0e16b94a0931b9"
        },
        "StepFlowConfigFromStepTitle": {
            "S": "Arrange accessment/interview/shortisting(ODI/Client)"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "StepFlowConfigFromStepId": {
            "S": "Step:ac3d4ee48c4c5e272d74ebd762ceaa41"
        }
    },
    {
        "StepFlowConfigSelectionProcessId": {
            "S": "SelectionProcess:078ce8c7c1d75b663c602c08a8700c3f"
        },
        "StepFlowConfigToStepId": {
            "S": "Step:741a08e9bde2708b59fee705d09f4cd9"
        },
        "StepFlowConfigToStepTitle": {
            "S": "Recommend to client"
        },
        "EntityItemId": {
            "S": "StepFlowConfig:d4ebadd0029c7a9d3f1801c8c559c98c"
        },
        "StepFlowConfigEndProcess": {
            "B": "NO"
        },
        "CompositeAccessPatterns": {
            "S": "StepFlowConfig#StepFlowConfigSelectionProcessId:SelectionProcess:078ce8c7c1d75b663c602c08a8700c3f#StepFlowConfigDecisionOptionId:DecisionOption:fcb1bba5b859b78aff0e16b94a0931b9"
        },
        "StepFlowConfigDecisionOptionId": {
            "S": "DecisionOption:fcb1bba5b859b78aff0e16b94a0931b9"
        },
        "StepFlowConfigFromStepTitle": {
            "S": "Arrange accessment/interview/shortisting(ODI/Client)"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "StepFlowConfigFromStepId": {
            "S": "Step:ac3d4ee48c4c5e272d74ebd762ceaa41"
        }
    },
    {
        "StepFlowConfigSelectionProcessId": {
            "S": "SelectionProcess:078ce8c7c1d75b663c602c08a8700c3f"
        },
        "StepFlowConfigToStepId": {
            "S": "Step:1625994eb1c32a0306e391f8b26e767e"
        },
        "StepFlowConfigToStepTitle": {
            "S": "Testing/Assessment"
        },
        "EntityItemId": {
            "S": "StepFlowConfig:f3f2f4e5b158583e54fbd6ea655c0d14"
        },
        "StepFlowConfigEndProcess": {
            "B": "NO"
        },
        "CompositeAccessPatterns": {
            "S": "StepFlowConfig#StepFlowConfigSelectionProcessId:SelectionProcess:078ce8c7c1d75b663c602c08a8700c3f#StepFlowConfigDecisionOptionId:DecisionOption:fcb1bba5b859b78aff0e16b94a0931b9"
        },
        "StepFlowConfigDecisionOptionId": {
            "S": "DecisionOption:fcb1bba5b859b78aff0e16b94a0931b9"
        },
        "StepFlowConfigFromStepTitle": {
            "S": "Arrange accessment/interview/shortisting(ODI/Client)"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "StepFlowConfigFromStepId": {
            "S": "Step:ac3d4ee48c4c5e272d74ebd762ceaa41"
        }
    }
]
```

This endpoint retrive StepFlowConfigs.

<aside class="warning">If you're not using an administrator API key, note that some StepFlowConfigs will return 403 Forbidden if they are hidden for admins only.</aside>

### HTTP Request

`GET https://dev.aimlapps.com/recruitment-svc/api/v1/selection-processes/SelectionProcess:bf8a7e80f6978e9a2d2ee54b9c6494d9/step-flow-configs?contains=Step:ac3d4ee48c4c5e272d74ebd762ceaa41&contains=DecisionOption:fcb1bba5b859b78aff0e16b94a0931b9`

# Selection Process
## Create Selection Process

```bash
curl "https://dev.aimlapps.com/recruitment-svc/api/v1/selection-processes"
  -H "Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw"
```

> The above command when submit JSON structured like this:

```json
{
    "SelectionProcess": {
        "SelectionProcessName": "Select Candidate",
        "CompositeAccessPatterns": "SelectionProcess#SelectionProcessName:Select Candidate",
        "Children":{
            "Step": [
                {
                
                    "StepTitle": "Screen Candidate",
                    "StepCouldStart": "YES",
                    "StepNeedDecision": "YES",
                    "StepOfferJob": "NO",
                    "StepLinkSystemResource": "Screen Candidate",
                    "StepLinkPurpose": "Screen Candidate",
                    "CompositeAccessPatterns": "Step#SelectioProcess:931cc0bd784645abaa12df07bb6390c8#StepCouldStart: YES",
                },
                {
                    "StepTitle": "Apply Job",
                    "StepCouldStart": "YES",
                    "StepNeedDecision": "YES",
                    "StepOfferJob": "NO",
                    "StepLinkSystemResource": "Apply Job",
                    "StepLinkPurpose": "Apply Job",
                    "CompositeAccessPatterns":"Step#SelectioProcess:931cc0bd784645abaa12df07bb6390c8#StepCouldStart: YES",

                }
            ]
        }
    }
    
}
```

This endpoint create a specific Selection Process.

<aside class="warning">If you're not using an administrator API key, note that some Selection Processs will return 403 Forbidden if they are hidden for admins only.</aside>

### HTTP Request

`POST https://dev.aimlapps.com/recruitment-svc/api/v1/selection-processes`

<===>
# Job Post
## Create Job Post

```bash
curl "https://dev.aimlapps.com/recruitment-svc/api/v1/job-posts"
  -H "Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw"
```

> The above command when submit JSON structured like this:

```json

{
    "JobPost": {
        "JobPostPostingDate": "02-03-2021",
        "JobPostDeadline": "02-20-2021",
        "JobPostDescription":"Choose on post for Network System",
        "Children":{
            "Channel":[
                {
                    "ChannelJobChannelId": "Male",
                    "ChannelJobChannelName": "ChannelJobChannelName",
                },
                {
                    "PeopleSex": "Female",
                    "PeopleName": "Vina chung",
                    "PeopleId": "People:4585454897fc431899dcdfc5b37fgdg5" 
                }
            ],
             "Vacancy":[
                {
                    "VacancyJobVacancyId": "Male",
                    "VacancyJobVacancyPositionTitle": "ChannelJobChannelName",
                },
                {
                    "PeopleSex": "Female",
                    "PeopleName": "Vina chung",
                    "PeopleId": "People:4585454897fc431899dcdfc5b37fgdg5" 
                }
            ]
        }
    }
}
```

This endpoint create a specific job post.

<aside class="warning">If you're not using an administrator API key, note that some Clients will return 403 Forbidden if they are hidden for admins only.</aside>

### HTTP Request

`POST https://dev.aimlapps.com/recruitment-svc/api/v1/job-posts`

## Retrive Job Posts
```bash
curl "https://dev.aimlapps.com/recruitment-svc/api/v1/job-posts"
  -H "Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw"
```

> The above command when submit JSON structured like this:

```json
{
    "JobPostVacancy": {
        "L": [
            {
                "M": {
                    "VacancyJobVacancyId": {
                        "S": "JobVacancy:f9cc3d391b10df5a81a8a4ea684bc1c8"
                    },
                    "VacancyJobVacancyPositionTitle": {
                        "S": "Accounting Manager"
                    }
                }
            },
            {
                "M": {
                    "VacancyJobVacancyId": {
                        "S": "JobVacancy:fadb9df5ac0b20c43f3f9f195d54e66f"
                    },
                    "VacancyJobVacancyPositionTitle": {
                        "S": "Mobile Developer"
                    }
                }
            }
        ]
    },
    "EntityItemId": {
        "S": "JobPost:3ea66f3b3689c4ddfc28f1d7c1e586a1"
    },
    "JobPostChannel": {
        "L": [
            {
                "M": {
                    "ChannelJobChannelId": {
                        "S": "JobChannel:2b03fb005f0d75e46924c1448b3e033c"
                    },
                    "ChannelJobChannelName": {
                        "S": "HR"
                    }
                }
            },
            {
                "M": {
                    "ChannelJobChannelId": {
                        "S": "JobChannel:6ee8925d50c058dbf55fb568afc71f54"
                    },
                    "ChannelJobChannelName": {
                        "S": "ODI"
                    }
                }
            }
        ]
    },
    "CompositeAccessPatterns": {
        "S": "JobPost#JobPostPostingDate:02-03-2021#JobPostDeadline:02-20-2021"
    },
    "JobPostDescription": {
        "S": "Choose on post for Network System"
    },
    "TenantId": {
        "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
    },
    "JobPostDeadline": {
        "S": "02-20-2021"
    },
    "JobPostPostingDate": {
        "S": "02-03-2021"
    }
}
```

This endpoint retrive job post.

<aside class="warning">If you're not using an administrator API key, note that some job post will return 403 Forbidden if they are hidden for admins only.</aside>

### HTTP Request

`GET https://dev.aimlapps.com/recruitment-svc/api/v1/job-posts`


## View Detail Job Post
```bash
curl "https://dev.aimlapps.com/recruitment-svc/api/v1/job-posts/JobPost:3ea66f3b3689c4ddfc28f1d7c1e586a1"
  -H "Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw"
```

> The above command when submit JSON structured like this:

```json
{
    "JobPostVacancy": {
        "L": [
            {
                "M": {
                    "VacancyJobVacancyId": {
                        "S": "JobVacancy:f9cc3d391b10df5a81a8a4ea684bc1c8"
                    },
                    "VacancyJobVacancyPositionTitle": {
                        "S": "Accounting Manager"
                    }
                }
            },
            {
                "M": {
                    "VacancyJobVacancyId": {
                        "S": "JobVacancy:fadb9df5ac0b20c43f3f9f195d54e66f"
                    },
                    "VacancyJobVacancyPositionTitle": {
                        "S": "Mobile Developer"
                    }
                }
            }
        ]
    },
    "EntityItemId": {
        "S": "JobPost:3ea66f3b3689c4ddfc28f1d7c1e586a1"
    },
    "JobPostChannel": {
        "L": [
            {
                "M": {
                    "ChannelJobChannelId": {
                        "S": "JobChannel:2b03fb005f0d75e46924c1448b3e033c"
                    },
                    "ChannelJobChannelName": {
                        "S": "HR"
                    }
                }
            },
            {
                "M": {
                    "ChannelJobChannelId": {
                        "S": "JobChannel:6ee8925d50c058dbf55fb568afc71f54"
                    },
                    "ChannelJobChannelName": {
                        "S": "ODI"
                    }
                }
            }
        ]
    },
    "CompositeAccessPatterns": {
        "S": "JobPost#JobPostPostingDate:02-03-2021#JobPostDeadline:02-20-2021"
    },
    "JobPostDescription": {
        "S": "Choose on post for Network System"
    },
    "TenantId": {
        "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
    },
    "JobPostDeadline": {
        "S": "02-20-2021"
    },
    "JobPostPostingDate": {
        "S": "02-03-2021"
    }
}
```

This endpoint view detail a specific job post.

<aside class="warning">If you're not using an administrator API key, note that some JobOrders will return 403 Forbidden if they are hidden for admins only.</aside>

### HTTP Request

`GET https://dev.aimlapps.com/recruitment-svc/api/v1/job-posts/JobPost:3ea66f3b3689c4ddfc28f1d7c1e586a1`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the Client to View Detail each job post

## Update Job Post
```bash
curl "https://dev.aimlapps.com/recruitment-svc/api/v1/job-posts/JobPost:3ea66f3b3689c4ddfc28f1d7c1e586a1"
  -H "Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw"
```

> The above command when submit JSON structured like this:

```json
{
    "JobPost": {
        "JobPostPostingDate": "02-03-2021",
        "JobPostDeadline": "02-28-2021",
        "JobPostDescription":"Choose on post for Network System",
        "Children":{
            "Channel":[
                {
                    "ChannelJobChannelId": "JobChannel:2b03fb005f0d75e46924c1448b3e033c",
                    "ChannelJobChannelName": "HR"
                },
                {
                    "ChannelJobChannelId": "JobChannel:6ee8925d50c058dbf55fb568afc71f54",
                    "ChannelJobChannelName": "ODI"
                }
            ],
             "Vacancy":[
                {
                    "VacancyJobVacancyId": "JobVacancy:f9cc3d391b10df5a81a8a4ea684bc1c8",
                    "VacancyJobVacancyPositionTitle": "Accounting Manager"
                },
                {
                    "VacancyJobVacancyId": "JobVacancy:fadb9df5ac0b20c43f3f9f195d54e66f",
                    "VacancyJobVacancyPositionTitle": "Mobile Developer"
                }
            ]
        }
    }
}
```

This endpoint update a specific Client Profile.

<aside class="warning">If you're not using an administrator API key, note that some JobOrders will return 403 Forbidden if they are hidden for admins only.</aside>

### HTTP Request

`PUT https://dev.aimlapps.com/recruitment-svc/api/v1/job-posts/JobPost:3ea66f3b3689c4ddfc28f1d7c1e586a1`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the job post

## Delete Job Post
```bash
curl "https://dev.aimlapps.com/recruitment-svc/api/v1/job-posts/JobPost:3ea66f3b3689c4ddfc28f1d7c1e586a1"
  -H "Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw"
```


This endpoint Delete a specific job post.

<aside class="warning">If you're not using an administrator API key, note that some job post will return 403 Forbidden if they are hidden for admins only.</aside>

### HTTP Request

`DELETE https://dev.aimlapps.com/recruitment-svc/api/v1/job-posts/JobPost:3ea66f3b3689c4ddfc28f1d7c1e586a1`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the job post to delete 
<===>


