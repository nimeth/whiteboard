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
### 1.Reqest Body
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
        "PeopleCreatedByUserId":"User:b03bb96458a86f867e6324ecd1c8133d",
        "PeopleCreatedDateTime":"02-03-2021",
        "PeopleUpdatedByUserId":"User:b03bb96458a86f867e6324ecd1c8133d",
        "PeopleUpdatedDateTime":"02-03-2021",
        "CompositeAccessPatterns":"",
        "Children":{
            "ComputerLiterace":[
                {
                    "ComputerLiteraceApplication": "Microsoft Excel",
                    "ComputerLiteracePracticalLevel": "Intermediate"
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

### 2.HTTP Response
```json
{
    "PeopleCreatedDateTime": {
        "S": "02-03-2021"
    },
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
        "S": "People#PeopleFirstName:Ratha#PeopleMiddleName:Ratha#PeopleLastName:Chan"
    },
    "PeopleContact": {
        "L": [
            {
                "M": {
                    "ContactName": {
                        "S": "Nita"
                    },
                    "ContactValue": {
                        "S": "Nita.pen@gmail.com"
                    }
                }
            }
        ]
    },
    "PeopleUpdatedDateTime": {
        "S": "02-03-2021"
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
        "S": "Bontay mean jey"
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
        "S": "People:5a47e4140b04a7be24774629bbcfc855"
    },
    "PeopleUpdatedByUserId": {
        "S": "User:b03bb96458a86f867e6324ecd1c8133d"
    },
    "PeopleFirstName": {
        "S": "Ratha"
    },
    "PeopleMiddleName": {
        "S": "Ratha"
    },
    "PeopleLastName": {
        "S": "Chan"
    },
    "PeopleCreatedByUserId": {
        "S": "User:b03bb96458a86f867e6324ecd1c8133d"
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
    "PeopleComputerLiterace": {
        "L": [
            {
                "M": {
                    "ComputerLiteracePracticalLevel": {
                        "S": "Advance"
                    },
                    "ComputerLiteraceApplication": {
                        "S": "Microsoft Excel"
                    }
                }
            }
        ]
    },
    "PeopleProfileSummary": {
        "S": "I am 23 year old. I finish ..."
    }
}
```

### 3.HTTP Request

`POST https://dev.aimlapps.com/people-svc/api/v1/people`

## Retrieve People
### 1.HTTP Response
>HTTP Response returns JSON structured like this:

```json
{
    "People": [
        {
            "PeopleCreatedDateTime": {
                "S": "02-03-2021"
            },
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
                "S": "People#PeopleFirstName:Ratha#PeopleMiddleName:Ratha#PeopleLastName:Chan"
            },
            "PeopleContact": {
                "L": [
                    {
                        "M": {
                            "ContactName": {
                                "S": "Nita"
                            },
                            "ContactValue": {
                                "S": "Nita.pen@gmail.com"
                            }
                        }
                    }
                ]
            },
            "PeopleUpdatedDateTime": {
                "S": "02-03-2021"
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
                "S": "Bontay mean jey"
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
                "S": "People:5a47e4140b04a7be24774629bbcfc855"
            },
            "PeopleUpdatedByUserId": {
                "S": "User:b03bb96458a86f867e6324ecd1c8133d"
            },
            "PeopleFirstName": {
                "S": "Ratha"
            },
            "PeopleMiddleName": {
                "S": "Ratha"
            },
            "PeopleLastName": {
                "S": "Chan"
            },
            "PeopleCreatedByUserId": {
                "S": "User:b03bb96458a86f867e6324ecd1c8133d"
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
            "PeopleComputerLiterace": {
                "L": [
                    {
                        "M": {
                            "ComputerLiteracePracticalLevel": {
                                "S": "Advance"
                            },
                            "ComputerLiteraceApplication": {
                                "S": "Microsoft Excel"
                            }
                        }
                    }
                ]
            },
            "PeopleProfileSummary": {
                "S": "I am 23 year old. I finish ..."
            }
        },
        {
            "PeopleCreatedDateTime": {
                "S": "02-03-2021"
            },
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
                "S": "People#PeopleFirstName:Son#PeopleMiddleName:Son#PeopleLastName:Hom"
            },
            "PeopleContact": {
                "L": [
                    {
                        "M": {
                            "ContactName": {
                                "S": "Nita"
                            },
                            "ContactValue": {
                                "S": "Nita.pen@gmail.com"
                            }
                        }
                    }
                ]
            },
            "PeopleUpdatedDateTime": {
                "S": "02-03-2021"
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
                "S": "Siem Reap"
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
                "S": "People:648311551b2f33a84d95f87ca878e6e5"
            },
            "PeopleUpdatedByUserId": {
                "S": "User:b03bb96458a86f867e6324ecd1c8133d"
            },
            "PeopleFirstName": {
                "S": "Son"
            },
            "PeopleMiddleName": {
                "S": "Son"
            },
            "PeopleLastName": {
                "S": "Hom"
            },
            "PeopleCreatedByUserId": {
                "S": "User:b03bb96458a86f867e6324ecd1c8133d"
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
            "PeopleComputerLiterace": {
                "L": [
                    {
                        "M": {
                            "ComputerLiteracePracticalLevel": {
                                "S": "Advance"
                            },
                            "ComputerLiteraceApplication": {
                                "S": "Microsoft Excel"
                            }
                        }
                    }
                ]
            },
            "PeopleProfileSummary": {
                "S": "I am 23 year old. I finish ..."
            }
        },
        {
            "PeopleCreatedDateTime": {
                "S": "02-03-2021"
            },
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
                "S": "People#PeopleFirstName:SreyTa#PeopleMiddleName:Ta#PeopleLastName:Sen"
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
            "PeopleUpdatedDateTime": {
                "S": "02-03-2021"
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
                "S": "Siem Reap"
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
                "S": "People:fa4a8b984a7ab3a99bdf74ae00d24fa8"
            },
            "PeopleUpdatedByUserId": {
                "S": "User:b03bb96458a86f867e6324ecd1c8133d"
            },
            "PeopleFirstName": {
                "S": "SreyTa"
            },
            "PeopleMiddleName": {
                "S": "Ta"
            },
            "PeopleLastName": {
                "S": "Sen"
            },
            "PeopleCreatedByUserId": {
                "S": "User:b03bb96458a86f867e6324ecd1c8133d"
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
            "PeopleComputerLiterace": {
                "L": [
                    {
                        "M": {
                            "ComputerLiteracePracticalLevel": {
                                "S": "Intermediate"
                            },
                            "ComputerLiteraceApplication": {
                                "S": "Microsoft Excel"
                            }
                        }
                    }
                ]
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

This endpoint List all People.

### 2.HTTP Request

`GET https://dev.aimlapps.com/people-svc/api/v1/people`

## Update People
### 1.Request Body
>Request Body submit JSON structured like this:

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
        "PeopleCreatedByUserId":"User:b03bb96458a86f867e6324ecd1c8133d",
        "PeopleCreatedDateTime":"02-03-2021",
        "PeopleUpdatedByUserId":"User:b03bb96458a86f867e6324ecd1c8133d",
        "PeopleUpdatedDateTime":"02-03-2021",
        "CompositeAccessPatterns":"",
        "Children":{
            "ComputerLiterace":[
                {
                    "ComputerLiteraceApplication": "Microsoft Excel",
                    "ComputerLiteracePracticalLevel": "Intermediate"
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
### 2.HTTP Response

```json
{
    "PeopleCreatedDateTime": {
        "S": "02-03-2021"
    },
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
        "S": "People#PeopleFirstName:Ratha#PeopleMiddleName:Ratha#PeopleLastName:Chan"
    },
    "PeopleContact": {
        "L": [
            {
                "M": {
                    "ContactName": {
                        "S": "Nita"
                    },
                    "ContactValue": {
                        "S": "Nita.pen@gmail.com"
                    }
                }
            }
        ]
    },
    "PeopleUpdatedDateTime": {
        "S": "02-03-2021"
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
        "S": "Bontay mean jey"
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
        "S": "People:5a47e4140b04a7be24774629bbcfc855"
    },
    "PeopleUpdatedByUserId": {
        "S": "User:b03bb96458a86f867e6324ecd1c8133d"
    },
    "PeopleFirstName": {
        "S": "Ratha"
    },
    "PeopleMiddleName": {
        "S": "Ratha"
    },
    "PeopleLastName": {
        "S": "Chan"
    },
    "PeopleCreatedByUserId": {
        "S": "User:b03bb96458a86f867e6324ecd1c8133d"
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
    "PeopleComputerLiterace": {
        "L": [
            {
                "M": {
                    "ComputerLiteracePracticalLevel": {
                        "S": "Advance"
                    },
                    "ComputerLiteraceApplication": {
                        "S": "Microsoft Excel"
                    }
                }
            }
        ]
    },
    "PeopleProfileSummary": {
        "S": "I am 23 year old. I finish ..."
    }
}
```

### 3.HTTP Request

`PUT https://dev.aimlapps.com/people-svc/api/v1/people/ID`

### 4.URL Parameters

Parameter | Description
--------- | -----------
ID      | The ID of the People. 
          | Ex : People:999ea2a64c7a26db46da69dcf1ba92fe

## View Detail People
### 1.HTTP Response
> HTTP Response returns JSON structured like this:

```json
{
    "PeopleCreatedDateTime": {
        "S": "02-03-2021"
    },
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
        "S": "People#PeopleFirstName:Ratha#PeopleMiddleName:Ratha#PeopleLastName:Chan"
    },
    "PeopleContact": {
        "L": [
            {
                "M": {
                    "ContactName": {
                        "S": "Nita"
                    },
                    "ContactValue": {
                        "S": "Nita.pen@gmail.com"
                    }
                }
            }
        ]
    },
    "PeopleUpdatedDateTime": {
        "S": "02-03-2021"
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
        "S": "Bontay mean jey"
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
        "S": "People:5a47e4140b04a7be24774629bbcfc855"
    },
    "PeopleUpdatedByUserId": {
        "S": "User:b03bb96458a86f867e6324ecd1c8133d"
    },
    "PeopleFirstName": {
        "S": "Ratha"
    },
    "PeopleMiddleName": {
        "S": "Ratha"
    },
    "PeopleLastName": {
        "S": "Chan"
    },
    "PeopleCreatedByUserId": {
        "S": "User:b03bb96458a86f867e6324ecd1c8133d"
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
    "PeopleComputerLiterace": {
        "L": [
            {
                "M": {
                    "ComputerLiteracePracticalLevel": {
                        "S": "Advance"
                    },
                    "ComputerLiteraceApplication": {
                        "S": "Microsoft Excel"
                    }
                }
            }
        ]
    },
    "PeopleProfileSummary": {
        "S": "I am 23 year old. I finish ..."
    }
}
```

This endpoint view detail People.

### 2.HTTP Request

`GET https://dev.aimlapps.com/people-svc/api/v1/people/ID`

### 3.URL Parameters

Parameter | Description
--------- | -----------
ID      | The ID of the People.
          | Ex : People:999ea2a64c7a26db46da69dcf1ba92fe

## Delete People

This endpoint delete a specific People.

### 1.HTTP Request

`DELETE https://dev.aimlapps.com/people-svc/api/v1/people/ID`

### 2.URL Parameters

Parameter | Description
--------- | -----------
ID        | The ID of the People to delete. 
          | Ex : People:999ea2a64c7a26db46da69dcf1ba92fe

# People Comment
## Create People Comment
### 1.Request Body
> Request Body submit JSON structured like this:

```json
{
    "PeopleComment": {
        "PeopleCommentPeopleId": "People:5a47e4140b04a7be24774629bbcfc855",
        "PeopleComment": "He want to apply Web Developer",
        "PeopleCommentAddedByUserId":"User:b03bb96458a86f867e6324ecd1c8133d",
        "PeopleCommentAddedDateTime":"02-03-2021",
        "PeopleCommentUpdatedByUserId":"User:b03bb96458a86f867e6324ecd1c8133d",
        "PeopleCommentUpdatedDateTime":"02-03-2021",
        "CompositeAccessPatterns":""
        
    }
}
```
### 2.HTTP Response

```json
{
    "EntityItemId": {
        "S": "PeopleComment:58a425cc6be0d8cada40a7ac001606e9"
    },
    "CompositeAccessPatterns": {
        "S": "PeopleComment#PeopleCommentPeopleId:People:5a47e4140b04a7be24774629bbcfc855"
    },
    "PeopleCommentPeopleId": {
        "S": "People:5a47e4140b04a7be24774629bbcfc855"
    },
    "TenantId": {
        "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
    },
    "PeopleComment": {
        "S": "He want to apply Web Developer"
    },
    "PeopleCommentAddedDateTime": {
        "S": "02-03-2021"
    },
    "PeopleCommentUpdatedDateTime": {
        "S": "02-03-2021"
    },
    "PeopleCommentUpdatedByUserId": {
        "S": "User:b03bb96458a86f867e6324ecd1c8133d"
    },
    "PeopleCommentAddedByUserId": {
        "S": "User:b03bb96458a86f867e6324ecd1c8133d"
    }
}
```

### 3.HTTP Request

`POST https://dev.aimlapps.com/people-svc/api/v1/people/<people_id>/comments`

### 4.URL paramater

Parameter   | Description
---------   | -----------
people_id   | The Id of the People.
            | Ex : People:999ea2a64c7a26db46da69dcf1ba92fe

## Update People Comment
### 1.Request Body
> The above command when submit JSON structured like this:

```json
{
    "PeopleComment": {
        "PeopleCommentPeopleId": "People:5a47e4140b04a7be24774629bbcfc855",
        "PeopleComment": "He want to apply Web Developer",
        "PeopleCommentAddedByUserId":"User:b03bb96458a86f867e6324ecd1c8133d",
        "PeopleCommentAddedDateTime":"02-03-2021",
        "PeopleCommentUpdatedByUserId":"User:b03bb96458a86f867e6324ecd1c8133d",
        "PeopleCommentUpdatedDateTime":"02-03-2021",
        "CompositeAccessPatterns":""
        
    }
}
```
### 2.HTTP Response

```json
{
    "EntityItemId": {
        "S": "PeopleComment:58a425cc6be0d8cada40a7ac001606e9"
    },
    "CompositeAccessPatterns": {
        "S": "PeopleComment#PeopleCommentPeopleId:People:5a47e4140b04a7be24774629bbcfc855"
    },
    "PeopleCommentPeopleId": {
        "S": "People:5a47e4140b04a7be24774629bbcfc855"
    },
    "TenantId": {
        "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
    },
    "PeopleComment": {
        "S": "He want to apply Web Developer"
    },
    "PeopleCommentAddedDateTime": {
        "S": "02-03-2021"
    },
    "PeopleCommentUpdatedDateTime": {
        "S": "02-03-2021"
    },
    "PeopleCommentUpdatedByUserId": {
        "S": "User:b03bb96458a86f867e6324ecd1c8133d"
    },
    "PeopleCommentAddedByUserId": {
        "S": "User:b03bb96458a86f867e6324ecd1c8133d"
    }
}
```

### 3.HTTP Request

`PUT https://dev.aimlapps.com/people-svc/api/v1/people/<people_id>/comments/ID`

### 4.URL Parameters
Parameter   | Description
---------   | -----------
people_id   | The Id of the People.
            | Ex : People:999ea2a64c7a26db46da69dcf1ba92fe
ID          | The Id of the People Comment.
            | Ex : PeopleComment:ba452ece82e9d2caf8014816ac580251

## Retrieve People Comment
### 1.HTTP Response
> HTTP Response returns JSON structured like this:

```json
{
    "PeopleComment": [
        {
            "EntityItemId": {
                "S": "PeopleComment:091ae479804f40941c88e384db0a3ffe"
            },
            "CompositeAccessPatterns": {
                "S": "PeopleComment#PeopleCommentPeopleId:People:5a47e4140b04a7be24774629bbcfc855"
            },
            "PeopleCommentPeopleId": {
                "S": "People:5a47e4140b04a7be24774629bbcfc855"
            },
            "TenantId": {
                "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
            },
            "PeopleComment": {
                "S": "He want to apply Web Developer"
            },
            "PeopleCommentAddedDateTime": {
                "S": "02-03-2021"
            },
            "PeopleCommentUpdatedDateTime": {
                "S": "02-03-2021"
            },
            "PeopleCommentUpdatedByUserId": {
                "S": "User:b03bb96458a86f867e6324ecd1c8133d"
            },
            "PeopleCommentAddedByUserId": {
                "S": "User:b03bb96458a86f867e6324ecd1c8133d"
            }
        },
        {
            "EntityItemId": {
                "S": "PeopleComment:32a4cd69511f6220f93d29ef82b9b6c1"
            },
            "CompositeAccessPatterns": {
                "S": "PeopleComment#PeopleCommentPeopleId:People:5a47e4140b04a7be24774629bbcfc855"
            },
            "PeopleCommentPeopleId": {
                "S": "People:5a47e4140b04a7be24774629bbcfc855"
            },
            "TenantId": {
                "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
            },
            "PeopleComment": {
                "S": "He want to apply Web Developer"
            },
            "PeopleCommentAddedDateTime": {
                "S": "02-03-2021"
            },
            "PeopleCommentUpdatedDateTime": {
                "S": "02-03-2021"
            },
            "PeopleCommentUpdatedByUserId": {
                "S": "User:b03bb96458a86f867e6324ecd1c8133d"
            },
            "PeopleCommentAddedByUserId": {
                "S": "User:b03bb96458a86f867e6324ecd1c8133d"
            }
        }
    ],
    "FilterAttributes": [
        {
            "PeopleCommentPeopleId": "People Id"
        }
    ]
}
```

This endpoint retrieve People Comment.

### 2.HTTP Request

`GET https://dev.aimlapps.com/people-svc/api/v1/people/<people_id>/comments/`

### 3.URL Parameters
Parameter   | Description
---------   | -----------
<People_id> | The Id of the People.
            | Ex : People:999ea2a64c7a26db46da69dcf1ba92fe

## View Detail People Comment
### 1.HTTP Response
> The above command returns JSON structured like this:

```json
{
    "EntityItemId": {
        "S": "PeopleComment:58a425cc6be0d8cada40a7ac001606e9"
    },
    "CompositeAccessPatterns": {
        "S": "PeopleComment#PeopleCommentPeopleId:People:5a47e4140b04a7be24774629bbcfc855"
    },
    "PeopleCommentPeopleId": {
        "S": "People:5a47e4140b04a7be24774629bbcfc855"
    },
    "TenantId": {
        "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
    },
    "PeopleComment": {
        "S": "He want to apply Web Developer"
    },
    "PeopleCommentAddedDateTime": {
        "S": "02-03-2021"
    },
    "PeopleCommentUpdatedDateTime": {
        "S": "02-03-2021"
    },
    "PeopleCommentUpdatedByUserId": {
        "S": "User:b03bb96458a86f867e6324ecd1c8133d"
    },
    "PeopleCommentAddedByUserId": {
        "S": "User:b03bb96458a86f867e6324ecd1c8133d"
    }
}
```

This endpoint view detail People Comment.

### 2.HTTP Request

`GET https://dev.aimlapps.com/people-svc/api/v1/people/<People_id>/comments/ID`

### 3.URL Parameters

Parameter   | Description
---------   | -----------
<People_id> | The ID of the People.
            | Ex : People:999ea2a64c7a26db46da69dcf1ba92fe
ID          | The ID of the People Comment.
            | Ex : PeopleComment:ba452ece82e9d2caf8014816ac580251

## Delete People Comment

This endpoint delete a specific People Comment.

### 1.HTTP Request

`DELETE https://dev.aimlapps.com/people-svc/api/v1/people/<people_id>/comments/ID`

### 2.URL Parameters

Parameter   | Description
---------   | -----------
people_id   | The ID of the People. Ex : People:999ea2a64c7a26db46da69dcf1ba92fe
ID          | The ID of the People Comment. Ex : PeopleComment:ba452ece82e9d2caf8014816ac580251


# People Education
## Create People Education
### 1.Body Request
> Request JSON structured like this:

```json
{
    "PeopleEducation": {
        "PeopleEducationPeopleId": "People:648311551b2f33a84d95f87ca878e6e5",
        "PeopleEducationDateFrom": "2020-12-12", 
        "PeopleEducationDateTo": "2020-12-12", 
        "PeopleEducationAchievement": "Bachelor Degree", 
        "PeopleEducationRemark": "I finish Bachelor Degree of IT programming",
        "PeopleEducationLevel": "Senoir", 
        "PeopleEducationStudyField": "Web Developer", 
        "PeopleEducationStudyMajor": "IT",
        "Children":{
            "School":{
                "OrganizationId":"OrganizationName:e05d7f46e40731dd0ae0760543eb5596",
                "OrganizationName": "ODI Asia Co., Ltd.",
                "OrganizationShortName": "ODI"
            }
        }
    }   
}
```


### 2.HTTP Response
>Response Json structured like this:

```json
{
    "EntityItemId": {
        "S": "PeopleEducation:5802c607335d3b513d9ead8066e62e7a"
    },
    "PeopleEducationDateFrom": {
        "S": "2020-12-12"
    },
    "CompositeAccessPatterns": {
        "S": "PeopleEducation#PeopleEducationDateFrom:2020-12-12#PeopleEducationDateTo:2020-12-12#PeopleEducationLevel:Senoir#PeopleEducationStudyField:Web Developer#PeopleEducationStudyMajor:IT"
    },
    "PeopleEducationDateTo": {
        "S": "2020-12-12"
    },
    "PeopleEducationRemark": {
        "S": "I finish Bachelor Degree of IT programming"
    },
    "PeopleEducationStudyField": {
        "S": "Web Developer"
    },
    "PeopleEducationStudyMajor": {
        "S": "IT"
    },
    "TenantId": {
        "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
    },
    "PeopleEducationSchool": {
        "M": {
            "OrganizationName": {
                "S": "ODI Asia Co., Ltd."
            },
            "OrganizationShortName": {
                "S": "ODI"
            },
            "OrganizationId": {
                "S": "OrganizationName:e05d7f46e40731dd0ae0760543eb5596"
            }
        }
    },
    "PeopleEducationLevel": {
        "S": "Senoir"
    },
    "PeopleEducationPeopleId": {
        "S": "People:648311551b2f33a84d95f87ca878e6e5"
    },
    "PeopleEducationAchievement": {
        "S": "Bachelor Degree"
    }
}
```

### 3.HTTP Request

`POST https://dev.aimlapps.com/people-svc/api/v1/people-educations`

## Update People Education
### 1.Body Request
> Request JSON structured like this:

```json
{
    "PeopleEducation": {
        "PeopleEducationPeopleId": "People:648311551b2f33a84d95f87ca878e6e5",
        "PeopleEducationDateFrom": "2020-12-12", 
        "PeopleEducationDateTo": "2020-12-12", 
        "PeopleEducationAchievement": "Bachelor Degree", 
        "PeopleEducationRemark": "I finish Bachelor Degree of IT programming",
        "PeopleEducationLevel": "Manager", 
        "PeopleEducationStudyField": "Web Developer", 
        "PeopleEducationStudyMajor": "IT",
        "Children":{
            "School":{
                "OrganizationId":"OrganizationName:e05d7f46e40731dd0ae0760543eb5596",
                "OrganizationName": "ODI Asia Co., Ltd.",
                "OrganizationShortName": "ODI"
            }
        }
    }   
}
```
### 2.HTTP Response
>Response Json structured like this:

```json
{
    "EntityItemId": {
        "S": "PeopleEducation:5802c607335d3b513d9ead8066e62e7a"
    },
    "PeopleEducationDateFrom": {
        "S": "2020-12-12"
    },
    "CompositeAccessPatterns": {
        "S": "PeopleEducation#PeopleEducationDateFrom:2020-12-12#PeopleEducationDateTo:2020-12-12#PeopleEducationLevel:Senoir#PeopleEducationStudyField:Web Developer#PeopleEducationStudyMajor:IT"
    },
    "PeopleEducationDateTo": {
        "S": "2020-12-12"
    },
    "PeopleEducationRemark": {
        "S": "I finish Bachelor Degree of IT programming"
    },
    "PeopleEducationStudyField": {
        "S": "Web Developer"
    },
    "PeopleEducationStudyMajor": {
        "S": "IT"
    },
    "TenantId": {
        "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
    },
    "PeopleEducationSchool": {
        "M": {
            "OrganizationName": {
                "S": "ODI Asia Co., Ltd."
            },
            "OrganizationShortName": {
                "S": "ODI"
            },
            "OrganizationId": {
                "S": "OrganizationName:e05d7f46e40731dd0ae0760543eb5596"
            }
        }
    },
    "PeopleEducationLevel": {
        "S": "Manager"
    },
    "PeopleEducationPeopleId": {
        "S": "People:648311551b2f33a84d95f87ca878e6e5"
    },
    "PeopleEducationAchievement": {
        "S": "Bachelor Degree"
    }
}
```


### 3.HTTP Request

`PUT https://dev.aimlapps.com/people-svc/api/v1/people-educations/ID`

### 4.URL Parameters

Parameter | Description
--------- | -----------
ID        | The Id of the People Education that use for update.
          | Ex : PeopleEducation:5802c607335d3b513d9ead8066e62e7a

## Get People Education
### 1.HTTP Response
> HTTP response returns JSON structured like this:

```json
{
    "ClientProfile": [
        {
            "EntityItemId": {
                "S": "PeopleEducation:5802c607335d3b513d9ead8066e62e7a"
            },
            "CompositeAccessPatterns": {
                "S": "PeopleEducation#PeopleEducationDateFrom:2020-12-12#PeopleEducationDateTo:2020-12-12#PeopleEducationLevel:Manager#PeopleEducationStudyField:Web Developer#PeopleEducationStudyMajor:IT"
            },
            "PeopleEducationDateFrom": {
                "S": "2020-12-12"
            },
            "PeopleEducationDateTo": {
                "S": "2020-12-12"
            },
            "PeopleEducationRemark": {
                "S": "I finish Bachelor Degree of IT programming"
            },
            "PeopleEducationStudyField": {
                "S": "Web Developer"
            },
            "PeopleEducationStudyMajor": {
                "S": "IT"
            },
            "TenantId": {
                "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
            },
            "PeopleEducationSchool": {
                "M": {
                    "OrganizationName": {
                        "S": "ODI Asia Co., Ltd."
                    },
                    "OrganizationShortName": {
                        "S": "ODI"
                    },
                    "OrganizationId": {
                        "S": "OrganizationName:e05d7f46e40731dd0ae0760543eb5596"
                    }
                }
            },
            "PeopleEducationLevel": {
                "S": "Manager"
            },
            "PeopleEducationPeopleId": {
                "S": "People:648311551b2f33a84d95f87ca878e6e5"
            },
            "PeopleEducationAchievement": {
                "S": "Bachelor Degree"
            }
        },
        {
            "EntityItemId": {
                "S": "PeopleEducation:c0ab654905d96c1f39c4d9917dd32572"
            },
            "PeopleEducationDateFrom": {
                "S": "2020-12-12"
            },
            "CompositeAccessPatterns": {
                "S": "PeopleEducation#PeopleEducationDateFrom:2020-12-12#PeopleEducationDateTo:2020-12-12#PeopleEducationLevel:Manager#PeopleEducationStudyField:Network#PeopleEducationStudyMajor:IT"
            },
            "PeopleEducationDateTo": {
                "S": "2020-12-12"
            },
            "PeopleEducationRemark": {
                "S": "I finish Bachelor Degree of IT Network"
            },
            "PeopleEducationStudyField": {
                "S": "Network"
            },
            "PeopleEducationStudyMajor": {
                "S": "IT"
            },
            "TenantId": {
                "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
            },
            "PeopleEducationSchool": {
                "M": {
                    "OrganizationName": {
                        "S": "ODI Asia Co., Ltd."
                    },
                    "OrganizationShortName": {
                        "S": "ODI"
                    },
                    "OrganizationId": {
                        "S": "OrganizationName:e05d7f46e40731dd0ae0760543eb5596"
                    }
                }
            },
            "PeopleEducationLevel": {
                "S": "Manager"
            },
            "PeopleEducationPeopleId": {
                "S": "People:648311551b2f33a84d95f87ca878e6e5"
            },
            "PeopleEducationAchievement": {
                "S": "Bachelor Degree"
            }
        }
    ],
    "FilterAttributes": [
        {
            "PeopleEducationDateFrom": "Education From Date"
        },
        {
            "PeopleEducationDateTo": "Education To Date"
        },
        {
            "PeopleEducationLevel": "Education Level"
        },
        {
            "PeopleEducationStudyField": "Study Field"
        },
        {
            "PeopleEducationStudyMajor": "Study Major"
        }
    ]
}
```

This endpoint retrieves all People Educations.

### 2.HTTP Request

`GET https://dev.aimlapps.com/people-svc/api/v1/people-educations`


## View People Education

### 1.HTTP Response
> The above command returns JSON structured like this:

```json
{
    "EntityItemId": {
        "S": "PeopleEducation:5802c607335d3b513d9ead8066e62e7a"
    },
    "CompositeAccessPatterns": {
        "S": "PeopleEducation#PeopleEducationDateFrom:2020-12-12#PeopleEducationDateTo:2020-12-12#PeopleEducationLevel:Manager#PeopleEducationStudyField:Web Developer#PeopleEducationStudyMajor:IT"
    },
    "PeopleEducationDateFrom": {
        "S": "2020-12-12"
    },
    "PeopleEducationDateTo": {
        "S": "2020-12-12"
    },
    "PeopleEducationRemark": {
        "S": "I finish Bachelor Degree of IT programming"
    },
    "PeopleEducationStudyField": {
        "S": "Web Developer"
    },
    "PeopleEducationStudyMajor": {
        "S": "IT"
    },
    "TenantId": {
        "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
    },
    "PeopleEducationSchool": {
        "M": {
            "OrganizationName": {
                "S": "ODI Asia Co., Ltd."
            },
            "OrganizationShortName": {
                "S": "ODI"
            },
            "OrganizationId": {
                "S": "OrganizationName:e05d7f46e40731dd0ae0760543eb5596"
            }
        }
    },
    "PeopleEducationLevel": {
        "S": "Manager"
    },
    "PeopleEducationPeopleId": {
        "S": "People:648311551b2f33a84d95f87ca878e6e5"
    },
    "PeopleEducationAchievement": {
        "S": "Bachelor Degree"
    }
}
```

This endpoint retrieves a specific People Education.

### 2.HTTP Request

`GET https://dev.aimlapps.com/people-svc/api/v1/people-educations/ID`

### 3.URL Parameters

Parameter | Description
--------- | -----------
ID        | The Id of the People Education that use for view datail.
          | Ex : PeopleEducation:5802c607335d3b513d9ead8066e62e7a


## Delete People Education
This endpoint delete a specific People Education.

### 1.HTTP Request

`DELETE https://dev.aimlapps.com/people-svc/api/v1/people-educations/ID`

### 2.URL Parameters

Parameter | Description
--------- | -----------
ID        | The Id of the People Education that use for delete.
          | Ex : PeopleEducation:5802c607335d3b513d9ead8066e62e7a

# People Training
## Create People Training
### 1.Body Request
> Request JSON structured like this:

```json
{
    "PeopleTraining": {
        "PeopleTrainingPeopleId": "People:648311551b2f33a84d95f87ca878e6e5",
        "PeopleTrainingDateFrom": "2020-12-12", 
        "PeopleTrainingDateTo": "2020-12-12", 
        "PeopleTrainingAchievement": "Bachelor Degree", 
        "PeopleTrainingRemark": "I finish Bachelor Degree of IT Network",
        "PeopleTrainingLevel": "Manager", 
        "PeopleTrainingCourse": "Network", 
        "PeopleTrainingDuration": "35",
        "Children":{
            "Center":{
                "OrganizationId":"OrganizationName:e05d7f46e40731dd0ae0760543eb5596",
                "OrganizationName": "ODI Asia Co., Ltd.",
                "OrganizationShortName": "ODI"
            },
            "Location":{
                "Country":"Thailand",
                "LocationLevel1Name": "Chiang Mai"
            }
        }
    }   
}
```


### 2.HTTP Response
>Response Json structured like this:

```json
{
    "CompositeAccessPatterns": {
        "S": "PeopleTraining#PeopleTrainingDateFrom:2020-12-12#PeopleTrainingDateTo:2020-12-12#PeopleTrainingCourse:Network#PeopleTrainingDuration:35"
    },
    "PeopleTrainingLocation": {
        "M": {
            "Country": {
                "S": "Thailand"
            },
            "LocationLevel1Name": {
                "S": "Chiang Mai"
            }
        }
    },
    "PeopleTrainingRemark": {
        "S": "I finish Bachelor Degree of IT Network"
    },
    "PeopleTrainingLevel": {
        "S": "Manager"
    },
    "PeopleTrainingDuration": {
        "N": "35"
    },
    "EntityItemId": {
        "S": "PeopleTraining:ca8d95bbc39e8ca6d282880c4510b5c7"
    },
    "PeopleTrainingDateTo": {
        "S": "2020-12-12"
    },
    "PeopleTrainingCenter": {
        "M": {
            "OrganizationName": {
                "S": "ODI Asia Co., Ltd."
            },
            "OrganizationShortName": {
                "S": "ODI"
            },
            "OrganizationId": {
                "S": "OrganizationName:e05d7f46e40731dd0ae0760543eb5596"
            }
        }
    },
    "PeopleTrainingAchievement": {
        "S": "Bachelor Degree"
    },
    "TenantId": {
        "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
    },
    "PeopleTrainingPeopleId": {
        "S": "People:648311551b2f33a84d95f87ca878e6e5"
    },
    "PeopleTrainingCourse": {
        "S": "Network"
    },
    "PeopleTrainingDateFrom": {
        "S": "2020-12-12"
    }
}
```

### 3.HTTP Request

`POST https://dev.aimlapps.com/people-svc/api/v1/people-trainings`

## Update People Training
### 1.Body Request
> Request JSON structured like this:

```json
{
    "PeopleTraining": {
        "PeopleTrainingPeopleId": "People:648311551b2f33a84d95f87ca878e6e5",
        "PeopleTrainingDateFrom": "2020-12-12", 
        "PeopleTrainingDateTo": "2020-12-12", 
        "PeopleTrainingAchievement": "Bachelor Degree", 
        "PeopleTrainingRemark": "I finish Bachelor Degree of IT Network",
        "PeopleTrainingLevel": "Manager", 
        "PeopleTrainingCourse": "Network", 
        "PeopleTrainingDuration": "35",
        "Children":{
            "Center":{
                "OrganizationId":"OrganizationName:e05d7f46e40731dd0ae0760543eb5596",
                "OrganizationName": "ODI Asia Co., Ltd.",
                "OrganizationShortName": "ODI"
            },
            "Location":{
                "Country":"Cambodian",
                "LocationLevel1Name": "Battambong"
            }
        }
    }   
}
```
### 2.HTTP Response
>Response Json structured like this:

```json
{
    "CompositeAccessPatterns": {
        "S": "PeopleTraining#PeopleTrainingDateFrom:2020-12-12#PeopleTrainingDateTo:2020-12-12#PeopleTrainingCourse:Network#PeopleTrainingDuration:35"
    },
    "PeopleTrainingLocation": {
        "M": {
            "Country": {
                "S": "Cambodian"
            },
            "LocationLevel1Name": {
                "S": "Battambong"
            }
        }
    },
    "PeopleTrainingRemark": {
        "S": "I finish Bachelor Degree of IT Network"
    },
    "PeopleTrainingLevel": {
        "S": "Manager"
    },
    "EntityItemId": {
        "S": "PeopleTraining:ca8d95bbc39e8ca6d282880c4510b5c7"
    },
    "PeopleTrainingDuration": {
        "N": "35"
    },
    "PeopleTrainingDateTo": {
        "S": "2020-12-12"
    },
    "PeopleTrainingCenter": {
        "M": {
            "OrganizationName": {
                "S": "ODI Asia Co., Ltd."
            },
            "OrganizationShortName": {
                "S": "ODI"
            },
            "OrganizationId": {
                "S": "OrganizationName:e05d7f46e40731dd0ae0760543eb5596"
            }
        }
    },
    "PeopleTrainingAchievement": {
        "S": "Bachelor Degree"
    },
    "TenantId": {
        "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
    },
    "PeopleTrainingPeopleId": {
        "S": "People:648311551b2f33a84d95f87ca878e6e5"
    },
    "PeopleTrainingCourse": {
        "S": "Network"
    },
    "PeopleTrainingDateFrom": {
        "S": "2020-12-12"
    }
}
```


### 3.HTTP Request

`PUT https://dev.aimlapps.com/people-svc/api/v1/people-trainings/ID`

### 4.URL Parameters

Parameter | Description
--------- | -----------
ID      | The Id of the People Training that use for update.
          | Ex : PeopleTraining:ca8d95bbc39e8ca6d282880c4510b5c7

## Get People Training
### 1.HTTP Response
> HTTP response returns JSON structured like this:

```json
{
    "PeopleTraining": [
        {
            "CompositeAccessPatterns": {
                "S": "PeopleTraining#PeopleTrainingDateFrom:2020-12-12#PeopleTrainingDateTo:2020-12-12#PeopleTrainingCourse:Network#PeopleTrainingDuration:35"
            },
            "PeopleTrainingLocation": {
                "M": {
                    "Country": {
                        "S": "Thailand"
                    },
                    "LocationLevel1Name": {
                        "S": "Chiang Mai"
                    }
                }
            },
            "PeopleTrainingRemark": {
                "S": "I finish Bachelor Degree of IT Network"
            },
            "PeopleTrainingLevel": {
                "S": "Senoir"
            },
            "PeopleTrainingDuration": {
                "N": "35"
            },
            "EntityItemId": {
                "S": "PeopleTraining:299e344654f4f5bc857f9a529dbdfa3b"
            },
            "PeopleTrainingDateTo": {
                "S": "2020-12-12"
            },
            "PeopleTrainingCenter": {
                "M": {
                    "OrganizationName": {
                        "S": "ODI Asia Co., Ltd."
                    },
                    "OrganizationShortName": {
                        "S": "ODI"
                    },
                    "OrganizationId": {
                        "S": "OrganizationName:e05d7f46e40731dd0ae0760543eb5596"
                    }
                }
            },
            "PeopleTrainingAchievement": {
                "S": "Bachelor Degree"
            },
            "TenantId": {
                "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
            },
            "PeopleTrainingPeopleId": {
                "S": "People:648311551b2f33a84d95f87ca878e6e5"
            },
            "PeopleTrainingCourse": {
                "S": "Network"
            },
            "PeopleTrainingDateFrom": {
                "S": "2020-12-12"
            }
        },
        {
            "CompositeAccessPatterns": {
                "S": "PeopleTraining#PeopleTrainingDateFrom:2020-12-12#PeopleTrainingDateTo:2020-12-12#PeopleTrainingCourse:Network#PeopleTrainingDuration:35"
            },
            "PeopleTrainingLocation": {
                "M": {
                    "Country": {
                        "S": "Cambodian"
                    },
                    "LocationLevel1Name": {
                        "S": "Battambong"
                    }
                }
            },
            "PeopleTrainingRemark": {
                "S": "I finish Bachelor Degree of IT Network"
            },
            "PeopleTrainingLevel": {
                "S": "Manager"
            },
            "PeopleTrainingDuration": {
                "N": "35"
            },
            "EntityItemId": {
                "S": "PeopleTraining:ca8d95bbc39e8ca6d282880c4510b5c7"
            },
            "PeopleTrainingDateTo": {
                "S": "2020-12-12"
            },
            "PeopleTrainingCenter": {
                "M": {
                    "OrganizationName": {
                        "S": "ODI Asia Co., Ltd."
                    },
                    "OrganizationShortName": {
                        "S": "ODI"
                    },
                    "OrganizationId": {
                        "S": "OrganizationName:e05d7f46e40731dd0ae0760543eb5596"
                    }
                }
            },
            "PeopleTrainingAchievement": {
                "S": "Bachelor Degree"
            },
            "TenantId": {
                "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
            },
            "PeopleTrainingPeopleId": {
                "S": "People:648311551b2f33a84d95f87ca878e6e5"
            },
            "PeopleTrainingCourse": {
                "S": "Network"
            },
            "PeopleTrainingDateFrom": {
                "S": "2020-12-12"
            }
        }
    ],
    "FilterAttributes": [
        {
            "PeopleTrainingDateFrom": "From Date"
        },
        {
            "PeopleTrainingDateTo": "To Date"
        },
        {
            "PeopleTrainingCourse": "Course"
        },
        {
            "PeopleTrainingDuration": "Duration"
        }
    ]
}
```

This endpoint retrieves all People Trainings.

### 2.HTTP Request

`GET https://dev.aimlapps.com/people-svc/api/v1/people-trainings`


## View People Training

### 1.HTTP Response
> The above command returns JSON structured like this:

```json
{
    "CompositeAccessPatterns": {
        "S": "PeopleTraining#PeopleTrainingDateFrom:2020-12-12#PeopleTrainingDateTo:2020-12-12#PeopleTrainingCourse:Network#PeopleTrainingDuration:35"
    },
    "PeopleTrainingLocation": {
        "M": {
            "Country": {
                "S": "Thailand"
            },
            "LocationLevel1Name": {
                "S": "Chiang Mai"
            }
        }
    },
    "PeopleTrainingRemark": {
        "S": "I finish Bachelor Degree of IT Network"
    },
    "PeopleTrainingLevel": {
        "S": "Manager"
    },
    "PeopleTrainingDuration": {
        "N": "35"
    },
    "EntityItemId": {
        "S": "PeopleTraining:ca8d95bbc39e8ca6d282880c4510b5c7"
    },
    "PeopleTrainingDateTo": {
        "S": "2020-12-12"
    },
    "PeopleTrainingCenter": {
        "M": {
            "OrganizationName": {
                "S": "ODI Asia Co., Ltd."
            },
            "OrganizationShortName": {
                "S": "ODI"
            },
            "OrganizationId": {
                "S": "OrganizationName:e05d7f46e40731dd0ae0760543eb5596"
            }
        }
    },
    "PeopleTrainingAchievement": {
        "S": "Bachelor Degree"
    },
    "TenantId": {
        "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
    },
    "PeopleTrainingPeopleId": {
        "S": "People:648311551b2f33a84d95f87ca878e6e5"
    },
    "PeopleTrainingCourse": {
        "S": "Network"
    },
    "PeopleTrainingDateFrom": {
        "S": "2020-12-12"
    }
}
```

This endpoint retrieves a specific People Training.

### 2.HTTP Request

`GET https://dev.aimlapps.com/people-svc/api/v1/people-trainings/ID`

### 3.URL Parameters

Parameter | Description
--------- | -----------
ID        | The Id of the People Training that use for view datail.
          | Ex : PeopleTraining:ca8d95bbc39e8ca6d282880c4510b5c7


## Delete People Training
This endpoint delete a specific People Training.

### 1.HTTP Request

`DELETE https://dev.aimlapps.com/people-svc/api/v1/people-trainings/ID`

### 2.URL Parameters

Parameter | Description
--------- | -----------
ID        | The Id of the People Training that use for delete.
          | Ex : PeopleTraining:ca8d95bbc39e8ca6d282880c4510b5c7

