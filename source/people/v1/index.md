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
Welcome to the People API! You can use our API access People API endpoints, which can get information on various candidate in our database.
# Authentication

> To authorize, use this code:

```php
# With shell, you can just pass the correct header with each request
curl "api_endpoint_here"
  -H "Authorization: Bearer eyJraWQiOiJEOFQ0V0IxWk9TTXVWUTd5d05KZWh6dDFhcGZFYkRwcVpwMEg5RWVicEd3PSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiIxNWNkOGNhZS0yY2M4LTQyNDMtYTdhMC03NjBiYzcwZmVhNmYiLCJjdXN0b206dGllciI6IlByb2Zlc3Npb25hbCBUaWVyIiwiaXNzIjoiaHR0cHM6XC9cL2NvZ25pdG8taWRwLmFwLXNvdXRoZWFzdC0xLmFtYXpvbmF3cy5jb21cL2FwLXNvdXRoZWFzdC0xX3dwMndwalZnaiIsImNvZ25pdG86dXNlcm5hbWUiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIiwiY3VzdG9tOnRlbmFudF9pZCI6IlRFTkFOVDllZDE3ZjA0MDQ1NDRkZDQ5NzdmMGE0MDRjNDIxNGEyIiwiZ2l2ZW5fbmFtZSI6IlNhbWFpIiwiYXVkIjoiNjgzOHBoNWVlY28wNmw2bzN0OXFtMGMxZDYiLCJldmVudF9pZCI6ImJlNGIxMTNmLTYzMWQtNDNlMi1hNzcxLTgzNDAwYzdlZjc0YyIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNjExNjI5Mjk3LCJleHAiOjE2MTE2MzI4OTcsImN1c3RvbTpyb2xlIjoiVGVuYW50VXNlciIsImlhdCI6MTYxMTYyOTI5NywiZmFtaWx5X25hbWUiOiJEdWNoIiwiZW1haWwiOiJzYW1haS5kdWNoQGFpbWxlcmEuY29tIn0.fz4bVGKbYsPkC3SI5MwD6Fro7KIFk9b3Q5UkebW9461VGV-dWGu7eQ45hFYBlMWry2Tn_43yuFkP-Ppd74VQ0Ua-czSgAWwln9OkXkfvQ8Ifrczkw0y7OSRzUaSNvh80y1K_YzDlRcuIHju70YqDSXylK4KyOv6P2JZ7ydwwvwkvnTNTctzqb_IL7ZWBinZaK_LXe79-smPi4EUwXANr7jXZg1I8Dd4tzsRiA5rOOd1IKZfRYYDTAeCHLwKwnvSU-ER-RkwW53pqDnwk9tPmd4gWDRao65Oj-ncRQRYtptPqFhQX0i2xF42etb8BUgTZxazTApOs40I5rxvapwp_Fw"
```

# People
## Create Create People

> The above command when submit JSON structured like this:

```json
{
    "People": {
        "PeopleFirstName": "Dalin",
        "PeopleMiddleName": "Lin",
         "PeopleLastName": "Luon",
        "PeopleGender": "F",
        "PeopleBirthDate": "04-02-1998",
        "PeopleMaritalStatus": "Available",
        "PeopleNationality": "Cambodia",
        "PeopleBirthLocationLevel1": "Battambong",
        "PeopleProfilePhoto": "profile.png",
        "PeopleProfileSummary": "I am 23 year old. I finish ...",
        "PeopleAchievement": "I finish ...",
        "CompositeAccessPatterns":"",
        "Children":{
            "ComputerApplication":[
                {
                    "ComputerApplicationName": "Microsoft Excel",
                    "ComputerApplicationLevel": "Intermediate"
                }
            ],
            "CoreCompetency":[
                {
                    "CoreCompetencyCompetency": "Use Computer"
                }
            ],
            "Document":[
                {
                    "DocumentName": "High School Certificate",
                    "DocumentFileName": "UUID"
                     
                }
            ],
            "Contact":[
                {
                    "ContactName": "Putheara",
                    "ContactValue": "putheara.pen@gmail.com"
                }
            ],
             "Language":[
                {
                    "LanguageLanguage": "English",
                    "LanguageSkill": "Speaking, Writing, Listening, Reading", 
                    "LanguageProficiencyLevel": "Professional Working Proficiency, Limited Working Proficiency" 
                }
            ]
        }
    }
}
```

### HTTP Request

`POST https://dev.aimlapps.com/people-svc/api/v1/people`

## Update People

> The above command when submit JSON structured like this:

```json
{
    "People": {
        "PeopleFirstName": "Dalin",
        "PeopleMiddleName": "Lin",
         "PeopleLastName": "Luon",
        "PeopleGender": "F",
        "PeopleBirthDate": "04-02-1998",
        "PeopleMaritalStatus": "Available",
        "PeopleNationality": "Cambodia",
        "PeopleBirthLocationLevel1": "Battambong",
        "PeopleProfilePhoto": "profile.png",
        "PeopleProfileSummary": "I am 23 year old. I finish ...",
        "PeopleAchievement": "I finish ...",
        "CompositeAccessPatterns":"",
        "Children":{
            "ComputerApplication":[
                {
                    "ComputerApplicationName": "Microsoft Excel",
                    "ComputerApplicationLevel": "Intermediate"
                }
            ],
            "CoreCompetency":[
                {
                    "CoreCompetencyCompetency": "Use Computer"
                }
            ],
            "Document":[
                {
                    "DocumentName": "High School Certificate",
                    "DocumentFileName": "UUID"
                     
                }
            ],
            "Contact":[
                {
                    "ContactName": "Putheara",
                    "ContactValue": "putheara.pen@gmail.com"
                }
            ],
             "Language":[
                {
                    "LanguageLanguage": "English",
                    "LanguageSkill": "Speaking, Writing, Listening, Reading", 
                    "LanguageProficiencyLevel": "Professional Working Proficiency, Limited Working Proficiency" 
                }
            ]
        }
    }
}
```

### HTTP Request

`PUT https://dev.aimlapps.com/people-svc/api/v1/people/People:b03bb96458a86f867e6324ecd1c8133d`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the People. Ex : People:b03bb96458a86f867e6324ecd1c8133d

## Retrieve People
> The above command returns JSON structured like this:

```json
{
    "People": [
        {
            "PeopleCoreCompetency": {
                "L": [
                    {
                        "M": {
                            "CoreCompetencyCompetency": {
                                "S": "Use Computer"
                            }
                        }
                    }
                ]
            },
            "PeopleNationality": {
                "S": "Cambodia"
            },
            "CompositeAccessPatterns": {
                "S": "People#PeopleFirstName:Dalin#PeopleMiddleName:Lin#PeopleLastName:Luon"
            },
            "PeopleContact": {
                "L": [
                    {
                        "M": {
                            "ContactName": {
                                "S": "Putheara"
                            },
                            "ContactValue": {
                                "S": "putheara.pen@gmail.com"
                            }
                        }
                    }
                ]
            },
            "PeopleDocument": {
                "L": [
                    {
                        "M": {
                            "DocumentFileName": {
                                "S": "UUID"
                            },
                            "DocumentName": {
                                "S": "High School Certificate"
                            }
                        }
                    }
                ]
            },
            "PeopleBirthLocationLevel1": {
                "S": "Battambong"
            },
            "PeopleBirthDate": {
                "S": "04-02-1998"
            },
            "PeopleAchievement": {
                "S": "I finish ..."
            },
            "PeopleLanguage": {
                "L": [
                    {
                        "M": {
                            "LanguageLanguage": {
                                "S": "English"
                            },
                            "LanguageProficiencyLevel": {
                                "S": "Professional Working Proficiency, Limited Working Proficiency"
                            },
                            "LanguageSkill": {
                                "S": "Speaking, Writing, Listening, Reading"
                            }
                        }
                    }
                ]
            },
            "PeopleProfilePhoto": {
                "S": "profile.png"
            },
            "EntityItemId": {
                "S": "People:b03bb96458a86f867e6324ecd1c8133d"
            },
            "PeopleFirstName": {
                "S": "Dalin"
            },
            "PeopleMiddleName": {
                "S": "Lin"
            },
            "PeopleLastName": {
                "S": "Luon"
            },
            "PeopleComputerApplication": {
                "L": [
                    {
                        "M": {
                            "ComputerApplicationName": {
                                "S": "Microsoft Excel"
                            },
                            "ComputerApplicationLevel": {
                                "S": "Intermediate"
                            }
                        }
                    }
                ]
            },
            "PeopleGender": {
                "S": "F"
            },
            "PeopleMaritalStatus": {
                "S": "Available"
            },
            "TenantId": {
                "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
            },
            "PeopleProfileSummary": {
                "S": "I am 23 year old. I finish ..."
            }
        }
    ],
    "FilterAttributes": [
        {
            "PeopleFirstName": "First Name"
        },
        {
            "PeopleMiddleName": "Middle Name"
        },
        {
            "PeopleLastName": "Last Name"
        }
    ]
}
```

This endpoint retrieves all People.

### HTTP Request

`GET https://dev.aimlapps.com/people-svc/api/v1/job-orders`

## View Detail People
> The above command returns JSON structured like this:

```json
{
    "PeopleCoreCompetency": {
        "L": [
            {
                "M": {
                    "CoreCompetencyCompetency": {
                        "S": "Use Computer"
                    }
                }
            }
        ]
    },
    "PeopleNationality": {
        "S": "Cambodia"
    },
    "CompositeAccessPatterns": {
        "S": "People#PeopleFirstName:Dalin#PeopleMiddleName:Lin#PeopleLastName:Luon"
    },
    "PeopleContact": {
        "L": [
            {
                "M": {
                    "ContactName": {
                        "S": "Putheara"
                    },
                    "ContactValue": {
                        "S": "putheara.pen@gmail.com"
                    }
                }
            }
        ]
    },
    "PeopleDocument": {
        "L": [
            {
                "M": {
                    "DocumentFileName": {
                        "S": "UUID"
                    },
                    "DocumentName": {
                        "S": "High School Certificate"
                    }
                }
            }
        ]
    },
    "PeopleBirthLocationLevel1": {
        "S": "Battambong"
    },
    "PeopleBirthDate": {
        "S": "04-02-1998"
    },
    "PeopleAchievement": {
        "S": "I finish ..."
    },
    "PeopleLanguage": {
        "L": [
            {
                "M": {
                    "LanguageLanguage": {
                        "S": "English"
                    },
                    "LanguageProficiencyLevel": {
                        "S": "Professional Working Proficiency, Limited Working Proficiency"
                    },
                    "LanguageSkill": {
                        "S": "Speaking, Writing, Listening, Reading"
                    }
                }
            }
        ]
    },
    "PeopleProfilePhoto": {
        "S": "profile.png"
    },
    "EntityItemId": {
        "S": "People:b03bb96458a86f867e6324ecd1c8133d"
    },
    "PeopleFirstName": {
        "S": "Dalin"
    },
    "PeopleMiddleName": {
        "S": "Lin"
    },
    "PeopleLastName": {
        "S": "Luon"
    },
    "PeopleComputerApplication": {
        "L": [
            {
                "M": {
                    "ComputerApplicationName": {
                        "S": "Microsoft Excel"
                    },
                    "ComputerApplicationLevel": {
                        "S": "Intermediate"
                    }
                }
            }
        ]
    },
    "PeopleGender": {
        "S": "F"
    },
    "PeopleMaritalStatus": {
        "S": "Available"
    },
    "TenantId": {
        "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
    },
    "PeopleProfileSummary": {
        "S": "I am 23 year old. I finish ..."
    }
}
```

This endpoint view detail People.

### HTTP Request

`GET https://dev.aimlapps.com/people-svc/api/v1/people/People:b03bb96458a86f867e6324ecd1c8133d`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the People. Ex : People:b03bb96458a86f867e6324ecd1c8133d

## Delete People

This endpoint delete a specific People.

### HTTP Request

`DELETE https://dev.aimlapps.com/people-svc/api/v1/people/People:b03bb96458a86f867e6324ecd1c8133d`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the People to delete. Ex : People:b03bb96458a86f867e6324ecd1c8133d

