---
title: Live Karaoke API Reference
logo: 'livekaraoke/v1/logo.png'
language_tabs:
  - javascript

toc_footers:
  - <a href='#'>Sign Up for a Developer Key</a>
  - <a href='http://github.com/mpociot/whiteboard'>Documentation Powered by Whiteboard</a>

includes:
  - errors

search: true
---

# Introduction

Welcome to the Live Karaoke API! You can use our API to access Live Karaoke API endpoints, which can get information in our database.

# Environment Variables
### Development
 - HOST: https://content.staging.livekaraoke.net

### Production
 - HOST: https://content.livekaraoke.net




# Authentication


# Phone Number

## Register a new phone number


```javascript
const axios = require('axios');

axios.post(`${HOST}/api/20200907v1/phone`, {
  firstName: 'Fred',
  lastName: 'Flintstone'
})
.then(function (response) {
  console.log(response);
})
.catch(function (error) {
  console.log(error);
});
```

> The above command returns JSON structured like this:

```json
{
  "message": "Phone number created!",
  "data": {
    "data": {
      "pk": 360,
      "phone_number": "0125516221",
      "created_at": "2021-01-28T14:46:18.099194+07:00"
    }
  }
}
```

### HTTP Request

`POST /api/20200907v1/phone`

### Request Body

Parameter | Default | Description
--------- | ------- | -----------
phone_number | 012551622 | Provide a valid phone number.
change_number | false | If set to true, this operation working when the subscriber want to change his/her current phone number.
sms_body | "ប្រើលេខ [CODE] ជាកូដបញ្ជាក់លេខទូរស័ព្ទរបស់អ្នកសំរាប់ Live Karaoke, The Live Singing App from Cambodia។" | 
