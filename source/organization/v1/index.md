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