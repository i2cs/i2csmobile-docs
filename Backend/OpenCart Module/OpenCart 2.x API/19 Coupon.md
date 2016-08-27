#i2CSMobile : 19 Coupon

This contains API calls related to adding a coupon to the cart

##19.1 api2/coupon : Add Coupon

Adds a coupon to current shopping cart. 

> Supported Parameters

* `coupon` [String] Valid coupon id

> Success Response

```
{
  "success": "Success: Your coupon discount has been applied!"
}
```

> Error Response

```
{
  "error": "Warning: Coupon is either invalid, expired or reached it's usage limit!"
}
```