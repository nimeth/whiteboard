# BPM API Documentation

# Introduction
This document guides you on how to work with resources at the backend of DSA service via API endpoints. Those resources include Trip Requests, etc.

# Authentication
### Header Request
Key             | Value
----            | -----
Authorization   | Bearer Token
Content-Type    | application/json    

# Operation
## Get Status Changes

### HTTP Request
`GET bpm-svc/api/v1/trip-request-item-status-changes`

### HTTP Response
> The above HTTP request, if successful, will return Json structured like this:

```json 
[
    {
        "TripRequestItemStatusChangeFrom": {
            "S": "DRAFTED"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "TripRequestItemStatusChangeTo": {
            "S": "SUBMITTED"
        },
        "EntityItemId": {
            "S": "TripRequestItemStatusChange:3da7f1b0b6c98a8e41d26bb885c2a109"
        },
        "CompositeAccessPatterns": {
            "S": "TripRequestItemStatusChange#TripRequestItemStatusChangeFrom:DRAFTED#TripRequestItemStatusChangeOperation:Submit"
        },
        "TripRequestItemStatusChangeOperation": {
            "S": "Submit"
        }
    },
    {
        "TripRequestItemStatusChangeFrom": {
            "S": "NULL"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "TripRequestItemStatusChangeTo": {
            "S": "DRAFTED"
        },
        "EntityItemId": {
            "S": "TripRequestItemStatusChange:cef56f337c4d27e85cd08d8da6a59e11"
        },
        "CompositeAccessPatterns": {
            "S": "TripRequestItemStatusChange#TripRequestItemStatusChangeFrom:NULL#TripRequestItemStatusChangeOperation:Create"
        },
        "TripRequestItemStatusChangeOperation": {
            "S": "Create"
        }
    }
]
```

### HTTP Request Filter 
`GET bpm-svc/api/v1/trip-request-item-status-changes?contains=TripRequestItemStatusChangeFrom:NULL#TripRequestItemStatusChangeOperation:Create`

### Query Paramaeters
Parameter                               | Description
---------                               | -----------
TripRequestItemStatusChangeOperation    | Is the action of operation. Ex: Create, Submit, Comment, Verify, Approve, Reject
TripRequestItemStatusChangeFrom         | Is the current status.

### HTTP Response Filter
> The above HTTP request, if successful, will return Json structured like this:

```json
[
    {
        "TripRequestItemStatusChangeFrom": {
            "S": "NULL"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "TripRequestItemStatusChangeTo": {
            "S": "DRAFTED"
        },
        "EntityItemId": {
            "S": "TripRequestItemStatusChange:cef56f337c4d27e85cd08d8da6a59e11"
        },
        "CompositeAccessPatterns": {
            "S": "TripRequestItemStatusChange#TripRequestItemStatusChangeFrom:NULL#TripRequestItemStatusChangeOperation:Create"
        },
        "TripRequestItemStatusChangeOperation": {
            "S": "Create"
        }
    }
]
```

## Create the Status Change
### HTTP Request
`POST bpm-svc/api/v1/trip-request-item-status-changes`

### Body Request

```json
{
    "TripRequestItemStatusChange": {
        "TripRequestItemStatusChangeFrom": "SUBMITTED",
        "TripRequestItemStatusChangeOperation": "Comment",
        "TripRequestItemStatusChangeTo": "COMMENTED"
    }
}
```

### HTTP Response
> The above HTTP request, if successful, will return Json structured like this:

```json
{
    "TripRequestItemStatusChangeFrom": {
        "S": "SUBMITTED"
    },
    "TenantId": {
        "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
    },
    "TripRequestItemStatusChangeTo": {
        "S": "COMMENTED"
    },
    "EntityItemId": {
        "S": "TripRequestItemStatusChange:8a3c3801c1af285286a90e132fffd79c"
    },
    "CompositeAccessPatterns": {
        "S": "TripRequestItemStatusChange#TripRequestItemStatusChangeFrom:SUBMITTED#TripRequestItemStatusChangeOperation:Comment"
    },
    "TripRequestItemStatusChangeOperation": {
        "S": "Comment"
    }
}
```

## Get A Specific Status Change

### HTTP Request
`GET bpm-svc/api/v1/trip-request-item-status-changes/{id}`

### Query Paramaeters
Parameter       | Description
---------       | -----------
id              | is the identify of status change

### HTTP Response
> The above HTTP request, if successful, will return Json structured like this:

```json
[
    {
        "TripRequestItemStatusChangeFrom": {
            "S": "NULL"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "TripRequestItemStatusChangeTo": {
            "S": "DRAFTED"
        },
        "EntityItemId": {
            "S": "TripRequestItemStatusChange:cef56f337c4d27e85cd08d8da6a59e11"
        },
        "CompositeAccessPatterns": {
            "S": "TripRequestItemStatusChange#TripRequestItemStatusChangeFrom:NULL#TripRequestItemStatusChangeOperation:Create"
        },
        "TripRequestItemStatusChangeOperation": {
            "S": "Create"
        }
    }
]
```

## Update the Status Change
### HTTP Request
`PUT bpm-svc/api/v1/trip-request-item-status-changes/{id}`

### Query Paramaeters
Parameter       | Description
---------       | -----------
id              | is the identify of status change

### Body Request

```json
{
    "TripRequestItemStatusChange": {
        "TripRequestItemStatusChangeFrom": "SUBMITTED",
        "TripRequestItemStatusChangeOperation": "Comment",
        "TripRequestItemStatusChangeTo": "COMMENTED"
    }
}
```
### HTTP Response
> The above HTTP request, if successful, will return Json structured like this:

```json
{
    "TripRequestItemStatusChangeFrom": {
        "S": "SUBMITTED"
    },
    "EntityItemId": {
        "S": "TripRequestItemStatusChange:3da7f1b0b6c98a8e41d26bb885c2a109"
    },
    "TenantId": {
        "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
    },
    "TripRequestItemStatusChangeTo": {
        "S": "COMMENTED"
    },
    "CompositeAccessPatterns": {
        "S": "TripRequestItemStatusChange#TripRequestItemStatusChangeFrom:SUBMITTED#TripRequestItemStatusChangeOperation:Comment"
    },
    "TripRequestItemStatusChangeOperation": {
        "S": "Comment"
    }
}
```

## Delete the Status Change
### HTTP Request
`DELETE bpm-svc/api/v1/trip-request-item-status-changes/{id}`

### Query Paramaeters
Parameter       | Description
---------       | -----------
id              | is the identify of status change

### HTTP Response
> The above HTTP request, if successful, will return Json structured like this:

```json
{
    "UnprocessedItems": [],
    "ConsumedCapacity": [
        {
            "TableName": "PolicyManagerDev",
            "CapacityUnits": 1
        }
    ],
    "@metadata": {
        "statusCode": 200,
        "effectiveUri": "https://dynamodb.ap-southeast-1.amazonaws.com",
        "headers": {
            "server": "Server",
            "date": "Fri, 19 Feb 2021 08:00:21 GMT",
            "content-type": "application/x-amz-json-1.0",
            "content-length": "97",
            "connection": "keep-alive",
            "x-amzn-requestid": "SUH7SV6P7TMI2JCTO09BPOUK0FVV4KQNSO5AEMVJF66Q9ASUAAJG",
            "x-amz-crc32": "1941590622"
        },
        "transferStats": {
            "http": [
                []
            ]
        }
    }
}
```