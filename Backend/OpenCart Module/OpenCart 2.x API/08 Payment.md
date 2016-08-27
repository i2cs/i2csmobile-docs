#i2CSMobile : 08 Payment

This contains API calls related to Payment

##8.1 api2/payment/address : Set Payment Address

Sets the Payment address for current shopping cart order. 

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
{
  "success": "Success: Payment address has been set!"
}
```

##8.2 api2/payment/methods : Get Payment Methods

Returns available Payment methods

> Success Response

```
{
  "payment_methods": {
    "cod": {
      "code": "cod",
      "title": "Cash On Delivery",
      "terms": "",
      "sort_order": "5"
    }
  }
}
```

> Error Response

* Caused by not setting a payment address. Set payment address before executing this method

```
{
  "error": "Warning: Payment address required!"
}
```

##8.3 api2/payment/method : Set Payment Method

Sets the Payment method for current shopping cart order. If cart is empty or does not support shipping, this will return an empty array

> Supported Parameters

* `payment_method` [String] Payment method code, ex : `cod`

> Success Response

```
{
  "success": "Success: Payment method has been set!"
}
```