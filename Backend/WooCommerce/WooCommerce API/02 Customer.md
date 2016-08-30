#i2CSMobile : 02 Customer

Contains customer related functions

##2.1 customers : Customer Registration `POST`

Registeres a new customer.

> Supported Parameters

* `email` [String] Customer email address
* `username` [String] Customer username
* `first_name` [String] First name
* `last_name` [String] Last name
* `password` [String] Password
* `billing[address_1]` [String] Billing address line 1
* `billing[address_2]` [String] Billing address line 2
* `billing[city]` [String] Billing city
* `billing[email]` [String] Customer billing email address
* `billing[first_name]` [String] Billing first name
* `billing[last_name]` [String] Billing last name
* `billing[phone]` [String] Billing phone
* `billing[postcode]` [String] Billing postcode
* `billing[state]` [String] Billing state
* `shipping[address_1]` [String] Shipping address line 1
* `shipping[address_2]` [String] Shipping address line 2
* `shipping[city]` [String] Shipping city
* `shipping[email]` [String] Customer shipping email address
* `shipping[first_name]:` [String] Shipping first name
* `shipping[last_name]` [String] Shipping last name
* `shipping[phone]` [String] Shipping phone
* `shipping[postcode]` [String] Shipping postcode
* `shipping[state]` [String] Shipping state

> Success Response

```
{
  "AF": "Afghanistan",
  "AL": "Albania",
  "US": "United States (US)"
}
```

##2.2 customers/login : Customer Log In `POST`

Logs in a customer by validating by email and password.

> Supported Parameters

* `email` [String] Login email address
* `password` [String] Login password

> Success Response

```
{
  "id": 26,
  "date_created": "2016-08-29T08:03:16",
  "date_modified": "2016-08-29T08:03:17",
  "email": "i2cssolutions@gmail.com",
  "first_name": "John",
  "last_name": "Doe",
  "username": "i2cssolutions@gmail.com",
  "last_order": {
    "id": null,
    "date": null
  },
  "orders_count": 0,
  "total_spent": "0.00",
  "avatar_url": "http://2.gravatar.com/avatar/?s=96",
  "billing": {
    "first_name": "John",
    "last_name": "Doe",
    "company": "",
    "address_1": "Addr 1",
    "address_2": "Addr 1",
    "city": "City",
    "state": "W",
    "postcode": "11850",
    "country": "",
    "email": "i2cssolutions@gmail.com",
    "phone": "0123456789"
  },
  "shipping": {
    "first_name": "John",
    "last_name": "Doe",
    "company": "",
    "address_1": "Addr 1",
    "address_2": "Addr 2",
    "city": "City",
    "state": "W",
    "postcode": "11850",
    "country": ""
  },
  "_links": {
    "self": [
      {
        "href": "http://localhost/wordpress/wp-json/i2cs/v1/customers/26"
      }
    ],
    "collection": [
      {
        "href": "http://localhost/wordpress/wp-json/i2cs/v1/customers"
      }
    ]
  }
}
```

> Error Response

```
{
  "code": "incorrect_password",
  "message": "<strong>ERROR</strong>: The password you entered for the email address <strong>i2cssolutions@gmail.com</strong> is incorrect. <a href=\"http://localhost/wordpress/my-account/lost-password/\">Lost your password?</a>",
  "data": null
}
```
```
{
  "code": "invalid_email",
  "message": "<strong>ERROR</strong>: Invalid email address. <a href=\"http://localhost/wordpress/my-account/lost-password/\">Lost your password?</a>",
  "data": null
}
```
```
{
  "code": "empty_username",
  "message": "<strong>ERROR</strong>: The email field is empty.",
  "data": null,
  "additional_errors": [
    {
      "code": "empty_password",
      "message": "<strong>ERROR</strong>: The password field is empty.",
      "data": null
    }
  ]
}
```

##2.3 customers/logout : Customer Log Out `POST`

Logs out and clears all session data related to customer.

> Success Response

```
    true
```