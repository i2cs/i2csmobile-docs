#i2CSMobile : 02 Customer Registration

This contains API calls related to Customer Registration 

##2.1 api2/user_register : Create a New Customer 

Registers a new customer to the store. Set default customer group `config_customer_group_id` from store settings to assign new mobile app registered users into one group

> Supported Parameters

* `firstname` [String] Customers first name. must be between 1 and 32 characters

* `lastname` [String] Customers last name. must be between 1 and 32 characters

* `email` [Email] Customers email address. must be a valid email address

* `password` [String] Password. must be between 4 and 20 characters

* `confirm` [String] Password confirmation. should be same as the password

* `telephone` [String] Customers telephone number. must be between 3 and 32 characters

* `address_1` [String] Address line 1. must be between 3 and 128 characters

* `address_2` [String] Address line 2

* `city` [String] Address City. must be between 2 and 128 characters

* `postcode` [String] Postal code

* `country_id` [Number] Country id

* `zone_id` [Number] Zone id

* `customer_group_id` [Number] Customer group id. if none provided `config_customer_group_id` will be assigned

* `newsletter` [Boolean] Sign up for newsletters

> Success Response [returns with `customer_info` field]

```
{
  "customer_info": {
    "customer_id": "3",
    "customer_group_id": "1",
    "store_id": "0",
    "firstname": "Madusha",
    "lastname": "Kumarasiri",
    "email": "i2cs.solutions@gmail.com",
    "telephone": "012345678",
    "fax": "",
    "password": "8574ada50307e3965d5cfd3a1266511e7f6bae50",
    "salt": "Zg6QkoTKH",
    "cart": null,
    "wishlist": null,
    "newsletter": "0",
    "address_id": "3",
    "custom_field": "",
    "ip": "::1",
    "status": "1",
    "approved": "1",
    "safe": "0",
    "token": "",
    "date_added": "2016-07-02 14:52:11"
  },
  "error_warning": "",
  "error_firstname": "",
  "error_lastname": "",
  "error_email": "",
  "error_telephone": "",
  "error_address_1": "",
  "error_city": "",
  "error_postcode": "",
  "error_country": "",
  "error_zone": "",
  "error_custom_field": [],
  "error_password": "",
  "error_confirm": "",
  "customer_group_id": "",
  "firstname": "Madusha",
  "lastname": "Kumarasiri",
  "email": "i2cs.solutions@gmail.com",
  "telephone": "012345678",
  "fax": "",
  "company": "",
  "address_1": "Address Line 1",
  "address_2": "Address Line 2",
  "postcode": "00100",
  "city": "Colombo",
  "country_id": "94",
  "zone_id": "35131",
  "custom_fields": [],
  "register_custom_field": [],
  "password": "123456",
  "confirm": "123456",
  "newsletter": ""
}
```

> Error Response

```
{
  "error_warning": "Warning: E-Mail Address is already registered!",
  "error_firstname": "",
  "error_lastname": "",
  "error_email": "",
  "error_telephone": "",
  "error_address_1": "",
  "error_city": "",
  "error_postcode": "",
  "error_country": "",
  "error_zone": "",
  "error_custom_field": [],
  "error_password": "",
  "error_confirm": "",
  "customer_group_id": "",
  "firstname": "Madusha",
  "lastname": "Kumarasiri",
  "email": "i2cssolutions@gmail.com",
  "telephone": "012345678",
  "fax": "",
  "company": "",
  "address_1": "Address Line 1",
  "address_2": "Address Line 2",
  "postcode": "00100",
  "city": "Colombo",
  "country_id": "94",
  "zone_id": "35131",
  "custom_fields": [],
  "register_custom_field": [],
  "password": "123456",
  "confirm": "123456",
  "newsletter": ""
}
```