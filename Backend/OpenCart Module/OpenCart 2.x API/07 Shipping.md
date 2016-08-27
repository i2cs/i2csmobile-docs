#i2CSMobile : 07 Shipping

This contains API calls related to Shipping

##7.1 api2/shipping/address : Set Shipping Address

Sets the Shipping address for current shopping cart order. If cart is empty or does not support shipping, this will return an empty array

> Supported Parameters

* `firstname` [String] Customers first name. must be between 1 and 32 characters

* `lastname` [String] Customers last name. must be between 1 and 32 characters

* `company` [String] Customers company name

* `address_1` [String] Address line 1. must be between 3 and 128 characters

* `address_2` [String] Address line 2

* `city` [String] Address City. must be between 2 and 128 characters

* `postcode` [String] Postal code

* `country_id` [Number] Country id

* `zone_id` [Number] Zone id

> Success Response

```

```

##7.2 api2/shipping/methods : Get Shipping Methods

Returns available Shipping methods for a perticular address. Customer has to enter their shipping address prior executing this method. If cart is empty or does not support shipping, this will return an empty array

> Success Response

```
{
  "shipping_methods": {
    "free": {
      "title": "Free Shipping",
      "quote": {
        "free": {
          "code": "free.free",
          "title": "Free Shipping",
          "cost": 0,
          "tax_class_id": 0,
          "text": "$0.00"
        }
      },
      "sort_order": "",
      "error": false
    }
}
```

##7.3 api2/shipping/method : Set Shipping Method

Sets the Shipping method for current shopping cart order. If cart is empty or does not support shipping, this will return an empty array

> Supported Parameters

* `shipping_method` [String] Shipping method code, ex : `flat`

> Success Response

```
{
  "success": "Success: Shipping method has been set!"
}
```