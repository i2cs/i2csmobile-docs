#i2CSMobile : 03 Customer Login

This contains API calls related to Customer Login 

##3.1 api2/user_login : Customer Login

Sign in a costomer into the system by email address and password

> Supported Parameters

* `email` [Email] Customers email address. must be a valid email address

* `password` [String] Password. must be between 4 and 20 characters and must match with the account of the email address provided

> Success Response
```
{
  "customer_info": {
    "customer_id": "2",
    "customer_group_id": "1",
    "store_id": "0",
    "firstname": "Madusha",
    "lastname": "Kumarasiri",
    "email": "i2cssolutions@gmail.com",
    "telephone": "012345678",
    "fax": "",
    "cart": null,
    "wishlist": null,
    "newsletter": "0",
    "address_id": "2",
    "custom_field": "",
    "ip": "::1",
    "status": "1",
    "approved": "1",
    "safe": "0",
    "token": "",
    "date_added": "2016-07-02 14:07:06"
  },
  "error_warning": "",
  "success": "",
  "email": "i2cssolutions@gmail.com",
  "password": "123456"
}
```

> Error Response

```
{
  "error_warning": "Warning: No match for E-Mail Address and/or Password.",
  "success": "",
  "email": "i2cssolutions@gmail.com",
  "password": "1234561"
}
```
