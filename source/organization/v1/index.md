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
`GET organization-svc/api/v1/organizations`

### HTTP Response
> The above HTTP request, if successful, will return Json structured like this:

```json
[
    {
        "OrganizationVatNumber": {
            "S": "Activate"
        },
        "EntityItemId": {
            "S": "Organization:726e989de1b117afbacc0d3f4d08a10f"
        },
        "OrganizationContactOther": {
            "L": [
                {
                    "M": {
                        "PhoneNumber": {
                            "S": "012 345 678"
                        },
                        "Website": {
                            "S": "https://www.aimltechnologies.com/"
                        },
                        "SocialProfile": {
                            "S": "https://www.facebook.com/AIMLTechnology/"
                        },
                        "Email": {
                            "S": "contact@aimltechnologies.com"
                        }
                    }
                }
            ]
        },
        "CompositeAccessPatterns": {
            "S": "Organization#OrganizationNature:Privately Held#OrganizationName:Artifcail Intelligence Machine Learning#OrganizationShortName:AIML"
        },
        "OrganizationIndustry": {
            "L": [
                {
                    "M": {
                        "IndustryName": {
                            "S": "Organization"
                        }
                    }
                }
            ]
        },
        "OrganizationName": {
            "S": "Artifcail Intelligence Machine Learning"
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
                            "S": "169"
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
            "S": "Privately Held"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "OrganizationShortName": {
            "S": "AIML"
        }
    },
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

## Create a Organization
### HTTP Request
`POST organization-svc/api/v1/organizations`

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
        "S": "Organization:fbdc938e2db8b822ba06ce05d30b4cc4"
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

## Update a Organization
### HTTP Request
`PUT organization-svc/api/v1/organizations/{item_id}`

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
`DELETE organization-svc/api/v1/organizations/{item_id}`

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
`GET organization-svc/api/v1/organizational-units`

### HTTP Response
> The above HTTP request, if successful, will return Json structured like this:

```json
[
    {
        "EntityItemId": {
            "S": "OrganizationalUnit:693a5f054f956b96749c9500203bec62"
        },
        "CompositeAccessPatterns": {
            "S": "OrganizationalUnit#OrganizationalUnitLevel:2#OrganizationalUnitName:Department Head#OrganizationalUnitShortName:DH#OrganizationalUnitParentId:OrganizationalUnit:ad11b1d2fe47e7a29288bdb512eefc05#OrganizationalUnitParentName:MD#OrganizationalUnitManagingRoleId:Role:5387cd2eff7523044338979d36b4b38c"
        },
        "OrganizationalUnitLevel": {
            "N": "2"
        },
        "OrganizationalUnitParentName": {
            "S": "MD"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "OrganizationalUnitShortName": {
            "S": "DH"
        },
        "OrganizationalUnitManagingRoleId": {
            "S": "Role:5387cd2eff7523044338979d36b4b38c"
        },
        "OrganizationalUnitName": {
            "S": "Department Head"
        },
        "OrganizationalUnitParentId": {
            "S": "OrganizationalUnit:ad11b1d2fe47e7a29288bdb512eefc05"
        }
    },
    {
        "EntityItemId": {
            "S": "OrganizationalUnit:6a6fe2d2bd9fb4dbae468e35704b977a"
        },
        "CompositeAccessPatterns": {
            "S": "OrganizationalUnit#OrganizationalUnitLevel:3#OrganizationalUnitName:Manager#OrganizationalUnitShortName:M#OrganizationalUnitParentId:OrganizationalUnit:693a5f054f956b96749c9500203bec62#OrganizationalUnitParentName:DH#OrganizationalUnitManagingRoleId:Role:5387cd2eff7523044338979d36b4b38c"
        },
        "OrganizationalUnitLevel": {
            "N": "3"
        },
        "OrganizationalUnitParentName": {
            "S": "DH"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "OrganizationalUnitShortName": {
            "S": "M"
        },
        "OrganizationalUnitManagingRoleId": {
            "S": "Role:5387cd2eff7523044338979d36b4b38c"
        },
        "OrganizationalUnitName": {
            "S": "Manager"
        },
        "OrganizationalUnitParentId": {
            "S": "OrganizationalUnit:693a5f054f956b96749c9500203bec62"
        }
    },
    {
        "EntityItemId": {
            "S": "OrganizationalUnit:ad11b1d2fe47e7a29288bdb512eefc05"
        },
        "CompositeAccessPatterns": {
            "S": "OrganizationalUnit#OrganizationalUnitLevel:1#OrganizationalUnitName:Managing Director#OrganizationalUnitShortName:MD#OrganizationalUnitParentId:null#OrganizationalUnitParentName:null#OrganizationalUnitManagingRoleId:Role:4d544df22238f1beccca28534e18b0ba"
        },
        "OrganizationalUnitLevel": {
            "N": "1"
        },
        "OrganizationalUnitParentName": {
            "S": "null"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "OrganizationalUnitShortName": {
            "S": "MD"
        },
        "OrganizationalUnitManagingRoleId": {
            "S": "Role:4d544df22238f1beccca28534e18b0ba"
        },
        "OrganizationalUnitName": {
            "S": "Managing Director"
        },
        "OrganizationalUnitParentId": {
            "S": "null"
        }
    }
]
```

### HTTP Request Filter 
`GET organization-svc/api/v1/organizational-units?contains=OrganizationalUnitLevel:1`

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
[
    {
        "EntityItemId": {
            "S": "OrganizationalUnit:ad11b1d2fe47e7a29288bdb512eefc05"
        },
        "CompositeAccessPatterns": {
            "S": "OrganizationalUnit#OrganizationalUnitLevel:1#OrganizationalUnitName:Managing Director#OrganizationalUnitShortName:MD#OrganizationalUnitParentId:null#OrganizationalUnitParentName:null#OrganizationalUnitManagingRoleId:Role:4d544df22238f1beccca28534e18b0ba"
        },
        "OrganizationalUnitLevel": {
            "N": "1"
        },
        "OrganizationalUnitParentName": {
            "S": "null"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "OrganizationalUnitShortName": {
            "S": "MD"
        },
        "OrganizationalUnitManagingRoleId": {
            "S": "Role:4d544df22238f1beccca28534e18b0ba"
        },
        "OrganizationalUnitName": {
            "S": "Managing Director"
        },
        "OrganizationalUnitParentId": {
            "S": "null"
        }
    }
]
```

## Create a OrganizationalUnit
### HTTP Request
`POST organization-svc/api/v1/organizational-units`

### Body Request

```json
{
    "OrganizationalUnit": {
        "OrganizationalUnitLevel": "3",
        "OrganizationalUnitName": "Manager",
        "OrganizationalUnitShortName": "M",
        "OrganizationalUnitParentId": "OrganizationalUnit:d514910ef21d74a536ded81f47e9ed31",
        "OrganizationalUnitParentName": "DH",
        "OrganizationalUnitManagingRoleId": "Role:5387cd2eff7523044338979d36b4b38c",
        "Children": {
            "EmployeeInCharge": {
                "EmployeeId": "Employee:9a5abe2c2c4ca99e4eb219fbd0b9a319",
                "EmployeeName": "Sreyta Sean"
            }
        }
    }
}
```

### HTTP Response
> The above HTTP request, if successful, will return Json structured like this:

```json
{
    "EntityItemId": {
        "S": "OrganizationalUnit:842a58eb29a6e0651ef72321cb9012d4"
    },
    "CompositeAccessPatterns": {
        "S": "OrganizationalUnit#OrganizationalUnitLevel:3#OrganizationalUnitName:Manager#OrganizationalUnitShortName:M#OrganizationalUnitParentId:OrganizationalUnit:d514910ef21d74a536ded81f47e9ed31#OrganizationalUnitParentName:DH#OrganizationalUnitManagingRoleId:Role:5387cd2eff7523044338979d36b4b38c"
    },
    "OrganizationalUnitLevel": {
        "N": "3"
    },
    "OrganizationalUnitParentName": {
        "S": "DH"
    },
    "TenantId": {
        "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
    },
    "OrganizationalUnitShortName": {
        "S": "M"
    },
    "OrganizationalUnitManagingRoleId": {
        "S": "Role:5387cd2eff7523044338979d36b4b38c"
    },
    "OrganizationalUnitName": {
        "S": "Manager"
    },
    "OrganizationalUnitParentId": {
        "S": "OrganizationalUnit:d514910ef21d74a536ded81f47e9ed31"
    }
}
```

## Update a OrganizationalUnit
### HTTP Request
`PUT organization-svc/api/v1/organizational-units/{item_id}`

### Query Paramaeters
Parameter                   | Description
---------                   | -----------
item_id                     | Is the entity item id of organizationalUnit. EX: OrganizationalUnit:cf89605f7a6536680b5ff7d952394607

### Body Request

```json
{
    "OrganizationalUnit": {
        "OrganizationalUnitLevel": "3",
        "OrganizationalUnitName": "Manager3",
        "OrganizationalUnitShortName": "M",
        "OrganizationalUnitParentId": "OrganizationalUnit:d514910ef21d74a536ded81f47e9ed31",
        "OrganizationalUnitParentName": "DH",
        "OrganizationalUnitManagingRoleId": "Role:5387cd2eff7523044338979d36b4b38c",
        "Children": {
            "EmployeeInCharge": {
                "EmployeeId": "Employee:9a5abe2c2c4ca99e4eb219fbd0b9a319",
                "EmployeeName": "Sreyta Sean3"
            }
        }
    }
}
```

### HTTP Response
> The above HTTP request, if successful, will return Json structured like this:

```json
{
    "EntityItemId": {
        "S": "OrganizationalUnit:842a58eb29a6e0651ef72321cb9012d4"
    },
    "CompositeAccessPatterns": {
        "S": "OrganizationalUnit#OrganizationalUnitLevel:3#OrganizationalUnitName:Manager3#OrganizationalUnitShortName:M#OrganizationalUnitParentId:OrganizationalUnit:d514910ef21d74a536ded81f47e9ed31#OrganizationalUnitParentName:DH#OrganizationalUnitManagingRoleId:Role:5387cd2eff7523044338979d36b4b38c"
    },
    "OrganizationalUnitLevel": {
        "N": "3"
    },
    "OrganizationalUnitParentName": {
        "S": "DH"
    },
    "OrganizationalUnitShortName": {
        "S": "M"
    },
    "TenantId": {
        "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
    },
    "OrganizationalUnitManagingRoleId": {
        "S": "Role:5387cd2eff7523044338979d36b4b38c"
    },
    "OrganizationalUnitName": {
        "S": "Manager3"
    },
    "OrganizationalUnitParentId": {
        "S": "OrganizationalUnit:d514910ef21d74a536ded81f47e9ed31"
    }
}
```

## Delete a OrganizationalUnit
### HTTP Request
`DELETE organization-svc/api/v1/organizational-units/{item_id}`

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
`GET organization-svc/api/v1/job-profiles`

### HTTP Response
> The above HTTP request, if successful, will return Json structured like this:

```json
[
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
]
```

### HTTP Request Filter 
`GET organization-svc/api/v1/job-profiles?contains=JobProfilePositionId:001`

### Query Paramaeters
Parameter                       | Description
---------                       | -----------
JobProfilePositionId            | Is the position id of jobProfile.
JobProfilePositionTitle         | Is the position title of the jobProfile.
JobProfileJobGrade              | Is the job grade of the jobProfile. Ex: 1, 2, 3, 4, 5...

### HTTP Response Filter
> The above HTTP request, if successful, will return Json structured like this:

```json
[
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
]
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
{
    "JobProfileSalaryMax": {
        "S": "2000"
    },
    "EntityItemId": {
        "S": "JobProfile:44c9f8996ff137e201f5de27048d688a"
    },
    "JobProfilePositionId": {
        "S": "001"
    },
    "JobProfileDetail": {
        "N": "112"
    },
    "CompositeAccessPatterns": {
        "S": "JobProfile#JobProfilePositionId:001#JobProfilePositionTitle:Java Team Lead#JobProfileJobGrade:1"
    },
    "JobProfileSalaryMin": {
        "S": "1500"
    },
    "JobProfilePositionTitle": {
        "S": "Java Team Lead"
    },
    "TenantId": {
        "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
    },
    "JobProfileOverview": {
        "N": "111"
    },
    "JobProfileJobGrade": {
        "N": "1"
    },
    "JobProfileWorkingHour": {
        "N": "8"
    }
}
```

## Update a jobProfile
### HTTP Request
`PUT organization-svc/api/v1/job-profiles/{item_id}`

### Query Paramaeters
Parameter                   | Description
---------                   | -----------
item_id                     | Is the entity item id of jobProfile. EX: JobProfile:9a7360586dcc7578cb792b58e3ba6072

### Body Request

```json
{
    "JobProfile": {
        "JobProfilePositionId": "002",
        "JobProfilePositionTitle": "Project Manager",
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
        "S": "JobProfile:44c9f8996ff137e201f5de27048d688a"
    },
    "JobProfileDetail": {
        "N": "112"
    },
    "JobProfilePositionId": {
        "S": "002"
    },
    "CompositeAccessPatterns": {
        "S": "JobProfile#JobProfilePositionId:002#JobProfilePositionTitle:Project Manager#JobProfileJobGrade:1"
    },
    "JobProfileSalaryMin": {
        "S": "1500"
    },
    "JobProfilePositionTitle": {
        "S": "Project Manager"
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
`DELETE organization-svc/api/v1/job-profiles/{item_id}`

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
`GET organization-svc/api/v1/positions`

### HTTP Response
> The above HTTP request, if successful, will return Json structured like this:

```json
[
    {
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "PositionTitleKh": {
            "S": "ហិរញ្ញវត្ថុ"
        },
        "EntityItemId": {
            "S": "Position:80e2f9adf264a144fd43218352bc5153"
        },
        "CompositeAccessPatterns": {
            "S": "Position#PositionTitleEn:Finance#PositionTitleKh:ហិរញ្ញវត្ថុ"
        },
        "PositionTitleEn": {
            "S": "Finance"
        }
    },
    {
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "PositionTitleKh": {
            "S": "ធនធានមនុស្ស"
        },
        "EntityItemId": {
            "S": "Position:9321b71bcbd8e70a3f0d2a73338b4015"
        },
        "CompositeAccessPatterns": {
            "S": "Position#PositionTitleEn:HR#PositionTitleKh:ធនធានមនុស្ស"
        },
        "PositionTitleEn": {
            "S": "HR"
        }
    },
    {
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "PositionTitleKh": {
            "S": "អ្នកគ្រប់គ្រងធនធានមនុស្ស"
        },
        "EntityItemId": {
            "S": "Position:f2581a8d878e61dcb27bf2ef7b505037"
        },
        "CompositeAccessPatterns": {
            "S": "Position#PositionTitleEn:HR Manager#PositionTitleKh:អ្នកគ្រប់គ្រងធនធានមនុស្ស"
        },
        "PositionTitleEn": {
            "S": "HR Manager"
        }
    },
    {
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "PositionTitleKh": {
            "S": "អ្នកសរសេរកម្មវិធី"
        },
        "EntityItemId": {
            "S": "Position:f521a525188a3f4aa04015625b6ce15a"
        },
        "CompositeAccessPatterns": {
            "S": "Position#PositionTitleEn:Programmer#PositionTitleKh:អ្នកសរសេរកម្មវិធី"
        },
        "PositionTitleEn": {
            "S": "Programmer"
        }
    }
]
```

### HTTP Request Filter 
`GET organization-svc/api/v1/positions?contains=PositionTitleEn:Finance`

### Query Paramaeters
Parameter                       | Description
---------                       | -----------
PostionTitleEn                  | Is the title English of the position.
PostionTitleKh                  | Is the title Khmer of the position.

### HTTP Response Filter
> The above HTTP request, if successful, will return Json structured like this:

```json
[
    {
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "PositionTitleKh": {
            "S": "ហិរញ្ញវត្ថុ"
        },
        "EntityItemId": {
            "S": "Position:80e2f9adf264a144fd43218352bc5153"
        },
        "CompositeAccessPatterns": {
            "S": "Position#PositionTitleEn:Finance#PositionTitleKh:ហិរញ្ញវត្ថុ"
        },
        "PositionTitleEn": {
            "S": "Finance"
        }
    }
]
```

## Create a Position
### HTTP Request
`POST organization-svc/api/position`

### Body Request

```json
{
    "Position": {
        "PositionTitleEn": "Programmer",
        "PositionTitleKh": "អ្នកសរសេរកម្មវិធី"
    }
}
```

### HTTP Response
> The above HTTP request, if successful, will return Json structured like this:

```json
{
    "TenantId": {
        "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
    },
    "PositionTitleKh": {
        "S": "អ្នកសរសេរកម្មវិធី"
    },
    "EntityItemId": {
        "S": "Position:4a143322ddfe9918b345021c0240a7c0"
    },
    "CompositeAccessPatterns": {
        "S": "Position#PositionTitleEn:Programmer#PositionTitleKh:អ្នកសរសេរកម្មវិធី"
    },
    "PositionTitleEn": {
        "S": "Programmer"
    }
}
```

## Update a Position
### HTTP Request
`PUT organization-svc/api/v1/positions/{item_id}`

### Query Paramaeters
Parameter                   | Description
---------                   | -----------
item_id                     | Is the entity item id of postion. EX: Postion:18053c214000057310161eb13f4e67d6

### Body Request

```json
{
    "Position": {
        "PositionTitleEn": "Writer",
        "PositionTitleKh": "អ្នកនិពន្ធ"
    }
}
```

### HTTP Response
> The above HTTP request, if successful, will return Json structured like this:

```json
{
    "EntityItemId": {
        "S": "Position:4a143322ddfe9918b345021c0240a7c0"
    },
    "PositionTitleKh": {
        "S": "អ្នកនិពន្ធ"
    },
    "TenantId": {
        "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
    },
    "CompositeAccessPatterns": {
        "S": "Position#PositionTitleEn:Writer#PositionTitleKh:អ្នកនិពន្ធ"
    },
    "PositionTitleEn": {
        "S": "Writer"
    }
}
```

## Delete a Position
### HTTP Request
`DELETE organization-svc/api/v1/positions/{item_id}`

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
`GET organization-svc/api/v1/benefits`

### HTTP Response
> The above HTTP request, if successful, will return Json structured like this:

```json
[
    {
        "BenefitGroupTitleKh": {
            "S": "ប្រាក់ខែ"
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "EntityItemId": {
            "S": "Benefit:c21268600e4c10798746b9e67000bd94"
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
`POST organization-svc/api/v1/benefits`

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
    "TenantId": {
        "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
    },
    "EntityItemId": {
        "S": "Benefit:5bcfff67ab0e203136d08c8b6704e883"
    },
    "CompositeAccessPatterns": {
        "S": "Benefit#BenefitGroupTitleEn:Salary#BenefitGroupTitleKh:ប្រាក់ខែ"
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
    "BenefitGroupTitleEn": {
        "S": "Salary"
    }
}
```

## Update a Benefit
### HTTP Request
`PUT organization-svc/api/v1/benefits/{item_id}`

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
    "TenantId": {
        "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
    },
    "EntityItemId": {
        "S": "Benefit:5bcfff67ab0e203136d08c8b6704e883"
    },
    "CompositeAccessPatterns": {
        "S": "Benefit#BenefitGroupTitleEn:Salary#BenefitGroupTitleKh:ប្រាក់ខែ"
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
    "BenefitGroupTitleEn": {
        "S": "Salary"
    }
}
```

## Delete a Benefit
### HTTP Request
`DELETE organization-svc/api/v1/benefits/{item_id}`

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

# ProcessSetting
## Get All ProcessSetting

### HTTP Request
`GET organization-svc/api/v1/process-settings`

### HTTP Response
> The above HTTP request, if successful, will return Json structured like this:

```json
[
    {
        "ProcessSettingValidationStructure": {
            "L": [
                {
                    "M": {
                        "OrganizationalUnitLevel": {
                            "S": "1"
                        },
                        "Operation": {
                            "L": [
                                {
                                    "S": "dsa:item-operation:Approve"
                                },
                                {
                                    "S": "dsa:item-operation:Return"
                                },
                                {
                                    "S": "dsa:item-operation:Reject"
                                }
                            ]
                        },
                        "ValidatedBy": {
                            "S": "DESIGNATED_OU"
                        },
                        "DesignatedOu": {
                            "S": "OrganizationalUnit:ad11b1d2fe47e7a29288bdb512eefc05"
                        }
                    }
                },
                {
                    "M": {
                        "OrganizationalUnitLevel": {
                            "S": "2"
                        },
                        "Operation": {
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
                        "ValidatedBy": {
                            "S": "PARENT_OU"
                        },
                        "DesignatedOu": {
                            "S": "OrganizationalUnit:ad11b1d2fe47e7a29288bdb512eefc05"
                        }
                    }
                },
                {
                    "M": {
                        "OrganizationalUnitLevel": {
                            "S": "3"
                        },
                        "Operation": {
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
                        "ValidatedBy": {
                            "S": "PARENT_OU"
                        },
                        "DesignatedOu": {
                            "S": "OrganizationalUnit:693a5f054f956b96749c9500203bec62"
                        }
                    }
                }
            ]
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "EntityItemId": {
            "S": "ProcessSetting:4ca2a855020863fac9b394f38f0d3477"
        },
        "ProcessSettingName": {
            "S": "Trip Request"
        },
        "CompositeAccessPatterns": {
            "S": "ProcessSetting#ProcessSettingName:Trip Request"
        },
        "ProcessSettingLifecycle": {
            "L": [
                {
                    "M": {
                        "ItemOperation": {
                            "S": "dsa:item-operation:Submit"
                        },
                        "ProcessState": {
                            "S": "ONGOING"
                        },
                        "ItemDirection": {
                            "S": "MOVE_UP"
                        }
                    }
                },
                {
                    "M": {
                        "ItemOperation": {
                            "S": "dsa:item-operation:Return"
                        },
                        "ProcessState": {
                            "S": "ONGOING"
                        },
                        "ItemDirection": {
                            "S": "RETURN"
                        }
                    }
                },
                {
                    "M": {
                        "ItemOperation": {
                            "S": "dsa:item-operation:Discuss"
                        },
                        "ProcessState": {
                            "S": "ONGOING"
                        },
                        "ItemDirection": {
                            "S": "MOVE_DOWN"
                        }
                    }
                },
                {
                    "M": {
                        "ItemOperation": {
                            "S": "dsa:item-operation:Verify"
                        },
                        "ProcessState": {
                            "S": "ONGOING"
                        },
                        "ItemDirection": {
                            "S": "MOVE_UP"
                        }
                    }
                },
                {
                    "M": {
                        "ItemOperation": {
                            "S": "dsa:item-operation:Reject"
                        },
                        "ProcessState": {
                            "S": "ENDED"
                        },
                        "ItemDirection": {
                            "S": "null"
                        }
                    }
                },
                {
                    "M": {
                        "ItemOperation": {
                            "S": "dsa:item-operation:Approve"
                        },
                        "ProcessState": {
                            "S": "ENDED"
                        },
                        "ItemDirection": {
                            "S": "null"
                        }
                    }
                },
                {
                    "M": {
                        "ItemOperation": {
                            "S": "dsa:item-operation:Revoke"
                        },
                        "ProcessState": {
                            "S": "ENDED"
                        },
                        "ItemDirection": {
                            "S": "null"
                        }
                    }
                }
            ]
        }
    }
]
```

### HTTP Request Filter 
`GET organization-svc/api/v1/process-settings?contains=ProcessSettingName:Trip Request`

### Query Paramaeters
Parameter                       | Description
---------                       | -----------
ProcessSettingName              | Is the name of the process setting.

### HTTP Response Filter
> The above HTTP request, if successful, will return Json structured like this:

```json
[
    {
        "ProcessSettingValidationStructure": {
            "L": [
                {
                    "M": {
                        "OrganizationalUnitLevel": {
                            "S": "1"
                        },
                        "Operation": {
                            "L": [
                                {
                                    "S": "dsa:item-operation:Approve"
                                },
                                {
                                    "S": "dsa:item-operation:Return"
                                },
                                {
                                    "S": "dsa:item-operation:Reject"
                                }
                            ]
                        },
                        "ValidatedBy": {
                            "S": "DESIGNATED_OU"
                        },
                        "DesignatedOu": {
                            "S": "OrganizationalUnit:ad11b1d2fe47e7a29288bdb512eefc05"
                        }
                    }
                },
                {
                    "M": {
                        "OrganizationalUnitLevel": {
                            "S": "2"
                        },
                        "Operation": {
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
                        "ValidatedBy": {
                            "S": "PARENT_OU"
                        },
                        "DesignatedOu": {
                            "S": "OrganizationalUnit:ad11b1d2fe47e7a29288bdb512eefc05"
                        }
                    }
                },
                {
                    "M": {
                        "OrganizationalUnitLevel": {
                            "S": "3"
                        },
                        "Operation": {
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
                        "ValidatedBy": {
                            "S": "PARENT_OU"
                        },
                        "DesignatedOu": {
                            "S": "OrganizationalUnit:693a5f054f956b96749c9500203bec62"
                        }
                    }
                }
            ]
        },
        "TenantId": {
            "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
        },
        "EntityItemId": {
            "S": "ProcessSetting:4ca2a855020863fac9b394f38f0d3477"
        },
        "ProcessSettingName": {
            "S": "Trip Request"
        },
        "CompositeAccessPatterns": {
            "S": "ProcessSetting#ProcessSettingName:Trip Request"
        },
        "ProcessSettingLifecycle": {
            "L": [
                {
                    "M": {
                        "ItemOperation": {
                            "S": "dsa:item-operation:Submit"
                        },
                        "ProcessState": {
                            "S": "ONGOING"
                        },
                        "ItemDirection": {
                            "S": "MOVE_UP"
                        }
                    }
                },
                {
                    "M": {
                        "ItemOperation": {
                            "S": "dsa:item-operation:Return"
                        },
                        "ProcessState": {
                            "S": "ONGOING"
                        },
                        "ItemDirection": {
                            "S": "RETURN"
                        }
                    }
                },
                {
                    "M": {
                        "ItemOperation": {
                            "S": "dsa:item-operation:Discuss"
                        },
                        "ProcessState": {
                            "S": "ONGOING"
                        },
                        "ItemDirection": {
                            "S": "MOVE_DOWN"
                        }
                    }
                },
                {
                    "M": {
                        "ItemOperation": {
                            "S": "dsa:item-operation:Verify"
                        },
                        "ProcessState": {
                            "S": "ONGOING"
                        },
                        "ItemDirection": {
                            "S": "MOVE_UP"
                        }
                    }
                },
                {
                    "M": {
                        "ItemOperation": {
                            "S": "dsa:item-operation:Reject"
                        },
                        "ProcessState": {
                            "S": "ENDED"
                        },
                        "ItemDirection": {
                            "S": "null"
                        }
                    }
                },
                {
                    "M": {
                        "ItemOperation": {
                            "S": "dsa:item-operation:Approve"
                        },
                        "ProcessState": {
                            "S": "ENDED"
                        },
                        "ItemDirection": {
                            "S": "null"
                        }
                    }
                },
                {
                    "M": {
                        "ItemOperation": {
                            "S": "dsa:item-operation:Revoke"
                        },
                        "ProcessState": {
                            "S": "ENDED"
                        },
                        "ItemDirection": {
                            "S": "null"
                        }
                    }
                }
            ]
        }
    }
]
```

## Create a ProcessSetting
### HTTP Request
`POST organization-svc/api/v1/process-settings`

### Body Request

```json
{
    "ProcessSetting": {
        "ProcessSettingName": "Trip Request",
        "Children": {
            "ValidationStructure": [
                {
                    "OrganizationalUnitLevel": "1",
                    "Operation": [
                        "dsa:item-operation:Approve",
                        "dsa:item-operation:Return",
                        "dsa:item-operation:Reject"
                    ],
                    
                    "ValidatedBy": "DESIGNATED_OU",
                    "DesignatedOu": "OrganizationalUnit:ad11b1d2fe47e7a29288bdb512eefc05"
                },
                {
                    "OrganizationalUnitLevel": "2",
                    "Operation": [
                        "dsa:item-operation:Verify",
                        "dsa:item-operation:Return",
                        "dsa:item-operation:Reject"
                    ],
                    "ValidatedBy": "PARENT_OU",
                    "DesignatedOu": "OrganizationalUnit:ad11b1d2fe47e7a29288bdb512eefc05"
                },
                {
                    "OrganizationalUnitLevel": "3",
                    "Operation": [
                        "dsa:item-operation:Verify",
                        "dsa:item-operation:Return",
                        "dsa:item-operation:Reject"
                    ],
                    "ValidatedBy": "PARENT_OU",
                    "DesignatedOu": "OrganizationalUnit:693a5f054f956b96749c9500203bec62"
                }
            ],
            "Lifecycle": [
                {
                    "ItemOperation": "dsa:item-operation:Submit",
                    "ItemDirection": "MOVE_UP",
                    "ProcessState": "ONGOING"
                },
                {
                    "ItemOperation": "dsa:item-operation:Return",
                    "ItemDirection": "RETURN",
                    "ProcessState": "ONGOING"
                },
                {
                    "ItemOperation": "dsa:item-operation:Discuss",
                    "ItemDirection": "MOVE_DOWN",
                    "ProcessState": "ONGOING"
                },
                {
                    "ItemOperation": "dsa:item-operation:Verify",
                    "ItemDirection": "MOVE_UP",
                    "ProcessState": "ONGOING"
                },
                {
                    "ItemOperation": "dsa:item-operation:Reject",
                    "ItemDirection": "null",
                    "ProcessState": "ENDED"
                },
                {
                    "ItemOperation": "dsa:item-operation:Approve",
                    "ItemDirection": "null",
                    "ProcessState": "ENDED"
                },
                {
                    "ItemOperation": "dsa:item-operation:Revoke",
                    "ItemDirection": "null",
                    "ProcessState": "ENDED"
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
    "ProcessSettingValidationStructure": {
        "L": [
            {
                "M": {
                    "OrganizationalUnitLevel": {
                        "S": "1"
                    },
                    "Operation": {
                        "L": [
                            {
                                "S": "dsa:item-operation:Approve"
                            },
                            {
                                "S": "dsa:item-operation:Return"
                            },
                            {
                                "S": "dsa:item-operation:Reject"
                            }
                        ]
                    },
                    "ValidatedBy": {
                        "S": "DESIGNATED_OU"
                    },
                    "DesignatedOu": {
                        "S": "OrganizationalUnit:ad11b1d2fe47e7a29288bdb512eefc05"
                    }
                }
            },
            {
                "M": {
                    "OrganizationalUnitLevel": {
                        "S": "2"
                    },
                    "Operation": {
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
                    "ValidatedBy": {
                        "S": "PARENT_OU"
                    },
                    "DesignatedOu": {
                        "S": "OrganizationalUnit:ad11b1d2fe47e7a29288bdb512eefc05"
                    }
                }
            },
            {
                "M": {
                    "OrganizationalUnitLevel": {
                        "S": "3"
                    },
                    "Operation": {
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
                    "ValidatedBy": {
                        "S": "PARENT_OU"
                    },
                    "DesignatedOu": {
                        "S": "OrganizationalUnit:693a5f054f956b96749c9500203bec62"
                    }
                }
            }
        ]
    },
    "TenantId": {
        "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
    },
    "EntityItemId": {
        "S": "ProcessSetting:5f8508633ddccfa47315dd52e7a2b400"
    },
    "ProcessSettingName": {
        "S": "Trip Request"
    },
    "CompositeAccessPatterns": {
        "S": "ProcessSetting#ProcessSettingName:Trip Request"
    },
    "ProcessSettingLifecycle": {
        "L": [
            {
                "M": {
                    "ItemOperation": {
                        "S": "dsa:item-operation:Submit"
                    },
                    "ProcessState": {
                        "S": "ONGOING"
                    },
                    "ItemDirection": {
                        "S": "MOVE_UP"
                    }
                }
            },
            {
                "M": {
                    "ItemOperation": {
                        "S": "dsa:item-operation:Return"
                    },
                    "ProcessState": {
                        "S": "ONGOING"
                    },
                    "ItemDirection": {
                        "S": "RETURN"
                    }
                }
            },
            {
                "M": {
                    "ItemOperation": {
                        "S": "dsa:item-operation:Discuss"
                    },
                    "ProcessState": {
                        "S": "ONGOING"
                    },
                    "ItemDirection": {
                        "S": "MOVE_DOWN"
                    }
                }
            },
            {
                "M": {
                    "ItemOperation": {
                        "S": "dsa:item-operation:Verify"
                    },
                    "ProcessState": {
                        "S": "ONGOING"
                    },
                    "ItemDirection": {
                        "S": "MOVE_UP"
                    }
                }
            },
            {
                "M": {
                    "ItemOperation": {
                        "S": "dsa:item-operation:Reject"
                    },
                    "ProcessState": {
                        "S": "ENDED"
                    },
                    "ItemDirection": {
                        "S": "null"
                    }
                }
            },
            {
                "M": {
                    "ItemOperation": {
                        "S": "dsa:item-operation:Approve"
                    },
                    "ProcessState": {
                        "S": "ENDED"
                    },
                    "ItemDirection": {
                        "S": "null"
                    }
                }
            },
            {
                "M": {
                    "ItemOperation": {
                        "S": "dsa:item-operation:Revoke"
                    },
                    "ProcessState": {
                        "S": "ENDED"
                    },
                    "ItemDirection": {
                        "S": "null"
                    }
                }
            }
        ]
    }
}
```

## Update a ProcessSetting
### HTTP Request
`PUT organization-svc/api/v1/process-settings/{item_id}`

### Query Paramaeters
Parameter                   | Description
---------                   | -----------
item_id                     | Is the entity item id of process setting. EX: ProcessSetting:5f8508633ddccfa47315dd52e7a2b400

### Body Request

```json
{
    "ProcessSetting": {
        "ProcessSettingName": "Trip Request",
        "Children": {
            "ValidationStructure": [
                {
                    "OrganizationalUnitLevel": "1",
                    "Operation": [
                        "dsa:item-operation:Approve",
                        "dsa:item-operation:Return",
                        "dsa:item-operation:Reject"
                    ],
                    
                    "ValidatedBy": "DESIGNATED_OU",
                    "DesignatedOu": "OrganizationalUnit:ad11b1d2fe47e7a29288bdb512eefc05"
                },
                {
                    "OrganizationalUnitLevel": "2",
                    "Operation": [
                        "dsa:item-operation:Verify",
                        "dsa:item-operation:Return",
                        "dsa:item-operation:Reject"
                    ],
                    "ValidatedBy": "PARENT_OU",
                    "DesignatedOu": "OrganizationalUnit:ad11b1d2fe47e7a29288bdb512eefc05"
                },
                {
                    "OrganizationalUnitLevel": "3",
                    "Operation": [
                        "dsa:item-operation:Verify",
                        "dsa:item-operation:Return",
                        "dsa:item-operation:Reject"
                    ],
                    "ValidatedBy": "PARENT_OU",
                    "DesignatedOu": "OrganizationalUnit:693a5f054f956b96749c9500203bec62"
                }
            ],
            "Lifecycle": [
                {
                    "ItemOperation": "dsa:item-operation:Submit",
                    "ItemDirection": "MOVE_UP",
                    "ProcessState": "ONGOING"
                },
                {
                    "ItemOperation": "dsa:item-operation:Return",
                    "ItemDirection": "RETURN",
                    "ProcessState": "ONGOING"
                },
                {
                    "ItemOperation": "dsa:item-operation:Discuss",
                    "ItemDirection": "MOVE_DOWN",
                    "ProcessState": "ONGOING"
                },
                {
                    "ItemOperation": "dsa:item-operation:Verify",
                    "ItemDirection": "MOVE_UP",
                    "ProcessState": "ONGOING"
                },
                {
                    "ItemOperation": "dsa:item-operation:Reject",
                    "ItemDirection": "null",
                    "ProcessState": "ENDED"
                },
                {
                    "ItemOperation": "dsa:item-operation:Approve",
                    "ItemDirection": "null",
                    "ProcessState": "ENDED"
                },
                {
                    "ItemOperation": "dsa:item-operation:Revoke",
                    "ItemDirection": "null",
                    "ProcessState": "ENDED"
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
    "ProcessSettingValidationStructure": {
        "L": [
            {
                "M": {
                    "OrganizationalUnitLevel": {
                        "S": "1"
                    },
                    "Operation": {
                        "L": [
                            {
                                "S": "dsa:item-operation:Approve"
                            },
                            {
                                "S": "dsa:item-operation:Return"
                            },
                            {
                                "S": "dsa:item-operation:Reject"
                            }
                        ]
                    },
                    "ValidatedBy": {
                        "S": "DESIGNATED_OU"
                    },
                    "DesignatedOu": {
                        "S": "OrganizationalUnit:ad11b1d2fe47e7a29288bdb512eefc05"
                    }
                }
            },
            {
                "M": {
                    "OrganizationalUnitLevel": {
                        "S": "2"
                    },
                    "Operation": {
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
                    "ValidatedBy": {
                        "S": "PARENT_OU"
                    },
                    "DesignatedOu": {
                        "S": "OrganizationalUnit:ad11b1d2fe47e7a29288bdb512eefc05"
                    }
                }
            },
            {
                "M": {
                    "OrganizationalUnitLevel": {
                        "S": "3"
                    },
                    "Operation": {
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
                    "ValidatedBy": {
                        "S": "PARENT_OU"
                    },
                    "DesignatedOu": {
                        "S": "OrganizationalUnit:693a5f054f956b96749c9500203bec62"
                    }
                }
            }
        ]
    },
    "EntityItemId": {
        "S": "ProcessSetting:5f8508633ddccfa47315dd52e7a2b400"
    },
    "TenantId": {
        "S": "TENANT9ed17f0404544dd4977f0a404c4214a2"
    },
    "ProcessSettingName": {
        "S": "Trip Request"
    },
    "CompositeAccessPatterns": {
        "S": "ProcessSetting#ProcessSettingName:Trip Request"
    },
    "ProcessSettingLifecycle": {
        "L": [
            {
                "M": {
                    "ItemOperation": {
                        "S": "dsa:item-operation:Submit"
                    },
                    "ProcessState": {
                        "S": "ONGOING"
                    },
                    "ItemDirection": {
                        "S": "MOVE_UP"
                    }
                }
            },
            {
                "M": {
                    "ItemOperation": {
                        "S": "dsa:item-operation:Return"
                    },
                    "ProcessState": {
                        "S": "ONGOING"
                    },
                    "ItemDirection": {
                        "S": "RETURN"
                    }
                }
            },
            {
                "M": {
                    "ItemOperation": {
                        "S": "dsa:item-operation:Discuss"
                    },
                    "ProcessState": {
                        "S": "ONGOING"
                    },
                    "ItemDirection": {
                        "S": "MOVE_DOWN"
                    }
                }
            },
            {
                "M": {
                    "ItemOperation": {
                        "S": "dsa:item-operation:Verify"
                    },
                    "ProcessState": {
                        "S": "ONGOING"
                    },
                    "ItemDirection": {
                        "S": "MOVE_UP"
                    }
                }
            },
            {
                "M": {
                    "ItemOperation": {
                        "S": "dsa:item-operation:Reject"
                    },
                    "ProcessState": {
                        "S": "ENDED"
                    },
                    "ItemDirection": {
                        "S": "null"
                    }
                }
            },
            {
                "M": {
                    "ItemOperation": {
                        "S": "dsa:item-operation:Approve"
                    },
                    "ProcessState": {
                        "S": "ENDED"
                    },
                    "ItemDirection": {
                        "S": "null"
                    }
                }
            },
            {
                "M": {
                    "ItemOperation": {
                        "S": "dsa:item-operation:Revoke"
                    },
                    "ProcessState": {
                        "S": "ENDED"
                    },
                    "ItemDirection": {
                        "S": "null"
                    }
                }
            }
        ]
    }
}
```

## Delete a ProcessSetting
### HTTP Request
`DELETE organization-svc/api/v1/process-settings/{item_id}`

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
