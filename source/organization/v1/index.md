# Organization API Documentation

# Introduction
This document guides you on how to work with resources at the backend of Organization service via API endpoints.

# Authentication
### Header Request
Key             | Value
----            | -----
Authorization   | Bearer Token
Content-Type    | application/json    

# Countries
## Get All Countries

### HTTP Request
`GET organization-svc/api/locations/countries`

### HTTP Response
> The above HTTP request, if successful, will return Json structured like this:

```json
[
    {
        "CountryIso_3166_2": {
            "S": "SB"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "EntityItemId": {
            "S": "Country:0003a74397fab2aa0d15c2d383c36eef"
        },
        "CountryIso_3166_3": {
            "S": "SLB"
        },
        "CountryName": {
            "S": "Solomon Islands"
        }
    },
    {
        "CountryIso_3166_2": {
            "S": "CN"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "EntityItemId": {
            "S": "Country:00c763e8e6895f6224cc56eef69d37c2"
        },
        "CountryIso_3166_3": {
            "S": "CHN"
        },
        "CountryName": {
            "S": "China"
        }
    },
    {
        "CountryIso_3166_2": {
            "S": "NR"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "EntityItemId": {
            "S": "Country:00e8c77c4aa9534224b424fe0ad6623f"
        },
        "CountryIso_3166_3": {
            "S": "NRU"
        },
        "CountryName": {
            "S": "Nauru"
        }
    }
]
```

# Province
## Get All Province

### HTTP Request
`GET organization-svc/api/locations/provinces`

### HTTP Response
> The above HTTP request, if successful, will return Json structured like this:

```json
[
    {
        "LocationLevel1Code": {
            "S": "03"
        },
        "EntityItemId": {
            "S": "LocationLevel1:67189629fc119919e1c8a2d65c80402f"
        },
        "CompositeAccessPatterns": {
            "S": "LocationLevel1#Country:e05d7f46e40731dd0ae0760543eb5596#CountryName:Cambodia"
        },
        "CountryName": {
            "S": "Cambodia"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "CountryId": {
            "S": "Country:e05d7f46e40731dd0ae0760543eb5596"
        },
        "LocationLevel1Name": {
            "S": "Kampong Cham"
        },
        "LocationLevel1KhmerName": {
            "S": "កំពង់ចាម"
        }
    },
    {
        "LocationLevel1Code": {
            "S": "02"
        },
        "EntityItemId": {
            "S": "LocationLevel1:7ed870110dc3d34491b73fe37f02f370"
        },
        "CompositeAccessPatterns": {
            "S": "LocationLevel1#Country:e05d7f46e40731dd0ae0760543eb5596#CountryName:Cambodia"
        },
        "CountryName": {
            "S": "Cambodia"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "CountryId": {
            "S": "Country:e05d7f46e40731dd0ae0760543eb5596"
        },
        "LocationLevel1Name": {
            "S": "Battambang"
        },
        "LocationLevel1KhmerName": {
            "S": "បាត់ដំបង"
        }
    },
    {
        "LocationLevel1Code": {
            "S": "01"
        },
        "EntityItemId": {
            "S": "LocationLevel1:fee79c83882b347f5bf2c4fd8cb3566f"
        },
        "CompositeAccessPatterns": {
            "S": "LocationLevel1#Country:e05d7f46e40731dd0ae0760543eb5596#CountryName:Cambodia"
        },
        "CountryName": {
            "S": "Cambodia"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "CountryId": {
            "S": "Country:e05d7f46e40731dd0ae0760543eb5596"
        },
        "LocationLevel1Name": {
            "S": "Banteay Meanchey"
        },
        "LocationLevel1KhmerName": {
            "S": "បន្ទាយមានជ័យ"
        }
    }
]
```
### HTTP Request Filter 
`GET organization-svc/api/locations/provinces?contains=Country:e05d7f46e40731dd0ae0760543eb5596#CountryName:Cambodia`

### Query Paramaeters
Parameter                   | Description
---------                   | -----------
Country                     | Is the id of the country that covert to uuid.
CountryName                 | Is the name of the country.

### HTTP Response Filter
> The above HTTP request, if successful, will return Json structured like this:

```json
[
{
        "LocationLevel1Code": {
            "S": "13"
        },
        "EntityItemId": {
            "S": "LocationLevel1:0ab897ddf8a29241d630ab4429c4b0d9"
        },
        "CompositeAccessPatterns": {
            "S": "LocationLevel1#Country:e05d7f46e40731dd0ae0760543eb5596#CountryName:Cambodia"
        },
        "CountryName": {
            "S": "Cambodia"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "CountryId": {
            "S": "Country:e05d7f46e40731dd0ae0760543eb5596"
        },
        "LocationLevel1Name": {
            "S": "Preah Vihear"
        },
        "LocationLevel1KhmerName": {
            "S": "ព្រះវិហារ"
        }
    },
    {
        "LocationLevel1Code": {
            "S": "11"
        },
        "EntityItemId": {
            "S": "LocationLevel1:111b3abe7795b6231a75523c37148713"
        },
        "CompositeAccessPatterns": {
            "S": "LocationLevel1#Country:e05d7f46e40731dd0ae0760543eb5596#CountryName:Cambodia"
        },
        "CountryName": {
            "S": "Cambodia"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "CountryId": {
            "S": "Country:e05d7f46e40731dd0ae0760543eb5596"
        },
        "LocationLevel1Name": {
            "S": "Mondul Kiri"
        },
        "LocationLevel1KhmerName": {
            "S": "មណ្ឌលគិរី"
        }
    }
]
```

# Districts
## Get All districts

### HTTP Request
`GET organization-svc/api/locations/districts`

### HTTP Response
> The above HTTP request, if successful, will return Json structured like this:

```json
[
    {
        "LocationLevel2KhmerName": {
            "S": "ស្រីសន្ធរ"
        },
        "LocationLevel1Id": {
            "S": "LocationLevel1:67189629fc119919e1c8a2d65c80402f"
        },
        "EntityItemId": {
            "S": "LocationLevel2:029d52772c42cf101560c4c52d929d5d"
        },
        "CompositeAccessPatterns": {
            "S": "LocationLevel2#LocationLevel1:67189629fc119919e1c8a2d65c80402f#LocationLevel1Name:Kampong Cham"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "LocationLevel1Name": {
            "S": "Kampong Cham"
        },
        "LocationLevel2Name": {
            "S": "Srei Santhor"
        },
        "LocationLevel2Code": {
            "S": "0314"
        }
    },
    {
        "LocationLevel2KhmerName": {
            "S": "ភ្នំស្រុក"
        },
        "LocationLevel1Id": {
            "S": "LocationLevel1:fee79c83882b347f5bf2c4fd8cb3566f"
        },
        "EntityItemId": {
            "S": "LocationLevel2:03c340c1c96e51312d7113f980b5eb5e"
        },
        "CompositeAccessPatterns": {
            "S": "LocationLevel2#LocationLevel1:fee79c83882b347f5bf2c4fd8cb3566f#LocationLevel1Name:Banteay Meanchey"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "LocationLevel1Name": {
            "S": "Banteay Meanchey"
        },
        "LocationLevel2Name": {
            "S": "Phnum Srok"
        },
        "LocationLevel2Code": {
            "S": "0103"
        }
    }
]
```

### HTTP Request Filter 
`GET organization-svc/api/locations/districts?contains=LocationLevel1:422886d8599c6cb51557a0da3423f43c#LocationLevel1Name:Takeo`

### Query Paramaeters
Parameter                   | Description
---------                   | -----------
LocationLevel1              | Is the id of the province that covert to uuid.
LocationLevel1Name          | Is the name of the province.

### HTTP Response Filter
> The above HTTP request, if successful, will return Json structured like this:

```json
[
    {
        "LocationLevel2KhmerName": {
            "S": "ដូនកែវ"
        },
        "LocationLevel1Id": {
            "S": "LocationLevel1:422886d8599c6cb51557a0da3423f43c"
        },
        "EntityItemId": {
            "S": "LocationLevel2:0b289bfd5d789cb4d5436d7f426ad839"
        },
        "CompositeAccessPatterns": {
            "S": "LocationLevel2#LocationLevel1:422886d8599c6cb51557a0da3423f43c#LocationLevel1Name:Takeo"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "LocationLevel1Name": {
            "S": "Takeo"
        },
        "LocationLevel2Name": {
            "S": "Doun Kaev"
        },
        "LocationLevel2Code": {
            "S": "2108"
        }
    },
    {
        "LocationLevel2KhmerName": {
            "S": "បាទី"
        },
        "LocationLevel1Id": {
            "S": "LocationLevel1:422886d8599c6cb51557a0da3423f43c"
        },
        "EntityItemId": {
            "S": "LocationLevel2:706c8226fa639cc261f056025151aa62"
        },
        "CompositeAccessPatterns": {
            "S": "LocationLevel2#LocationLevel1:422886d8599c6cb51557a0da3423f43c#LocationLevel1Name:Takeo"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "LocationLevel1Name": {
            "S": "Takeo"
        },
        "LocationLevel2Name": {
            "S": "Bati"
        },
        "LocationLevel2Code": {
            "S": "2102"
        }
    }
]
```

# Communes
## Get All communes

### HTTP Request
`GET organization-svc/api/locations/communes`

### HTTP Response
> The above HTTP request, if successful, will return Json structured like this:

```json
[
    {
        "LocationLevel3Name": {
            "S": "Damril"
        },
        "EntityItemId": {
            "S": "LocationLevel3:001922002831aae1fe4f6d660d32456d"
        },
        "LocationLevel2Id": {
            "S": "LocationLevel2:73b7d51328eab8c2b34fbb51bc2ccefb"
        },
        "CompositeAccessPatterns": {
            "S": "LocationLevel3#LocationLevel2:73b7d51328eab8c2b34fbb51bc2ccefb#LocationLevel2Name:Ou Reang Ov"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "LocationLevel2Name": {
            "S": "Ou Reang Ov"
        },
        "LocationLevel3KhmerName": {
            "S": "ដំរិល"
        },
        "LocationLevel3Code": {
            "S": "250403"
        }
    },
    {
        "LocationLevel3Name": {
            "S": "Krang Dei Vay"
        },
        "EntityItemId": {
            "S": "LocationLevel3:00b27092931ce4550ffca0afe8928c40"
        },
        "LocationLevel2Id": {
            "S": "LocationLevel2:43415b8b6ab8b1c9e542f7da5eb136d5"
        },
        "CompositeAccessPatterns": {
            "S": "LocationLevel3#LocationLevel2:43415b8b6ab8b1c9e542f7da5eb136d5#LocationLevel2Name:Phnum Sruoch"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "LocationLevel2Name": {
            "S": "Phnum Sruoch"
        },
        "LocationLevel3KhmerName": {
            "S": "ក្រាំងដីវ៉ាយ"
        },
        "LocationLevel3Code": {
            "S": "050605"
        }
    }
]
```
### HTTP Request Filter 
`GET organization-svc/api/locations/communes?contains=LocationLevel2:0b289bfd5d789cb4d5436d7f426ad839#LocationLevel2Name:Doun Kaev`

### Query Paramaeters
Parameter                   | Description
---------                   | -----------
LocationLevel2              | Is the id of the district that covert to uuid.
LocationLevel2Name          | Is the name of the district.

### HTTP Response Filter
> The above HTTP request, if successful, will return Json structured like this:

```json
[
    {
        "LocationLevel3Name": {
            "S": "Roka Knong"
        },
        "EntityItemId": {
            "S": "LocationLevel3:0974848effdedabe74730bfe597b7067"
        },
        "LocationLevel2Id": {
            "S": "LocationLevel2:0b289bfd5d789cb4d5436d7f426ad839"
        },
        "CompositeAccessPatterns": {
            "S": "LocationLevel3#LocationLevel2:0b289bfd5d789cb4d5436d7f426ad839#LocationLevel2Name:Doun Kaev"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "LocationLevel2Name": {
            "S": "Doun Kaev"
        },
        "LocationLevel3KhmerName": {
            "S": "រកាក្នុង"
        },
        "LocationLevel3Code": {
            "S": "210802"
        }
    },
    {
        "LocationLevel3Name": {
            "S": "Roka Krau"
        },
        "EntityItemId": {
            "S": "LocationLevel3:39c5749804bc8318c94a9fcba70d069a"
        },
        "LocationLevel2Id": {
            "S": "LocationLevel2:0b289bfd5d789cb4d5436d7f426ad839"
        },
        "CompositeAccessPatterns": {
            "S": "LocationLevel3#LocationLevel2:0b289bfd5d789cb4d5436d7f426ad839#LocationLevel2Name:Doun Kaev"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "LocationLevel2Name": {
            "S": "Doun Kaev"
        },
        "LocationLevel3KhmerName": {
            "S": "រកាក្រៅ"
        },
        "LocationLevel3Code": {
            "S": "210803"
        }
    },
    {
        "LocationLevel3Name": {
            "S": "Baray"
        },
        "EntityItemId": {
            "S": "LocationLevel3:d6440f5391b68e53822f4451fc039ecb"
        },
        "LocationLevel2Id": {
            "S": "LocationLevel2:0b289bfd5d789cb4d5436d7f426ad839"
        },
        "CompositeAccessPatterns": {
            "S": "LocationLevel3#LocationLevel2:0b289bfd5d789cb4d5436d7f426ad839#LocationLevel2Name:Doun Kaev"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "LocationLevel2Name": {
            "S": "Doun Kaev"
        },
        "LocationLevel3KhmerName": {
            "S": "បារាយណ៍"
        },
        "LocationLevel3Code": {
            "S": "210801"
        }
    }
]
```
# Villages
## Get All villages

### HTTP Request
`GET organization-svc/api/locations/villages`

### HTTP Response
> The above HTTP request, if successful, will return Json structured like this:

```json
[
    {
        "LocationLevel3Name": {
            "S": "Rohal"
        },
        "EntityItemId": {
            "S": "LocationLevel4:00010964629e272de1c53626cf9284e2"
        },
        "CompositeAccessPatterns": {
            "S": "LocationLevel4#LocationLevel3:f6d397999fbabfbfa3ce9c17bce7b3d8#LocationLevel3Name:Rohal"
        },
        "LocationLevel4KhmerName": {
            "S": "ស្នាយ"
        },
        "LocationLevel4Code": {
            "S": "01040605"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "LocationLevel3Id": {
            "S": "LocationLevel3:f6d397999fbabfbfa3ce9c17bce7b3d8"
        },
        "LocationLevel4Name": {
            "S": "Snay"
        }
    },
    {
        "LocationLevel3Name": {
            "S": "Ou Mlu"
        },
        "EntityItemId": {
            "S": "LocationLevel4:00099b4b2b8c0a44beea20294a9bb8a2"
        },
        "CompositeAccessPatterns": {
            "S": "LocationLevel4#LocationLevel3:b4397a4cc8406529514cd8cbe6fc156b#LocationLevel3Name:Ou Mlu"
        },
        "LocationLevel4KhmerName": {
            "S": "អូរប្រឡោះ"
        },
        "LocationLevel4Code": {
            "S": "03150605"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "LocationLevel3Id": {
            "S": "LocationLevel3:b4397a4cc8406529514cd8cbe6fc156b"
        },
        "LocationLevel4Name": {
            "S": "Ou Pralaoh"
        }
    },
    {
        "LocationLevel3Name": {
            "S": "Sragnae"
        },
        "EntityItemId": {
            "S": "LocationLevel4:000ddaddb43521b970359cdd9be7476f"
        },
        "CompositeAccessPatterns": {
            "S": "LocationLevel4#LocationLevel3:c0e60fc6c03d6c9608e678e70f3e3986#LocationLevel3Name:Sragnae"
        },
        "LocationLevel4KhmerName": {
            "S": "ត្រពាំងរូង"
        },
        "LocationLevel4Code": {
            "S": "03131208"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "LocationLevel3Id": {
            "S": "LocationLevel3:c0e60fc6c03d6c9608e678e70f3e3986"
        },
        "LocationLevel4Name": {
            "S": "Trapeang Rung"
        }
    }
]
```

### HTTP Request Filter 
`GET organization-svc/api/locations/villages?contains=LocationLevel3:d6440f5391b68e53822f4451fc039ecb#LocationLevel3Name:Baray Kaev`

### Query Paramaeters
Parameter                   | Description
---------                   | -----------
LocationLevel3              | Is the id of the communes that covert to uuid.
LocationLevel3Name          | Is the name of the communes.

### HTTP Response Filter
> The above HTTP request, if successful, will return Json structured like this:

```json
[
    {
        "LocationLevel3Name": {
            "S": "Baray"
        },
        "EntityItemId": {
            "S": "LocationLevel4:08a398d5762b83b247714472094ff015"
        },
        "CompositeAccessPatterns": {
            "S": "LocationLevel4#LocationLevel3:d6440f5391b68e53822f4451fc039ecb#LocationLevel3Name:Baray"
        },
        "LocationLevel4KhmerName": {
            "S": "ក្រាំងតាពូង"
        },
        "LocationLevel4Code": {
            "S": "21080113"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "LocationLevel3Id": {
            "S": "LocationLevel3:d6440f5391b68e53822f4451fc039ecb"
        },
        "LocationLevel4Name": {
            "S": "Krang Ta Pung"
        }
    },
    {
        "LocationLevel3Name": {
            "S": "Baray"
        },
        "EntityItemId": {
            "S": "LocationLevel4:0aee6625d7809bd49453f77b42554492"
        },
        "CompositeAccessPatterns": {
            "S": "LocationLevel4#LocationLevel3:d6440f5391b68e53822f4451fc039ecb#LocationLevel3Name:Baray"
        },
        "LocationLevel4KhmerName": {
            "S": "ជ្រោយប្រឃរ"
        },
        "LocationLevel4Code": {
            "S": "21080104"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "LocationLevel3Id": {
            "S": "LocationLevel3:d6440f5391b68e53822f4451fc039ecb"
        },
        "LocationLevel4Name": {
            "S": "Chrouy Prakhor"
        }
    },
    {
        "LocationLevel3Name": {
            "S": "Baray"
        },
        "EntityItemId": {
            "S": "LocationLevel4:10077a6ce405bbb3d4465d52715ab798"
        },
        "CompositeAccessPatterns": {
            "S": "LocationLevel4#LocationLevel3:07bdde0902576757d6deff54f884bda7#LocationLevel3Name:Baray"
        },
        "LocationLevel4KhmerName": {
            "S": "ពោធិ៍ពីរ"
        },
        "LocationLevel4Code": {
            "S": "06010311"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "LocationLevel3Id": {
            "S": "LocationLevel3:07bdde0902576757d6deff54f884bda7"
        },
        "LocationLevel4Name": {
            "S": "Pou Pir"
        }
    }
]
```

# Organization
## Get All Organization

### HTTP Request
`GET organization-svc/api/organizations`

### HTTP Response
> The above HTTP request, if successful, will return Json structured like this:

```json
[
    {
        "OrganizationVatNumber": {
            "S": "Activate"
        },
        "EntityItemId": {
            "S": "Organization:efb8fc57567919cce70374bf1a1f3f8d"
        },
        "OrganizationContactOther": {
            "L": [
                {
                    "M": {
                        "PhoneNumber": {
                            "S": "023 995 500"
                        },
                        "Website": {
                            "S": "https://www.passerellesnumeriques.org/en/"
                        },
                        "SocialProfile": {
                            "S": "https://www.facebook.com/PnCambodiaAlumni/"
                        },
                        "Email": {
                            "S": "info.cambodia@passerellesnumeriques.org"
                        }
                    }
                }
            ]
        },
        "CompositeAccessPatterns": {
            "S": "Organization#OrganizationNature:Nonprofit#OrganizationName:Passerelles Numeriques Cambodia#OrganizationShortName:PNC"
        },
        "OrganizationIndustry": {
            "L": [
                {
                    "M": {
                        "IndustryName": {
                            "S": "Organization"
                        },
                        "SubIndustry": {
                            "L": [
                                {
                                    "M": {
                                        "Name": {
                                            "S": "School"
                                        }
                                    }
                                }
                            ]
                        }
                    }
                }
            ]
        },
        "OrganizationName": {
            "S": "Passerelles Numeriques Cambodia"
        },
        "OrganizationAddress": {
            "L": [
                {
                    "M": {
                        "CountryName": {
                            "S": "Cambodia"
                        },
                        "LocationLevel4Name": {
                            "S": "Phum Tropeang Chhuk"
                        },
                        "StreetAddessDetail": {
                            "S": "371"
                        },
                        "LocationLevel1Name": {
                            "S": "Phnom Penh"
                        },
                        "LocationLevel2Name": {
                            "S": "Sen Sok"
                        },
                        "LocationLevel3Name": {
                            "S": "Tek Thla"
                        },
                        "PostalCode": {
                            "S": "120209"
                        }
                    }
                }
            ]
        },
        "OrganizationNature": {
            "S": "Nonprofit"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "OrganizationShortName": {
            "S": "PNC"
        }
    }
]
```

### HTTP Request Filter 
`GET organization-svc/api/organizations?contains=OrganizationNature:Nonprofit`

### Query Paramaeters
Parameter                   | Description
---------                   | -----------
OrganizationNature          | Is the nature of organization. EX: Private, Nonprofit, Public
OrganizationName            | Is the name of the organization. EX: Artifcial Intelligence Machine Learning
OrganizationShortName       | Is the short name of the organization. Ex: AIML

### HTTP Response Filter
> The above HTTP request, if successful, will return Json structured like this:

```json
{
    "OrganizationVatNumber": {
        "S": "Activate"
    },
    "EntityItemId": {
        "S": "Organization:efb8fc57567919cce70374bf1a1f3f8d"
    },
    "OrganizationContactOther": {
        "L": [
            {
                "M": {
                    "PhoneNumber": {
                        "S": "023 995 500"
                    },
                    "Website": {
                        "S": "https://www.passerellesnumeriques.org/en/"
                    },
                    "SocialProfile": {
                        "S": "https://www.facebook.com/PnCambodiaAlumni/"
                    },
                    "Email": {
                        "S": "info.cambodia@passerellesnumeriques.org"
                    }
                }
            }
        ]
    },
    "CompositeAccessPatterns": {
        "S": "Organization#OrganizationNature:Nonprofit#OrganizationName:Passerelles Numeriques Cambodia#OrganizationShortName:PNC"
    },
    "OrganizationIndustry": {
        "L": [
            {
                "M": {
                    "IndustryName": {
                        "S": "Organization"
                    },
                    "SubIndustry": {
                        "L": [
                            {
                                "M": {
                                    "Name": {
                                        "S": "School"
                                    }
                                }
                            }
                        ]
                    }
                }
            }
        ]
    },
    "OrganizationName": {
        "S": "Passerelles Numeriques Cambodia"
    },
    "OrganizationAddress": {
        "L": [
            {
                "M": {
                    "CountryName": {
                        "S": "Cambodia"
                    },
                    "LocationLevel4Name": {
                        "S": "Phum Tropeang Chhuk"
                    },
                    "StreetAddessDetail": {
                        "S": "371"
                    },
                    "LocationLevel1Name": {
                        "S": "Phnom Penh"
                    },
                    "LocationLevel2Name": {
                        "S": "Sen Sok"
                    },
                    "LocationLevel3Name": {
                        "S": "Tek Thla"
                    },
                    "PostalCode": {
                        "S": "120209"
                    }
                }
            }
        ]
    },
    "OrganizationNature": {
        "S": "Nonprofit"
    },
    "TenantId": {
        "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
    },
    "OrganizationShortName": {
        "S": "PNC"
    }
}
```

## Create a Organization
### HTTP Request
`POST organization-svc/api/organization`

### Body Request

```json
{
    "Organization": {
        "OrganizationName": "Passerelles Numeriques Cambodia",
        "OrganizationShortName": "PNC",
        "OrganizationNature": "Nonprofit",
        "OrganizationVatNumber": "Activate",
        "Children": {
            "Industry": [
                {
                    "IndustryName":"Organization",
                    "SubIndustry":[
                        {
                            "Name":"School"
                        }
                    ]
                }
            ],
            "Address": [
                {
                    "CountryName": "Cambodia",
                    "LocationLevel1Name": "Phnom Penh",
                    "PostalCode": "120209",
                    "LocationLevel2Name": "Sen Sok",
                    "LocationLevel3Name": "Tek Thla",
                    "LocationLevel4Name": "Phum Tropeang Chhuk",
                    "StreetAddessDetail": "371"
                }
            ],
            "ContactOther": [
                {
                    "PhoneNumber": "023 995 500",
                    "Email": "info.cambodia@passerellesnumeriques.org",
                    "Website": "https://www.passerellesnumeriques.org/en/",
                    "SocialProfile": "https://www.facebook.com/PnCambodiaAlumni/"
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

## Update a Organization
### HTTP Request
`PUT organization-svc/api/organization/{item_id}`

### Query Paramaeters
Parameter                   | Description
---------                   | -----------
item_id                     | Is the entity item id of organization. EX: Organization:c38176abf908a76616ed9ab31bc63eb4

### Body Request

```json
{
    "Organization": {
        "OrganizationName": "Passerelles Numeriques Cambodia",
        "OrganizationShortName": "PNC",
        "OrganizationNature": "Nonprofit",
        "OrganizationVatNumber": "Activate",
        "Children": {
            "Industry": [
                {
                    "IndustryName":"Organization",
                    "SubIndustry":[
                        {
                            "Name":"School"
                        }
                    ]
                }
            ],
            "Address": [
                {
                    "CountryName": "Cambodia",
                    "LocationLevel1Name": "Phnom Penh",
                    "PostalCode": "120209",
                    "LocationLevel2Name": "Sen Sok",
                    "LocationLevel3Name": "Tek Thla",
                    "LocationLevel4Name": "Phum Tropeang Chhuk",
                    "StreetAddessDetail": "371"
                }
            ],
            "ContactOther": [
                {
                    "PhoneNumber": "023 995 500",
                    "Email": "info.cambodia@passerellesnumeriques.org",
                    "Website": "https://www.passerellesnumeriques.org/en/",
                    "SocialProfile": "https://www.facebook.com/PnCambodiaAlumni/"
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
    "OrganizationVatNumber": {
        "S": "Activate"
    },
    "EntityItemId": {
        "S": "Organization:efb8fc57567919cce70374bf1a1f3f8d"
    },
    "OrganizationContactOther": {
        "L": [
            {
                "M": {
                    "PhoneNumber": {
                        "S": "023 995 500"
                    },
                    "Website": {
                        "S": "https://www.passerellesnumeriques.org/en/"
                    },
                    "SocialProfile": {
                        "S": "https://www.facebook.com/PnCambodiaAlumni/"
                    },
                    "Email": {
                        "S": "info.cambodia@passerellesnumeriques.org"
                    }
                }
            }
        ]
    },
    "CompositeAccessPatterns": {
        "S": "Organization#OrganizationNature:Nonprofit#OrganizationName:Passerelles Numeriques Cambodia#OrganizationShortName:PNC"
    },
    "OrganizationIndustry": {
        "L": [
            {
                "M": {
                    "IndustryName": {
                        "S": "Organization"
                    },
                    "SubIndustry": {
                        "L": [
                            {
                                "M": {
                                    "Name": {
                                        "S": "School"
                                    }
                                }
                            }
                        ]
                    }
                }
            }
        ]
    },
    "OrganizationName": {
        "S": "Passerelles Numeriques Cambodia"
    },
    "OrganizationAddress": {
        "L": [
            {
                "M": {
                    "CountryName": {
                        "S": "Cambodia"
                    },
                    "LocationLevel4Name": {
                        "S": "Phum Tropeang Chhuk"
                    },
                    "StreetAddessDetail": {
                        "S": "371"
                    },
                    "LocationLevel1Name": {
                        "S": "Phnom Penh"
                    },
                    "LocationLevel2Name": {
                        "S": "Sen Sok"
                    },
                    "LocationLevel3Name": {
                        "S": "Tek Thla"
                    },
                    "PostalCode": {
                        "S": "120209"
                    }
                }
            }
        ]
    },
    "OrganizationNature": {
        "S": "Nonprofit"
    },
    "TenantId": {
        "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
    },
    "OrganizationShortName": {
        "S": "PNC"
    }
}
```

## Delete a Organization
### HTTP Request
`DELETE organization-svc/api/organization/{item_id}`

### Query Paramaeters
Parameter                   | Description
---------                   | -----------
item_id                     | Is the entity item id of organization. EX: Organization:c38176abf908a76616ed9ab31bc63eb4

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

# OrganizationalUnit
## Get All OrganizationalUnits

### HTTP Request
`GET organization-svc/api/organizationalUnits`

### HTTP Response
> The above HTTP request, if successful, will return Json structured like this:

```json
[
    {
        "OrganizationalUnitPrimaryInCharge": {
            "L": [
                {
                    "M": {
                        "EmployeeId": {
                            "S": "Employee:748f596f-3144-4704-b816-3d0cbd5f5f64"
                        },
                        "EmployeeName": {
                            "S": "Dyna"
                        }
                    }
                }
            ]
        },
        "EntityItemId": {
            "S": "OrganizationalUnit:cf89605f7a6536680b5ff7d952394607"
        },
        "CompositeAccessPatterns": {
            "S": "OrganizationalUnit#OrganizationalUnitLevel:1#OrganizationalUnitName:Sopheap#OrganizationalUnitShortName:SP#OrganizationalUnitParentId:61751b1b-0d66-4b80-82dc-4c3d12969224#OrganizationalUnitParentName:ODI"
        },
        "OrganizationalUnitLevel": {
            "N": "1"
        },
        "OrganizationalUnitParentName": {
            "S": "ODI"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "OrganizationalUnitShortName": {
            "S": "SP"
        },
        "OrganizationalUnitSecondaryInCharge": {
            "L": [
                {
                    "M": {
                        "EmployeeId": {
                            "S": "Employee:b4b09720-bf38-4f56-a6b1-df9876f5f000"
                        },
                        "EmployeeName": {
                            "S": "Sina"
                        }
                    }
                }
            ]
        },
        "OrganizationalUnitName": {
            "S": "Sopheap"
        },
        "OrganizationalUnitParentId": {
            "S": "61751b1b-0d66-4b80-82dc-4c3d12969224"
        }
    }
]
```

### HTTP Request Filter 
`GET organization-svc/api/organizationalUnits?contains=OrganizationalUnitLevel:1`

### Query Paramaeters
Parameter                       | Description
---------                       | -----------
OrganizationalUnitLevel         | Is the level of organizational unit.
OrganizationalUnitName          | Is the name of the organizational unit.
OrganizationalUnitShortName     | Is the short name of the organizational unit.
OrganizationalUnitParentId      | Is the parent id of the organizational unit.
OrganizationalUnitParentName    | Is the parent name of the organizational unit.

### HTTP Response Filter
> The above HTTP request, if successful, will return Json structured like this:

```json
{
    "OrganizationalUnitPrimaryInCharge": {
        "L": [
            {
                "M": {
                    "EmployeeId": {
                        "S": "Employee:748f596f-3144-4704-b816-3d0cbd5f5f64"
                    },
                    "EmployeeName": {
                        "S": "Dyna"
                    }
                }
            }
        ]
    },
    "EntityItemId": {
        "S": "OrganizationalUnit:cf89605f7a6536680b5ff7d952394607"
    },
    "CompositeAccessPatterns": {
        "S": "OrganizationalUnit#OrganizationalUnitLevel:1#OrganizationalUnitName:Sopheap#OrganizationalUnitShortName:SP#OrganizationalUnitParentId:61751b1b-0d66-4b80-82dc-4c3d12969224#OrganizationalUnitParentName:ODI"
    },
    "OrganizationalUnitLevel": {
        "N": "1"
    },
    "OrganizationalUnitParentName": {
        "S": "ODI"
    },
    "TenantId": {
        "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
    },
    "OrganizationalUnitShortName": {
        "S": "SP"
    },
    "OrganizationalUnitSecondaryInCharge": {
        "L": [
            {
                "M": {
                    "EmployeeId": {
                        "S": "Employee:b4b09720-bf38-4f56-a6b1-df9876f5f000"
                    },
                    "EmployeeName": {
                        "S": "Sina"
                    }
                }
            }
        ]
    },
    "OrganizationalUnitName": {
        "S": "Sopheap"
    },
    "OrganizationalUnitParentId": {
        "S": "61751b1b-0d66-4b80-82dc-4c3d12969224"
    }
}
```

## Create a OrganizationalUnit
### HTTP Request
`POST organization-svc/api/organizationalUnit`

### Body Request

```json
{
    "OrganizationalUnit": {
        "OrganizationalUnitName": "Sopheap",
        "OrganizationalUnitShortName": "SP",
        "OrganizationalUnitLevel": "1",
        "OrganizationalUnitParentId": "61751b1b-0d66-4b80-82dc-4c3d12969224",
        "OrganizationalUnitParentName": "ODI",
        "Children": {
            "PrimaryInCharge": [
                {
                    "EmployeeId": "Employee:748f596f-3144-4704-b816-3d0cbd5f5f64",
                    "EmployeeName": "Dyna"
                }
            ],
            "SecondaryInCharge":[
                {
                    "EmployeeId": "Employee:b4b09720-bf38-4f56-a6b1-df9876f5f000",
                    "EmployeeName": "Sina"
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

## Update a OrganizationalUnit
### HTTP Request
`PUT organization-svc/api/organizationalUnit/{item_id}`

### Query Paramaeters
Parameter                   | Description
---------                   | -----------
item_id                     | Is the entity item id of organizationalUnit. EX: OrganizationalUnit:cf89605f7a6536680b5ff7d952394607

### Body Request

```json
{
    "OrganizationalUnit": {
        "OrganizationalUnitName": "Sopheap",
        "OrganizationalUnitShortName": "SP",
        "OrganizationalUnitLevel": "1",
        "OrganizationalUnitParentId": "61751b1b-0d66-4b80-82dc-4c3d12969224",
        "OrganizationalUnitParentName": "ODI",
        "Children": {
            "PrimaryInCharge": [
                {
                    "EmployeeId": "Employee:748f596f-3144-4704-b816-3d0cbd5f5f64",
                    "EmployeeName": "Dyna"
                }
            ],
            "SecondaryInCharge":[
                {
                    "EmployeeId": "Employee:b4b09720-bf38-4f56-a6b1-df9876f5f000",
                    "EmployeeName": "Sina"
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
    "OrganizationalUnitPrimaryInCharge": {
        "L": [
            {
                "M": {
                    "EmployeeId": {
                        "S": "Employee:748f596f-3144-4704-b816-3d0cbd5f5f64"
                    },
                    "EmployeeName": {
                        "S": "Dyna"
                    }
                }
            }
        ]
    },
    "EntityItemId": {
        "S": "OrganizationalUnit:cf89605f7a6536680b5ff7d952394607"
    },
    "CompositeAccessPatterns": {
        "S": "OrganizationalUnit#OrganizationalUnitLevel:1#OrganizationalUnitName:Sopheap#OrganizationalUnitShortName:SP#OrganizationalUnitParentId:61751b1b-0d66-4b80-82dc-4c3d12969224#OrganizationalUnitParentName:ODI"
    },
    "OrganizationalUnitLevel": {
        "N": "1"
    },
    "OrganizationalUnitParentName": {
        "S": "ODI"
    },
    "TenantId": {
        "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
    },
    "OrganizationalUnitShortName": {
        "S": "SP"
    },
    "OrganizationalUnitSecondaryInCharge": {
        "L": [
            {
                "M": {
                    "EmployeeId": {
                        "S": "Employee:b4b09720-bf38-4f56-a6b1-df9876f5f000"
                    },
                    "EmployeeName": {
                        "S": "Sina"
                    }
                }
            }
        ]
    },
    "OrganizationalUnitName": {
        "S": "Sopheap"
    },
    "OrganizationalUnitParentId": {
        "S": "61751b1b-0d66-4b80-82dc-4c3d12969224"
    }
}
```

## Delete a OrganizationalUnit
### HTTP Request
`DELETE organization-svc/api/organizationalUnit/{item_id}`

### Query Paramaeters
Parameter                   | Description
---------                   | -----------
item_id                     | Is the entity item id of organization. EX: OrganizationalUnit:cf89605f7a6536680b5ff7d952394607

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

# JobProfile
## Get All JobProfiles

### HTTP Request
`GET organization-svc/api/jobProfiles`

### HTTP Response
> The above HTTP request, if successful, will return Json structured like this:

```json
[
    {
        "JobProfileSalaryMax": {
            "S": "300"
        },
        "EntityItemId": {
            "S": "JobProfile:9a7360586dcc7578cb792b58e3ba6072"
        },
        "JobProfilePositionId": {
            "S": "bebb9cdb-230a-4e7c-9f7b-a9e175445ca6"
        },
        "JobProfileDetail": {
            "N": "2"
        },
        "CompositeAccessPatterns": {
            "S": "JobProfile#JobProfilePositionId:bebb9cdb-230a-4e7c-9f7b-a9e175445ca6#JobProfilePositionTitle:Web Programing"
        },
        "JobProfileSalaryMin": {
            "S": "250"
        },
        "JobProfilePositionTitle": {
            "S": "Web Programing"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "JobProfileOverview": {
            "N": "1"
        },
        "JobProfileJobGrade": {
            "N": "5"
        },
        "JobProfileWorkingHour": {
            "N": "8"
        }
    }
]
```

### HTTP Request Filter 
`GET organization-svc/api/jobProfiles?contains=JobProfilePositionId:001`

### Query Paramaeters
Parameter                       | Description
---------                       | -----------
JobProfilePositionId            | Is the position id of jobProfile.
JobProfilePositionTitle         | Is the position title of the jobProfile.
JobProfileJobGrade              | Is the job grade of the jobProfile. Ex: 1, 2, 3, 4, 5...

### HTTP Response Filter
> The above HTTP request, if successful, will return Json structured like this:

```json
{
    "JobProfileSalaryMax": {
        "S": "2000"
    },
    "EntityItemId": {
        "S": "JobProfile:9a7360586dcc7578cb792b58e3ba6072"
    },
    "JobProfileDetail": {
        "N": "112"
    },
    "JobProfilePositionId": {
        "S": "001"
    },
    "CompositeAccessPatterns": {
        "S": "JobProfile#JobProfilePositionId:001#JobProfilePositionTitle:Java Team Lead"
    },
    "JobProfileSalaryMin": {
        "S": "1500"
    },
    "JobProfilePositionTitle": {
        "S": "Java Team Lead"
    },
    "JobProfileOverview": {
        "N": "111"
    },
    "TenantId": {
        "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
    },
    "JobProfileJobGrade": {
        "N": "1"
    },
    "JobProfileWorkingHour": {
        "N": "8"
    }
}
```

## Create a JobProfile
### HTTP Request
`POST organization-svc/api/jobProfile`

### Body Request

```json
{
    "JobProfile": {
        "JobProfilePositionId": "001",
        "JobProfilePositionTitle": "Java Team Lead",
        "JobProfileJobGrade": "1",
        "JobProfileSalaryMin": "1500",
        "JobProfileSalaryMax": "2000",
        "JobProfileWorkingHour": "8",
        "JobProfileOverview": "111",
        "JobProfileDetail": "112"
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

## Update a jobProfile
### HTTP Request
`PUT organization-svc/api/jobProfile/{item_id}`

### Query Paramaeters
Parameter                   | Description
---------                   | -----------
item_id                     | Is the entity item id of jobProfile. EX: JobProfile:9a7360586dcc7578cb792b58e3ba6072

### Body Request

```json
{
    "JobProfile": {
        "JobProfilePositionId": "001",
        "JobProfilePositionTitle": "Java Team Lead",
        "JobProfileJobGrade": "1",
        "JobProfileSalaryMin": "1500",
        "JobProfileSalaryMax": "2000",
        "JobProfileWorkingHour": "8",
        "JobProfileOverview": "111",
        "JobProfileDetail": "112"
    }
}
```

### HTTP Response
> The above HTTP request, if successful, will return Json structured like this:

```json
{
    "JobProfileSalaryMax": {
        "S": "2000"
    },
    "EntityItemId": {
        "S": "JobProfile:9a7360586dcc7578cb792b58e3ba6072"
    },
    "JobProfileDetail": {
        "N": "112"
    },
    "JobProfilePositionId": {
        "S": "001"
    },
    "CompositeAccessPatterns": {
        "S": "JobProfile#JobProfilePositionId:001#JobProfilePositionTitle:Java Team Lead"
    },
    "JobProfileSalaryMin": {
        "S": "1500"
    },
    "JobProfilePositionTitle": {
        "S": "Java Team Lead"
    },
    "JobProfileOverview": {
        "N": "111"
    },
    "TenantId": {
        "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
    },
    "JobProfileJobGrade": {
        "N": "1"
    },
    "JobProfileWorkingHour": {
        "N": "8"
    }
}
```

## Delete a jobProfile
### HTTP Request
`DELETE organization-svc/api/jobProfile/{item_id}`

### Query Paramaeters
Parameter                   | Description
---------                   | -----------
item_id                     | Is the entity item id of jobProfile. EX: JobProfile:9a7360586dcc7578cb792b58e3ba6072

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

# Position
## Get All Positions

### HTTP Request
`GET organization-svc/api/postions`

### HTTP Response
> The above HTTP request, if successful, will return Json structured like this:

```json
[
    {
        "PostionTitleEn": {
            "S": "Programmer"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "EntityItemId": {
            "S": "Postion:18053c214000057310161eb13f4e67d6"
        },
        "CompositeAccessPatterns": {
            "S": "Postion#PostionTitleEn:Programmer#PostionTitleKh:អ្នកសរសេរកម្មវិធី"
        },
        "PostionTitleKh": {
            "S": "អ្នកសរសេរកម្មវិធី"
        }
    },
    {
        "PostionTitleEn": {
            "S": "Marketing"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "EntityItemId": {
            "S": "Postion:97ae6cded39dc1c42890b9075bb7e183"
        },
        "CompositeAccessPatterns": {
            "S": "Postion#PostionTitleEn:Marketing#PostionTitleKh:ផ្នែកទីផ្សារ"
        },
        "PostionTitleKh": {
            "S": "ផ្នែកទីផ្សារ"
        }
    },
]
```

### HTTP Request Filter 
`GET organization-svc/api/positions?contains=PostionTitleEn:Programmer`

### Query Paramaeters
Parameter                       | Description
---------                       | -----------
PostionTitleEn                  | Is the title English of the position.
PostionTitleKh                  | Is the title Khmer of the position.

### HTTP Response Filter
> The above HTTP request, if successful, will return Json structured like this:

```json
{
    "PostionTitleEn": {
        "S": "Programmer"
    },
    "TenantId": {
        "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
    },
    "EntityItemId": {
        "S": "Postion:18053c214000057310161eb13f4e67d6"
    },
    "CompositeAccessPatterns": {
        "S": "Postion#PostionTitleEn:Programmer#PostionTitleKh:អ្នកសរសេរកម្មវិធី"
    },
    "PostionTitleKh": {
        "S": "អ្នកសរសេរកម្មវិធី"
    }
}
```

## Create a Position
### HTTP Request
`POST organization-svc/api/postion`

### Body Request

```json
{
    "Postion": {
        "PostionTitleEn": "Programmer",
        "PostionTitleKh": "អ្នកសរសេរកម្មវិធី"
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

## Update a Position
### HTTP Request
`PUT organization-svc/api/postion/{item_id}`

### Query Paramaeters
Parameter                   | Description
---------                   | -----------
item_id                     | Is the entity item id of postion. EX: Postion:18053c214000057310161eb13f4e67d6

### Body Request

```json
{
    "Postion": {
        "PostionTitleEn": "Programmer",
        "PostionTitleKh": "អ្នកសរសេរកម្មវិធី"
    }
}
```

### HTTP Response
> The above HTTP request, if successful, will return Json structured like this:

```json
{
    "PostionTitleEn": {
        "S": "Programmer"
    },
    "TenantId": {
        "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
    },
    "EntityItemId": {
        "S": "Postion:18053c214000057310161eb13f4e67d6"
    },
    "CompositeAccessPatterns": {
        "S": "Postion#PostionTitleEn:Programmer#PostionTitleKh:អ្នកសរសេរកម្មវិធី"
    },
    "PostionTitleKh": {
        "S": "អ្នកសរសេរកម្មវិធី"
    }
}
```

## Delete a Position
### HTTP Request
`DELETE organization-svc/api/postion/{item_id}`

### Query Paramaeters
Parameter                   | Description
---------                   | -----------
item_id                     | Is the entity item id of postion. EX: Postion:18053c214000057310161eb13f4e67d6

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

# Benefit
## Get All Benefits

### HTTP Request
`GET organization-svc/api/benefits`

### HTTP Response
> The above HTTP request, if successful, will return Json structured like this:

```json
[
    {
        "BenefitGroupTitleKh": {
            "S": "ប្រាក់ខែ"
        },
        "EntityItemId": {
            "S": "Benefit:c21268600e4c10798746b9e67000bd94"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "BenefitBenefitItem": {
            "L": [
                {
                    "M": {
                        "TitleEn": {
                            "S": "Holiday"
                        },
                        "TitleKh": {
                            "S": "ថ្ងៃឈប់សំរាក"
                        }
                    }
                }
            ]
        },
        "CompositeAccessPatterns": {
            "S": "Benefit#BenefitGroupTitleEn:Salary#BenefitGroupTitleKh:ប្រាក់ខែ"
        },
        "BenefitGroupTitleEn": {
            "S": "Salary"
        }
    }
]
```

## Create a Benifit
### HTTP Request
`POST organization-svc/api/benefit`

### Body Request

```json
{
    "Benefit": {
        "BenefitGroupTitleEn": "Salary",
        "BenefitGroupTitleKh": "ប្រាក់ខែ",
        "Children": {
            "BenefitItem":[
                {
                    "TitleEn":"Holiday",
                    "TitleKh":"ថ្ងៃឈប់សំរាក"
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

## Update a Benefit
### HTTP Request
`PUT organization-svc/api/benefit/{item_id}`

### Query Paramaeters
Parameter                   | Description
---------                   | -----------
item_id                     | Is the entity item id of benefit. EX: Benefit:18053c214000057310161eb13f4e67d6

### Body Request

```json
{
    "Benefit": {
        "BenefitGroupTitleEn": "Salary",
        "BenefitGroupTitleKh": "ប្រាក់ខែ",
        "Children": {
            "BenefitItem":[
                {
                    "TitleEn":"Holiday",
                    "TitleKh":"ថ្ងៃឈប់សំរាក"
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
    "BenefitGroupTitleKh": {
        "S": "ប្រាក់ខែ"
    },
    "EntityItemId": {
        "S": "Benefit:c21268600e4c10798746b9e67000bd94"
    },
    "TenantId": {
        "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
    },
    "BenefitBenefitItem": {
        "L": [
            {
                "M": {
                    "TitleEn": {
                        "S": "Holiday"
                    },
                    "TitleKh": {
                        "S": "ថ្ងៃឈប់សំរាក"
                    }
                }
            }
        ]
    },
    "CompositeAccessPatterns": {
        "S": "Benefit#BenefitGroupTitleEn:Salary#BenefitGroupTitleKh:ប្រាក់ខែ"
    },
    "BenefitGroupTitleEn": {
        "S": "Salary"
    }
}
```

## Delete a Benefit
### HTTP Request
`DELETE organization-svc/api/benefit/{item_id}`

### Query Paramaeters
Parameter                   | Description
---------                   | -----------
item_id                     | Is the entity item id of Benefit. EX: Benefit:18053c214000057310161eb13f4e67d6

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



