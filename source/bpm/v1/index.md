# BPM API Documentation

# Introduction
This document guides you on how to work with resources at the backend of BPM service via API endpoints.

# Authentication
### Header Request
Key             | Value
----            | -----
Authorization   | Bearer Token
Content-Type    | application/json    

# Item Status Changes
## Retrieve All Item Status Changes

### HTTP Request
`GET bpm-svc/api/v1/item-status-changes`

### HTTP Response
> The above HTTP request, if successful, will return Json structured like this:

```json
[
    {
        "ItemStatusChangeRule": {
            "L": [
                {
                    "M": {
                        "PreviousStatus": {
                            "S": "null"
                        },
                        "Operation": {
                            "S": "dsa:item-operation:Create"
                        },
                        "NextStatus": {
                            "S": "dsa:item-status:Drafted"
                        }
                    }
                },
                {
                    "M": {
                        "PreviousStatus": {
                            "S": "dsa:item-status:Drafted"
                        },
                        "Operation": {
                            "S": "dsa:item-operation:Update"
                        },
                        "NextStatus": {
                            "S": "dsa:item-status:Drafted"
                        }
                    }
                },
                {
                    "M": {
                        "PreviousStatus": {
                            "S": "dsa:item-status:Drafted"
                        },
                        "Operation": {
                            "S": "dsa:item-operation:Submit"
                        },
                        "NextStatus": {
                            "S": "dsa:item-status:Submitted"
                        }
                    }
                },
                {
                    "M": {
                        "PreviousStatus": {
                            "S": "dsa:item-status:Submitted"
                        },
                        "Operation": {
                            "S": "dsa:item-operation:Return"
                        },
                        "NextStatus": {
                            "S": "dsa:item-status:Returned"
                        }
                    }
                },
                {
                    "M": {
                        "PreviousStatus": {
                            "S": "dsa:item-status:Returned"
                        },
                        "Operation": {
                            "S": "dsa:item-operation:Update"
                        },
                        "NextStatus": {
                            "S": "dsa:item-status:Updated"
                        }
                    }
                },
                {
                    "M": {
                        "PreviousStatus": {
                            "S": "dsa:item-status:Returned"
                        },
                        "Operation": {
                            "S": "dsa:item-operation:Submit"
                        },
                        "NextStatus": {
                            "S": "dsa:item-status:Submitted"
                        }
                    }
                },
                {
                    "M": {
                        "PreviousStatus": {
                            "S": "dsa:item-status:Updated"
                        },
                        "Operation": {
                            "S": "dsa:item-operation:Update"
                        },
                        "NextStatus": {
                            "S": "dsa:item-status:Updated"
                        }
                    }
                },
                {
                    "M": {
                        "PreviousStatus": {
                            "S": "dsa:item-status:Updated"
                        },
                        "Operation": {
                            "S": "dsa:item-operation:Submit"
                        },
                        "NextStatus": {
                            "S": "dsa:item-status:Submitted"
                        }
                    }
                },
                {
                    "M": {
                        "PreviousStatus": {
                            "S": "dsa:item-status:Submitted"
                        },
                        "Operation": {
                            "S": "dsa:item-operation:Reject"
                        },
                        "NextStatus": {
                            "S": "dsa:item-status:Rejected"
                        }
                    }
                },
                {
                    "M": {
                        "PreviousStatus": {
                            "S": "dsa:item-status:Submitted"
                        },
                        "Operation": {
                            "S": "dsa:item-operation:Verify"
                        },
                        "NextStatus": {
                            "S": "dsa:item-status:Verified"
                        }
                    }
                },
                {
                    "M": {
                        "PreviousStatus": {
                            "S": "dsa:item-status:Submitted"
                        },
                        "Operation": {
                            "S": "dsa:item-operation:Approve"
                        },
                        "NextStatus": {
                            "S": "dsa:item-status:Approved"
                        }
                    }
                },
                {
                    "M": {
                        "PreviousStatus": {
                            "S": "dsa:item-status:Verified"
                        },
                        "Operation": {
                            "S": "dsa:item-operation:Reject"
                        },
                        "NextStatus": {
                            "S": "dsa:item-status:Rejected"
                        }
                    }
                },
                {
                    "M": {
                        "PreviousStatus": {
                            "S": "dsa:item-status:Verified"
                        },
                        "Operation": {
                            "S": "dsa:item-operation:Return"
                        },
                        "NextStatus": {
                            "S": "dsa:item-status:Returned"
                        }
                    }
                },
                {
                    "M": {
                        "PreviousStatus": {
                            "S": "dsa:item-status:Verified"
                        },
                        "Operation": {
                            "S": "dsa:item-operation:Approve"
                        },
                        "NextStatus": {
                            "S": "dsa:item-status:Approved"
                        }
                    }
                }
            ]
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "EntityItemId": {
            "S": "ItemStatusChange:fd526b328805050bbad2a5d61adc3f9e"
        },
        "CompositeAccessPatterns": {
            "S": "ItemStatusChange"
        }
    }
]

```

## Create the Status Change
### HTTP Request
`POST bpm-svc/api/v1/item-status-changes`

### Body Request

```json
{
    "ItemStatusChange": {
        "Children": {
            "Rule": [
                {
                    "PreviousStatus": "null",
                    "Operation": "dsa:item-operation:Create",
                    "NextStatus": "dsa:item-status:Drafted"
                },
                {
                    "PreviousStatus": "dsa:item-status:Drafted",
                    "Operation": "dsa:item-operation:Update",
                    "NextStatus": "dsa:item-status:Drafted"
                },
                {
                    "PreviousStatus": "dsa:item-status:Drafted",
                    "Operation": "dsa:item-operation:Submit",
                    "NextStatus": "dsa:item-status:Submitted"
                },
                {
                    "PreviousStatus": "dsa:item-status:Submitted",
                    "Operation": "dsa:item-operation:Return",
                    "NextStatus": "dsa:item-status:Returned"
                },
                {
                    "PreviousStatus": "dsa:item-status:Returned",
                    "Operation": "dsa:item-operation:Update",
                    "NextStatus": "dsa:item-status:Updated"
                },
                {
                    "PreviousStatus": "dsa:item-status:Returned",
                    "Operation": "dsa:item-operation:Submit",
                    "NextStatus": "dsa:item-status:Submitted"
                },
                {
                    "PreviousStatus": "dsa:item-status:Updated",
                    "Operation": "dsa:item-operation:Update",
                    "NextStatus": "dsa:item-status:Updated"
                },
                {
                    "PreviousStatus": "dsa:item-status:Updated",
                    "Operation": "dsa:item-operation:Submit",
                    "NextStatus": "dsa:item-status:Submitted"
                },
                {
                    "PreviousStatus": "dsa:item-status:Submitted",
                    "Operation": "dsa:item-operation:Reject",
                    "NextStatus": "dsa:item-status:Rejected"
                },
                {
                    "PreviousStatus": "dsa:item-status:Submitted",
                    "Operation": "dsa:item-operation:Verify",
                    "NextStatus": "dsa:item-status:Verified"
                },
                {
                    "PreviousStatus": "dsa:item-status:Submitted",
                    "Operation": "dsa:item-operation:Approve",
                    "NextStatus": "dsa:item-status:Approved"
                },
                {
                    "PreviousStatus": "dsa:item-status:Verified",
                    "Operation": "dsa:item-operation:Reject",
                    "NextStatus": "dsa:item-status:Rejected"
                },
                {
                    "PreviousStatus": "dsa:item-status:Verified",
                    "Operation": "dsa:item-operation:Return",
                    "NextStatus": "dsa:item-status:Returned"
                },
                {
                    "PreviousStatus": "dsa:item-status:Verified",
                    "Operation": "dsa:item-operation:Approve",
                    "NextStatus": "dsa:item-status:Approved"
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
    "ItemStatusChangeRule": {
        "L": [
            {
                "M": {
                    "PreviousStatus": {
                        "S": "null"
                    },
                    "Operation": {
                        "S": "dsa:item-operation:Create"
                    },
                    "NextStatus": {
                        "S": "dsa:item-status:Drafted"
                    }
                }
            },
            {
                "M": {
                    "PreviousStatus": {
                        "S": "dsa:item-status:Drafted"
                    },
                    "Operation": {
                        "S": "dsa:item-operation:Update"
                    },
                    "NextStatus": {
                        "S": "dsa:item-status:Drafted"
                    }
                }
            },
            {
                "M": {
                    "PreviousStatus": {
                        "S": "dsa:item-status:Drafted"
                    },
                    "Operation": {
                        "S": "dsa:item-operation:Submit"
                    },
                    "NextStatus": {
                        "S": "dsa:item-status:Submitted"
                    }
                }
            },
            {
                "M": {
                    "PreviousStatus": {
                        "S": "dsa:item-status:Submitted"
                    },
                    "Operation": {
                        "S": "dsa:item-operation:Return"
                    },
                    "NextStatus": {
                        "S": "dsa:item-status:Returned"
                    }
                }
            },
            {
                "M": {
                    "PreviousStatus": {
                        "S": "dsa:item-status:Returned"
                    },
                    "Operation": {
                        "S": "dsa:item-operation:Update"
                    },
                    "NextStatus": {
                        "S": "dsa:item-status:Updated"
                    }
                }
            },
            {
                "M": {
                    "PreviousStatus": {
                        "S": "dsa:item-status:Returned"
                    },
                    "Operation": {
                        "S": "dsa:item-operation:Submit"
                    },
                    "NextStatus": {
                        "S": "dsa:item-status:Submitted"
                    }
                }
            },
            {
                "M": {
                    "PreviousStatus": {
                        "S": "dsa:item-status:Updated"
                    },
                    "Operation": {
                        "S": "dsa:item-operation:Update"
                    },
                    "NextStatus": {
                        "S": "dsa:item-status:Updated"
                    }
                }
            },
            {
                "M": {
                    "PreviousStatus": {
                        "S": "dsa:item-status:Updated"
                    },
                    "Operation": {
                        "S": "dsa:item-operation:Submit"
                    },
                    "NextStatus": {
                        "S": "dsa:item-status:Submitted"
                    }
                }
            },
            {
                "M": {
                    "PreviousStatus": {
                        "S": "dsa:item-status:Submitted"
                    },
                    "Operation": {
                        "S": "dsa:item-operation:Reject"
                    },
                    "NextStatus": {
                        "S": "dsa:item-status:Rejected"
                    }
                }
            },
            {
                "M": {
                    "PreviousStatus": {
                        "S": "dsa:item-status:Submitted"
                    },
                    "Operation": {
                        "S": "dsa:item-operation:Verify"
                    },
                    "NextStatus": {
                        "S": "dsa:item-status:Verified"
                    }
                }
            },
            {
                "M": {
                    "PreviousStatus": {
                        "S": "dsa:item-status:Submitted"
                    },
                    "Operation": {
                        "S": "dsa:item-operation:Approve"
                    },
                    "NextStatus": {
                        "S": "dsa:item-status:Approved"
                    }
                }
            },
            {
                "M": {
                    "PreviousStatus": {
                        "S": "dsa:item-status:Verified"
                    },
                    "Operation": {
                        "S": "dsa:item-operation:Reject"
                    },
                    "NextStatus": {
                        "S": "dsa:item-status:Rejected"
                    }
                }
            },
            {
                "M": {
                    "PreviousStatus": {
                        "S": "dsa:item-status:Verified"
                    },
                    "Operation": {
                        "S": "dsa:item-operation:Return"
                    },
                    "NextStatus": {
                        "S": "dsa:item-status:Returned"
                    }
                }
            },
            {
                "M": {
                    "PreviousStatus": {
                        "S": "dsa:item-status:Verified"
                    },
                    "Operation": {
                        "S": "dsa:item-operation:Approve"
                    },
                    "NextStatus": {
                        "S": "dsa:item-status:Approved"
                    }
                }
            }
        ]
    },
    "TenantId": {
        "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
    },
    "EntityItemId": {
        "S": "ItemStatusChange:fd526b328805050bbad2a5d61adc3f9e"
    },
    "CompositeAccessPatterns": {
        "S": "ItemStatusChange"
    }
}
```

## Get A Specific Status Change

### HTTP Request
`GET bpm-svc/api/v1/item-status-changes/{id}`

### Query Paramaeters
Parameter       | Description
---------       | -----------
id              | is the identify of status change

### HTTP Response
> The above HTTP request, if successful, will return Json structured like this:

```json
{
    "ItemStatusChangeRule": {
        "L": [
            {
                "M": {
                    "PreviousStatus": {
                        "S": "null"
                    },
                    "Operation": {
                        "S": "dsa:item-operation:Create"
                    },
                    "NextStatus": {
                        "S": "dsa:item-status:Drafted"
                    }
                }
            },
            {
                "M": {
                    "PreviousStatus": {
                        "S": "dsa:item-status:Drafted"
                    },
                    "Operation": {
                        "S": "dsa:item-operation:Update"
                    },
                    "NextStatus": {
                        "S": "dsa:item-status:Drafted"
                    }
                }
            },
            {
                "M": {
                    "PreviousStatus": {
                        "S": "dsa:item-status:Drafted"
                    },
                    "Operation": {
                        "S": "dsa:item-operation:Submit"
                    },
                    "NextStatus": {
                        "S": "dsa:item-status:Submitted"
                    }
                }
            },
            {
                "M": {
                    "PreviousStatus": {
                        "S": "dsa:item-status:Submitted"
                    },
                    "Operation": {
                        "S": "dsa:item-operation:Return"
                    },
                    "NextStatus": {
                        "S": "dsa:item-status:Returned"
                    }
                }
            },
            {
                "M": {
                    "PreviousStatus": {
                        "S": "dsa:item-status:Returned"
                    },
                    "Operation": {
                        "S": "dsa:item-operation:Update"
                    },
                    "NextStatus": {
                        "S": "dsa:item-status:Updated"
                    }
                }
            },
            {
                "M": {
                    "PreviousStatus": {
                        "S": "dsa:item-status:Returned"
                    },
                    "Operation": {
                        "S": "dsa:item-operation:Submit"
                    },
                    "NextStatus": {
                        "S": "dsa:item-status:Submitted"
                    }
                }
            },
            {
                "M": {
                    "PreviousStatus": {
                        "S": "dsa:item-status:Updated"
                    },
                    "Operation": {
                        "S": "dsa:item-operation:Update"
                    },
                    "NextStatus": {
                        "S": "dsa:item-status:Updated"
                    }
                }
            },
            {
                "M": {
                    "PreviousStatus": {
                        "S": "dsa:item-status:Updated"
                    },
                    "Operation": {
                        "S": "dsa:item-operation:Submit"
                    },
                    "NextStatus": {
                        "S": "dsa:item-status:Submitted"
                    }
                }
            },
            {
                "M": {
                    "PreviousStatus": {
                        "S": "dsa:item-status:Submitted"
                    },
                    "Operation": {
                        "S": "dsa:item-operation:Reject"
                    },
                    "NextStatus": {
                        "S": "dsa:item-status:Rejected"
                    }
                }
            },
            {
                "M": {
                    "PreviousStatus": {
                        "S": "dsa:item-status:Submitted"
                    },
                    "Operation": {
                        "S": "dsa:item-operation:Verify"
                    },
                    "NextStatus": {
                        "S": "dsa:item-status:Verified"
                    }
                }
            },
            {
                "M": {
                    "PreviousStatus": {
                        "S": "dsa:item-status:Submitted"
                    },
                    "Operation": {
                        "S": "dsa:item-operation:Approve"
                    },
                    "NextStatus": {
                        "S": "dsa:item-status:Approved"
                    }
                }
            },
            {
                "M": {
                    "PreviousStatus": {
                        "S": "dsa:item-status:Verified"
                    },
                    "Operation": {
                        "S": "dsa:item-operation:Reject"
                    },
                    "NextStatus": {
                        "S": "dsa:item-status:Rejected"
                    }
                }
            },
            {
                "M": {
                    "PreviousStatus": {
                        "S": "dsa:item-status:Verified"
                    },
                    "Operation": {
                        "S": "dsa:item-operation:Return"
                    },
                    "NextStatus": {
                        "S": "dsa:item-status:Returned"
                    }
                }
            },
            {
                "M": {
                    "PreviousStatus": {
                        "S": "dsa:item-status:Verified"
                    },
                    "Operation": {
                        "S": "dsa:item-operation:Approve"
                    },
                    "NextStatus": {
                        "S": "dsa:item-status:Approved"
                    }
                }
            }
        ]
    },
    "TenantId": {
        "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
    },
    "EntityItemId": {
        "S": "ItemStatusChange:fd526b328805050bbad2a5d61adc3f9e"
    },
    "CompositeAccessPatterns": {
        "S": "ItemStatusChange"
    }
}
```

## Update the Status Change
### HTTP Request
`PUT bpm-svc/api/v1/item-status-changes/{id}`

### Query Paramaeters
Parameter       | Description
---------       | -----------
id              | is the identify of status change

### Body Request

```json
{
    "ItemStatusChange": {
        "Children": {
            "Rule": [
                {
                    "PreviousStatus": "null",
                    "Operation": "dsa:item-operation:Create",
                    "NextStatus": "dsa:item-status:Drafted"
                },
                {
                    "PreviousStatus": "dsa:item-status:Drafted",
                    "Operation": "dsa:item-operation:Update",
                    "NextStatus": "dsa:item-status:Drafted"
                },
                {
                    "PreviousStatus": "dsa:item-status:Drafted",
                    "Operation": "dsa:item-operation:Submit",
                    "NextStatus": "dsa:item-status:Submitted"
                },
                {
                    "PreviousStatus": "dsa:item-status:Submitted",
                    "Operation": "dsa:item-operation:Return",
                    "NextStatus": "dsa:item-status:Returned"
                },
                {
                    "PreviousStatus": "dsa:item-status:Returned",
                    "Operation": "dsa:item-operation:Update",
                    "NextStatus": "dsa:item-status:Updated"
                },
                {
                    "PreviousStatus": "dsa:item-status:Returned",
                    "Operation": "dsa:item-operation:Submit",
                    "NextStatus": "dsa:item-status:Submitted"
                },
                {
                    "PreviousStatus": "dsa:item-status:Updated",
                    "Operation": "dsa:item-operation:Update",
                    "NextStatus": "dsa:item-status:Updated"
                },
                {
                    "PreviousStatus": "dsa:item-status:Updated",
                    "Operation": "dsa:item-operation:Submit",
                    "NextStatus": "dsa:item-status:Submitted"
                },
                {
                    "PreviousStatus": "dsa:item-status:Submitted",
                    "Operation": "dsa:item-operation:Reject",
                    "NextStatus": "dsa:item-status:Rejected"
                },
                {
                    "PreviousStatus": "dsa:item-status:Submitted",
                    "Operation": "dsa:item-operation:Verify",
                    "NextStatus": "dsa:item-status:Verified"
                },
                {
                    "PreviousStatus": "dsa:item-status:Submitted",
                    "Operation": "dsa:item-operation:Approve",
                    "NextStatus": "dsa:item-status:Approved"
                },
                {
                    "PreviousStatus": "dsa:item-status:Verified",
                    "Operation": "dsa:item-operation:Reject",
                    "NextStatus": "dsa:item-status:Rejected"
                },
                {
                    "PreviousStatus": "dsa:item-status:Verified",
                    "Operation": "dsa:item-operation:Return",
                    "NextStatus": "dsa:item-status:Returned"
                },
                {
                    "PreviousStatus": "dsa:item-status:Verified",
                    "Operation": "dsa:item-operation:Approve",
                    "NextStatus": "dsa:item-status:Approved"
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
    "ItemStatusChangeRule": {
        "L": [
            {
                "M": {
                    "PreviousStatus": {
                        "S": "null"
                    },
                    "Operation": {
                        "S": "dsa:item-operation:Create"
                    },
                    "NextStatus": {
                        "S": "dsa:item-status:Drafted"
                    }
                }
            },
            {
                "M": {
                    "PreviousStatus": {
                        "S": "dsa:item-status:Drafted"
                    },
                    "Operation": {
                        "S": "dsa:item-operation:Update"
                    },
                    "NextStatus": {
                        "S": "dsa:item-status:Drafted"
                    }
                }
            },
            {
                "M": {
                    "PreviousStatus": {
                        "S": "dsa:item-status:Drafted"
                    },
                    "Operation": {
                        "S": "dsa:item-operation:Submit"
                    },
                    "NextStatus": {
                        "S": "dsa:item-status:Submitted"
                    }
                }
            },
            {
                "M": {
                    "PreviousStatus": {
                        "S": "dsa:item-status:Submitted"
                    },
                    "Operation": {
                        "S": "dsa:item-operation:Return"
                    },
                    "NextStatus": {
                        "S": "dsa:item-status:Returned"
                    }
                }
            },
            {
                "M": {
                    "PreviousStatus": {
                        "S": "dsa:item-status:Returned"
                    },
                    "Operation": {
                        "S": "dsa:item-operation:Update"
                    },
                    "NextStatus": {
                        "S": "dsa:item-status:Updated"
                    }
                }
            },
            {
                "M": {
                    "PreviousStatus": {
                        "S": "dsa:item-status:Returned"
                    },
                    "Operation": {
                        "S": "dsa:item-operation:Submit"
                    },
                    "NextStatus": {
                        "S": "dsa:item-status:Submitted"
                    }
                }
            },
            {
                "M": {
                    "PreviousStatus": {
                        "S": "dsa:item-status:Updated"
                    },
                    "Operation": {
                        "S": "dsa:item-operation:Update"
                    },
                    "NextStatus": {
                        "S": "dsa:item-status:Updated"
                    }
                }
            },
            {
                "M": {
                    "PreviousStatus": {
                        "S": "dsa:item-status:Updated"
                    },
                    "Operation": {
                        "S": "dsa:item-operation:Submit"
                    },
                    "NextStatus": {
                        "S": "dsa:item-status:Submitted"
                    }
                }
            },
            {
                "M": {
                    "PreviousStatus": {
                        "S": "dsa:item-status:Submitted"
                    },
                    "Operation": {
                        "S": "dsa:item-operation:Reject"
                    },
                    "NextStatus": {
                        "S": "dsa:item-status:Rejected"
                    }
                }
            },
            {
                "M": {
                    "PreviousStatus": {
                        "S": "dsa:item-status:Submitted"
                    },
                    "Operation": {
                        "S": "dsa:item-operation:Verify"
                    },
                    "NextStatus": {
                        "S": "dsa:item-status:Verified"
                    }
                }
            },
            {
                "M": {
                    "PreviousStatus": {
                        "S": "dsa:item-status:Submitted"
                    },
                    "Operation": {
                        "S": "dsa:item-operation:Approve"
                    },
                    "NextStatus": {
                        "S": "dsa:item-status:Approved"
                    }
                }
            },
            {
                "M": {
                    "PreviousStatus": {
                        "S": "dsa:item-status:Verified"
                    },
                    "Operation": {
                        "S": "dsa:item-operation:Reject"
                    },
                    "NextStatus": {
                        "S": "dsa:item-status:Rejected"
                    }
                }
            },
            {
                "M": {
                    "PreviousStatus": {
                        "S": "dsa:item-status:Verified"
                    },
                    "Operation": {
                        "S": "dsa:item-operation:Return"
                    },
                    "NextStatus": {
                        "S": "dsa:item-status:Returned"
                    }
                }
            },
            {
                "M": {
                    "PreviousStatus": {
                        "S": "dsa:item-status:Verified"
                    },
                    "Operation": {
                        "S": "dsa:item-operation:Approve"
                    },
                    "NextStatus": {
                        "S": "dsa:item-status:Approved"
                    }
                }
            }
        ]
    },
    "TenantId": {
        "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
    },
    "EntityItemId": {
        "S": "ItemStatusChange:fd526b328805050bbad2a5d61adc3f9e"
    },
    "CompositeAccessPatterns": {
        "S": "ItemStatusChange"
    }
}
```

## Delete the Status Change
### HTTP Request
`DELETE bpm-svc/api/v1/item-status-changes/{id}`

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

# Policies
## Retrieve All Policies

### HTTP Request
`GET bpm-svc/api/v1/policies`

### HTTP Response
> The above HTTP request, if successful, will return Json structured like this:

```json
[
    {
        "PolicyName": {
            "S": "Trip request basic operations"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "EntityItemId": {
            "S": "Policy:15a08cc214f576649ab3bec4682e3748"
        },
        "CompositeAccessPatterns": {
            "S": "Policy"
        },
        "PolicyStatement": {
            "L": [
                {
                    "M": {
                        "Resource": {
                            "L": [
                                {
                                    "S": "aiml:dsa:trip-request/*"
                                }
                            ]
                        },
                        "Effect": {
                            "S": "Allow"
                        },
                        "Action": {
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
                        }
                    }
                }
            ]
        },
        "PolicyType": {
            "S": "DSA_ITEM_BASIC_OPERATION"
        }
    },
    {
        "PolicyName": {
            "S": "Trip request managing operations"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "EntityItemId": {
            "S": "Policy:5cd7d152d789404f4a7b107241f0e8e1"
        },
        "CompositeAccessPatterns": {
            "S": "Policy"
        },
        "PolicyStatement": {
            "L": [
                {
                    "M": {
                        "Condition": {
                            "M": {
                                "StringNotEquals": {
                                    "M": {
                                        "aiml:UserId": {
                                            "S": "${aiml:ResourceOwner}"
                                        }
                                    }
                                }
                            }
                        },
                        "Resource": {
                            "L": [
                                {
                                    "S": "aiml:dsa:trip-request/*"
                                }
                            ]
                        },
                        "Action": {
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
                                    "S": "dsa:item-operation:Discuss"
                                }
                            ]
                        },
                        "Effect": {
                            "S": "Allow"
                        }
                    }
                }
            ]
        },
        "PolicyType": {
            "S": "DSA_ITEM_EXTENDED_OPERATION"
        }
    },
    {
        "PolicyName": {
            "S": "Trip request final validation"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "EntityItemId": {
            "S": "Policy:61ed51b24a12128bfddbe6c1fab37cb4"
        },
        "CompositeAccessPatterns": {
            "S": "Policy"
        },
        "PolicyStatement": {
            "L": [
                {
                    "M": {
                        "Condition": {
                            "M": {
                                "StringNotEquals": {
                                    "M": {
                                        "aiml:UserId": {
                                            "S": "${aiml:ResourceOwner}"
                                        }
                                    }
                                }
                            }
                        },
                        "Resource": {
                            "L": [
                                {
                                    "S": "aiml:dsa:trip-request/*"
                                }
                            ]
                        },
                        "Action": {
                            "L": [
                                {
                                    "S": "dsa:item-operation:Retrieve"
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
                        "Effect": {
                            "S": "Allow"
                        }
                    }
                }
            ]
        },
        "PolicyType": {
            "S": "DSA_ITEM_EXTENDED_OPERATION"
        }
    },
    {
        "PolicyName": {
            "S": "Item Operation DSA"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "EntityItemId": {
            "S": "Policy:f5872a63a0bdd9a9deda03c1de1de6bf"
        },
        "CompositeAccessPatterns": {
            "S": "Policy"
        },
        "PolicyStatement": {
            "L": [
                {
                    "M": {
                        "Condition": {
                            "M": {
                                "StringEquals": {
                                    "M": {
                                        "aiml:UserId": {
                                            "S": "${aiml:ResourceOwner}"
                                        },
                                        "aiml:dsa:item-status": {
                                            "L": [
                                                {
                                                    "S": "Drafted"
                                                },
                                                {
                                                    "S": "Returned"
                                                },
                                                {
                                                    "S": "Updated"
                                                }
                                            ]
                                        }
                                    }
                                }
                            }
                        },
                        "Resource": {
                            "L": [
                                {
                                    "S": "aiml:dsa:trip-request/*"
                                }
                            ]
                        },
                        "Action": {
                            "L": [
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
                        "Effect": {
                            "S": "Allow"
                        }
                    }
                },
                {
                    "M": {
                        "Condition": {
                            "M": {
                                "StringEquals": {
                                    "M": {
                                        "aiml:dsa:item-status": {
                                            "L": [
                                                {
                                                    "S": "Submitted"
                                                },
                                                {
                                                    "S": "Verified"
                                                }
                                            ]
                                        }
                                    }
                                },
                                "Bool": {
                                    "M": {
                                        "aiml:UserRoleDirectSupervisor": {
                                            "S": "true"
                                        },
                                        "aiml:UserFinalValidator": {
                                            "S": "false"
                                        },
                                        "aiml:UserPerformedLatestOperation": {
                                            "S": "false"
                                        }
                                    }
                                }
                            }
                        },
                        "Resource": {
                            "L": [
                                {
                                    "S": "aiml:dsa:trip-request/*"
                                }
                            ]
                        },
                        "Action": {
                            "L": [
                                {
                                    "S": "dsa:item-operation:Verify"
                                },
                                {
                                    "S": "dsa:item-operation:Return"
                                },
                                {
                                    "S": "dsa:item-operation:Reject"
                                }
                            ]
                        },
                        "Effect": {
                            "S": "Allow"
                        }
                    }
                },
                {
                    "M": {
                        "Condition": {
                            "M": {
                                "StringEquals": {
                                    "M": {
                                        "aiml:dsa:item-status": {
                                            "L": [
                                                {
                                                    "S": "Submitted"
                                                },
                                                {
                                                    "S": "Verified"
                                                }
                                            ]
                                        }
                                    }
                                },
                                "Bool": {
                                    "M": {
                                        "aiml:UserFinalValidator": {
                                            "S": "true"
                                        },
                                        "aiml:UserPerformedLatestOperation": {
                                            "S": "false"
                                        }
                                    }
                                }
                            }
                        },
                        "Resource": {
                            "L": [
                                {
                                    "S": "aiml:dsa:trip-request/*"
                                }
                            ]
                        },
                        "Action": {
                            "L": [
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
                        "Effect": {
                            "S": "Allow"
                        }
                    }
                }
            ]
        },
        "PolicyType": {
            "S": "DSA_ITEM_OPERATION_CONTROL"
        }
    }
]
```

## Create a new Policy
### HTTP Request
`POST bpm-svc/api/v1/policies`

### Body Request

```json
{
    "PolicyName": "Trip request basic operations",
    "PolicyStatement": [
        {
            "Effect": "Allow",
            "Action": [
                "dsa:item-operation:Create",
                "dsa:item-operation:Retrieve",
                "dsa:item-operation:Update",
                "dsa:item-operation:Delete",
                "dsa:item-operation:Submit",
            ],
            "Resource": [
                "aiml:dsa:trip-request/*"
            ]
        }
    ]
}
```

### HTTP Response
> The above HTTP request, if successful, will return Json structured like this:

```json
[
    {
        "PolicyName": {
            "S": "Trip request basic operations"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "EntityItemId": {
            "S": "Policy:15a08cc214f576649ab3bec4682e3748"
        },
        "CompositeAccessPatterns": {
            "S": "Policy"
        },
        "PolicyStatement": {
            "L": [
                {
                    "M": {
                        "Resource": {
                            "L": [
                                {
                                    "S": "aiml:dsa:trip-request/*"
                                }
                            ]
                        },
                        "Effect": {
                            "S": "Allow"
                        },
                        "Action": {
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
                        }
                    }
                }
            ]
        },
        "PolicyType": {
            "S": "DSA_ITEM_BASIC_OPERATION"
        }
    }
]
```

## Retrieve A Policy

### HTTP Request
`GET bpm-svc/api/v1/policies/{id}`

### Query Paramaeters
Parameter       | Description
---------       | -----------
id              | is the identify of policy

### HTTP Response
> The above HTTP request, if successful, will return Json structured like this:

```json
{
    "PolicyName": {
        "S": "Trip request basic operations"
    },
    "TenantId": {
        "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
    },
    "EntityItemId": {
        "S": "Policy:15a08cc214f576649ab3bec4682e3748"
    },
    "CompositeAccessPatterns": {
        "S": "Policy"
    },
    "PolicyStatement": {
        "L": [
            {
                "M": {
                    "Resource": {
                        "L": [
                            {
                                "S": "aiml:dsa:trip-request/*"
                            }
                        ]
                    },
                    "Effect": {
                        "S": "Allow"
                    },
                    "Action": {
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
                    }
                }
            }
        ]
    },
    "PolicyType": {
        "S": "DSA_ITEM_BASIC_OPERATION"
    }
}
```

## Update the Status Change
### HTTP Request
`PUT bpm-svc/api/v1/policies/{id}`

### Query Paramaeters
Parameter       | Description
---------       | -----------
id              | is the identify of policy

### Body Request

```json
{
    "PolicyName": "Trip request basic operations",
    "PolicyStatement": [
        {
            "Effect": "Allow",
            "Action": [
                "dsa:item-operation:Create",
                "dsa:item-operation:Retrieve",
                "dsa:item-operation:Update",
                "dsa:item-operation:Delete",
                "dsa:item-operation:Submit",
            ],
            "Resource": [
                "aiml:dsa:trip-request/*"
            ]
        }
    ]
}
```

### HTTP Response
> The above HTTP request, if successful, will return Json structured like this:

```json
{
    "PolicyName": {
        "S": "Trip request basic operations"
    },
    "TenantId": {
        "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
    },
    "EntityItemId": {
        "S": "Policy:15a08cc214f576649ab3bec4682e3748"
    },
    "CompositeAccessPatterns": {
        "S": "Policy"
    },
    "PolicyStatement": {
        "L": [
            {
                "M": {
                    "Resource": {
                        "L": [
                            {
                                "S": "aiml:dsa:trip-request/*"
                            }
                        ]
                    },
                    "Effect": {
                        "S": "Allow"
                    },
                    "Action": {
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
                    }
                }
            }
        ]
    },
    "PolicyType": {
        "S": "DSA_ITEM_BASIC_OPERATION"
    }
}
```

## Delete the Status Change
### HTTP Request
`DELETE bpm-svc/api/v1/policies/{id}`

### Query Paramaeters
Parameter       | Description
---------       | -----------
id              | is the identify of policy

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

# Get Next Operation

### HTTP Request
`GET bpm-svc/api/v1/get-next-item-operations?aiml:dsa:item-status=Returned&aiml:ResourceOwner=son.hom@aimlera.com&aiml:UserId=son.hom@aimlera.com&aiml:UserRoleDirectSupervisor=false&aiml:UserFinalValidator=false&aiml:UserPerformedLatestOperation=false`

### Query Paramaeters
Parameter                           | Description
---------                           | -----------
aiml:dsa:item-status                | is the status of item.
aiml:ResourceOwner                  | is the email of creator.
aiml:UserId                         | is the email of user login into application.
aiml:UserRoleDirectSupervisor       | is the user role direct supervior. It return boolean.
aiml:UserFinalValidator             | is the user final validator. It return boolean.
aiml:UserPerformedLatestOperation   | is the user performed lastest operation. It return boolean.

### HTTP Response
> The above HTTP request, if successful, will return Json structured like this:

```json
[
    true,
    "You're denied from performing the operation.",
    {
        "Effect": "Allow",
        "Action": [
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
    200
]
```

# Check Operation

### HTTP Request
`GET bpm-svc/api/v1/get-next-item-operations?aiml:ResourceOwner=son.hom@aimlera.com&aiml:UserId=son.hom@aimlera.com&Resource=aiml:dsa:trip-request/&PreviousStatus=dsa:item-status:Returned&Operation=dsa:item-operation:Submit`

### Query Paramaeters
Parameter                           | Description
---------                           | -----------
aiml:ResourceOwner                  | is the email of creator.
aiml:UserId                         | is the email of user login into application.
Resource                            | is the resource of trip request.
PreviousStatus                      | is the previous status of the item.
Operation                           | is the action that you want to do on the resource.

### HTTP Response
> The above HTTP request, if successful, will return Json structured like this:

```json
[
    false,
    "You're allowed to perform the operation.",
    {
        "Resource": "aiml:dsa:trip-request/",
        "Effect": "Allow",
        "Message": "You're allowed to perform the operation."
    },
    200
]
```

# Get New Status

### HTTP Request
`GET bpm-svc/api/v1/get-new-status?Resource=aiml:dsa:trip-request/&PreviousStatus=dsa:item-status:Returned&Operation=dsa:item-operation:Submit`

### Query Paramaeters
Parameter                           | Description
---------                           | -----------
Resource                            | is the resource of trip request.
PreviousStatus                      | is the previous status of the item.
Operation                           | is the action that you want to do on the resource.

### HTTP Response
> The above HTTP request, if successful, will return Json structured like this:

```json
[
    false,
    "New status could be determined.",
    {
        "NextStatus": "dsa:item-status:Submitted",
        "PreviousStatus": "dsa:item-status:Returned",
        "Message": "New status could be determined."
    },
    200
]
```

# Roles

## Get User Roles

### HTTP Request
`GET bpm-svc/api/v1/user-roles`

### HTTP Response
> The above HTTP request, if successful, will return Json structured like this:

```json
[
    {
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "EntityItemId": {
            "S": "UserRole:21e38395d03b1eae5009264bc96f3608"
        },
        "UserRoleRole": {
            "L": [
                {
                    "M": {
                        "RoleId": {
                            "S": "Role:8f4086c5a8c48e44c9f2a7e03a44b7d9"
                        },
                        "RoleType": {
                            "S": "NATIVE"
                        }
                    }
                }
            ]
        },
        "CompositeAccessPatterns": {
            "S": "UserRole#User:son.hom@aimlera.com"
        },
        "UserRoleUserId": {
            "S": "son.hom@aimlera.com"
        }
    },
    {
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "EntityItemId": {
            "S": "UserRole:a00f3ebd56e43f79218038be79b1ff98"
        },
        "UserRoleRole": {
            "L": [
                {
                    "M": {
                        "RoleId": {
                            "S": "Role:0deb8fcac085437d8a0df572a5d216b4"
                        },
                        "RoleType": {
                            "S": "NATIVE"
                        }
                    }
                },
                {
                    "M": {
                        "RoleId": {
                            "S": "Role:5387cd2eff7523044338979d36b4b38c"
                        },
                        "RoleType": {
                            "S": "EXTENDED"
                        }
                    }
                }
            ]
        },
        "CompositeAccessPatterns": {
            "S": "UserRole#User:sreyta.sean@aimlera.com"
        },
        "UserRoleUserId": {
            "S": "sreyta.sean@aimlera.com"
        }
    },
    {
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "EntityItemId": {
            "S": "UserRole:d564f6c30e5470b981377cb3cd4b0351"
        },
        "UserRoleRole": {
            "L": [
                {
                    "M": {
                        "RoleId": {
                            "S": "Role:9f66281525f4760fb34bfd2012dbdcf9"
                        },
                        "RoleType": {
                            "S": "NATIVE"
                        }
                    }
                },
                {
                    "M": {
                        "RoleId": {
                            "S": "Role:4d544df22238f1beccca28534e18b0ba"
                        },
                        "RoleType": {
                            "S": "EXTENDED"
                        }
                    }
                }
            ]
        },
        "CompositeAccessPatterns": {
            "S": "UserRole#User:samai.duch@aimlera.com"
        },
        "UserRoleUserId": {
            "S": "samai.duch@aimlera.com"
        }
    }
]
```

## Retrieve all Roles

### HTTP Request
`GET bpm-svc/api/v1/roles`

### HTTP Response
> The above HTTP request, if successful, will return Json structured like this:

```json
[
    {
        "RoleName": {
            "S": "Individual Staff Role"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "EntityItemId": {
            "S": "Role:0deb8fcac085437d8a0df572a5d216b4"
        },
        "RolePolicy": {
            "L": [
                {
                    "S": "Policy:15a08cc214f576649ab3bec4682e3748"
                }
            ]
        }
    },
    {
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "RoleName": {
            "S": "MD's Role"
        },
        "EntityItemId": {
            "S": "Role:4d544df22238f1beccca28534e18b0ba"
        },
        "RolePolicy": {
            "L": [
                {
                    "S": "Policy:61ed51b24a12128bfddbe6c1fab37cb4"
                }
            ]
        }
    },
    {
        "RoleName": {
            "S": "Manager's Role"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "EntityItemId": {
            "S": "Role:5387cd2eff7523044338979d36b4b38c"
        },
        "RolePolicy": {
            "L": [
                {
                    "S": "Policy:5cd7d152d789404f4a7b107241f0e8e1"
                }
            ]
        }
    },
    {
        "RoleName": {
            "S": "Individual Staff Role"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "EntityItemId": {
            "S": "Role:8f4086c5a8c48e44c9f2a7e03a44b7d9"
        },
        "RolePolicy": {
            "L": [
                {
                    "S": "Policy:15a08cc214f576649ab3bec4682e3748"
                }
            ]
        }
    },
    {
        "RoleName": {
            "S": "Individual Staff Role"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "EntityItemId": {
            "S": "Role:9f66281525f4760fb34bfd2012dbdcf9"
        },
        "RolePolicy": {
            "L": [
                {
                    "S": "Policy:15a08cc214f576649ab3bec4682e3748"
                }
            ]
        }
    }
]
```

## Retrieve a Role

### HTTP Request
`GET bpm-svc/api/v1/roles/{id}`

### Query Paramaeters
Parameter       | Description
---------       | -----------
id              | is the identify of the role

### HTTP Response
> The above HTTP request, if successful, will return Json structured like this:

```json
{
    "RoleName": {
        "S": "Individual Staff Role"
    },
    "TenantId": {
        "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
    },
    "EntityItemId": {
        "S": "Role:0deb8fcac085437d8a0df572a5d216b4"
    },
    "RolePolicy": {
        "L": [
            {
                "S": "Policy:15a08cc214f576649ab3bec4682e3748"
            }
        ]
    }
}
```

# DSA Travel Fee Allowance

## Retrieve All Travel Fee Allowances

### HTTP Request
`GET bpm-svc/api/v1/dsa-travel-fee-allowances`

### HTTP Response
> The above HTTP request, if successful, will return Json structured like this:

```json
[
    {
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "EntityItemId": {
            "S": "TravelFeeAllowanceDsa:24fecbd22b8e2a706a31b1b3e137fb6a"
        },
        "Effect": {
            "S": "Allow"
        },
        "CompositeAccessPatterns": {
            "S": "TravelFeeAllowanceDsa"
        },
        "TravelFeeAllowanceDsaCondition": {
            "L": [
                {
                    "M": {
                        "StringEquals": {
                            "M": {
                                "aiml:dsa:TransportMode": {
                                    "S": "PublicTransport"
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

## Create A Travel Fee Allowance

### HTTP Request
`POST bpm-svc/api/v1/dsa-travel-fee-allowances`

### HTTP Response
> The above HTTP request, if successful, will return Json structured like this:

```json
{
    "TravelFeeAllowanceDsa": {
        "Effect": "Allow",
        "Children": {
            "Condition": [
                {
                    "StringEquals": {
                        "aiml:dsa:TransportMode": "PublicTransport"
                    }
                }
            ]
        }
    }
}
```

## Delete A Travel Fee Allowance

### HTTP Request
`DELETE bpm-svc/api/v1/dsa-travel-fee-allowances/{id}`

### Query Paramaeters
Parameter       | Description
---------       | -----------
id              | is the identify of the travel fee allowance.

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

# Check Business Role

### HTTP Request
`GET bpm-svc/api/v1/business-roles?Policy=TravelFeeAllowanceDsa&aiml:dsa:TransportMode=PublicTransport`

### Query Paramaeters
Parameter                       | Description
---------                       | -----------
Policy                          | is the name of policy.
aiml:dsa:TransportMode          | is the mode of transport. Ex: PublicTransport, CompanyCar, ...
### HTTP Response
> The above HTTP request, if successful, will return Json structured like this:

```json
{
    "Effect": "Allow"
}
```

