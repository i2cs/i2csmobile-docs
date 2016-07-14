#i2CSMobile : 09 Order

This contains API calls related to Orders

##9.1 api2/order/add : Add New Order

Adds a new Order to the system


> Supported Parameters

* `shipping_method` [String] Shipping method if previously not set

* `payment_method` [String] Payment method if previously not set

* `comment` [Number] Image thumbnail width in pixels. defualt is `200px`

* `affiliate_id` [Number] Affiliate id

* `order_status_id` [Number] Order history status id

> Success Response

```
{
  "order_id": 2,
  "success": "Success: You have modified orders!"
}
```

##9.2 api2/order/clear : Order Clear

Clear session data related to shopping cart order

> Success Response

```

```
