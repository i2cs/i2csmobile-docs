#i2CSMobile : 05 Order

Contains order listing and order creation methods.

##5.1 order : Add New Order `[POST]`

Adds a new order. Billing parameters are required.

> Supported Parameters

* `payment_method` [String] Payment method
* `shipping_method` [String] Shipping method
* `billing_first_name` [String] First name
* `billing_last_name` [String] Last name
* `billing_company` [String] Company name
* `billing_email` [String] Email address
* `billing_phone` [String] Phone
* `billing_country` [String] Country
* `billing_address_1` [String] Address line 1
* `billing_address_2` [String] Address line 2
* `billing_city` [String] City
* `billing_state` [String] State
* `billing_postcode` [String] Postcode
* `order_comments` [String] Comments
* `_wpnonce` [String] WP Nonce. Must save from one of previous get cart calls

> Success Response

```
{
  "result": "success",
  "redirect": "http://localhost/wordpress/checkout/order-received/142?key=wc_order_57c52892dd232"
}
```

> Error Response
```
{
  "result": "failure",
  "messages": "<ul class=\"woocommerce-error\">\n\t\t\t<li>We were unable to process your order, please try again.</li>\n\t</ul>\n",
  "refresh": "true",
  "reload": "false"
}
```

##5.2 order : Orders List `[GET]`

Gets previous order list of the current logged in customer. If customer is not logged in, an empty array is returned.


> Success Response

```
[
  {
    "id": 140,
    "parent_id": "",
    "status": "cancelled",
    "order_key": "wc_order_57b967037932d",
    "number": 140,
    "currency": "USD",
    "version": "2.6.4",
    "prices_include_tax": false,
    "date_created": "",
    "date_modified": "",
    "customer_id": 1,
    "discount_total": "0.00",
    "discount_tax": "0.00",
    "shipping_total": "10.00",
    "shipping_tax": "0.30",
    "cart_tax": "1.05",
    "total": "46.35",
    "total_tax": "1.35",
    "billing": {
      "first_name": "John",
      "last_name": "Doe",
      "company": "",
      "address_1": "Line 1",
      "address_2": "Line 2",
      "city": "C",
      "state": "W",
      "postcode": "11850",
      "country": "AF",
      "email": "john@doe.com",
      "phone": "0123456789"
    },
    "shipping": {
      "first_name": "John",
      "last_name": "Doe",
      "company": "",
      "address_1": "Line 1",
      "address_2": "Line 2",
      "city": "C",
      "state": "W",
      "postcode": "11850",
      "country": "AF"
    },
    "payment_method": "paypal",
    "payment_method_title": "PayPal",
    "transaction_id": "",
    "customer_ip_address": "::1",
    "customer_user_agent": "Mozilla/5.0 (Windows NT 10.0; WOW64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/52.0.2743.116 Safari/537.36",
    "created_via": "checkout",
    "customer_note": "",
    "date_completed": "2016-08-21T16:03:29",
    "date_paid": "",
    "cart_hash": "5334b6cbdc239acd6cdea288be527b8a",
    "line_items": [
      {
        "id": 99,
        "name": "Ninja Silhouette",
        "sku": "",
        "product_id": 56,
        "variation_id": 0,
        "quantity": 1,
        "tax_class": "",
        "price": "35.00",
        "subtotal": "35.00",
        "subtotal_tax": "1.05",
        "total": "35.00",
        "total_tax": "1.05",
        "taxes": [
          {
            "id": 1,
            "total": "1.05",
            "subtotal": "1.05"
          }
        ],
        "meta": []
      }
    ],
    "tax_lines": [
      {
        "id": 101,
        "rate_code": "TAX-1",
        "rate_id": "1",
        "label": "Tax",
        "compound": false,
        "tax_total": "1.05",
        "shipping_tax_total": "0.30"
      }
    ],
    "shipping_lines": [
      {
        "id": 100,
        "method_title": "Flat Rate",
        "method_id": "flat_rate:1",
        "total": "10.00",
        "total_tax": "0.30",
        "taxes": [
          {
            "id": 1,
            "total": "0.3"
          }
        ]
      }
    ],
    "fee_lines": [],
    "coupon_lines": [],
    "refunds": []
  }
]
```

##5.3 order : Order Details `[GET]`

Get order details of the current logged in customer.


> Success Response

```
{
    "id": 140,
    "parent_id": "",
    "status": "cancelled",
    "order_key": "wc_order_57b967037932d",
    "number": 140,
    "currency": "USD",
    "version": "2.6.4",
    "prices_include_tax": false,
    "date_created": "",
    "date_modified": "",
    "customer_id": 1,
    "discount_total": "0.00",
    "discount_tax": "0.00",
    "shipping_total": "10.00",
    "shipping_tax": "0.30",
    "cart_tax": "1.05",
    "total": "46.35",
    "total_tax": "1.35",
    "billing": {
      "first_name": "John",
      "last_name": "Doe",
      "company": "",
      "address_1": "Line 1",
      "address_2": "Line 2",
      "city": "C",
      "state": "W",
      "postcode": "11850",
      "country": "AF",
      "email": "john@doe.com",
      "phone": "0123456789"
    },
    "shipping": {
      "first_name": "John",
      "last_name": "Doe",
      "company": "",
      "address_1": "Line 1",
      "address_2": "Line 2",
      "city": "C",
      "state": "W",
      "postcode": "11850",
      "country": "AF"
    },
    "payment_method": "paypal",
    "payment_method_title": "PayPal",
    "transaction_id": "",
    "customer_ip_address": "::1",
    "customer_user_agent": "Mozilla/5.0 (Windows NT 10.0; WOW64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/52.0.2743.116 Safari/537.36",
    "created_via": "checkout",
    "customer_note": "",
    "date_completed": "2016-08-21T16:03:29",
    "date_paid": "",
    "cart_hash": "5334b6cbdc239acd6cdea288be527b8a",
    "line_items": [
      {
        "id": 99,
        "name": "Ninja Silhouette",
        "sku": "",
        "product_id": 56,
        "variation_id": 0,
        "quantity": 1,
        "tax_class": "",
        "price": "35.00",
        "subtotal": "35.00",
        "subtotal_tax": "1.05",
        "total": "35.00",
        "total_tax": "1.05",
        "taxes": [
          {
            "id": 1,
            "total": "1.05",
            "subtotal": "1.05"
          }
        ],
        "meta": []
      }
    ],
    "tax_lines": [
      {
        "id": 101,
        "rate_code": "TAX-1",
        "rate_id": "1",
        "label": "Tax",
        "compound": false,
        "tax_total": "1.05",
        "shipping_tax_total": "0.30"
      }
    ],
    "shipping_lines": [
      {
        "id": 100,
        "method_title": "Flat Rate",
        "method_id": "flat_rate:1",
        "total": "10.00",
        "total_tax": "0.30",
        "taxes": [
          {
            "id": 1,
            "total": "0.3"
          }
        ]
      }
    ],
    "fee_lines": [],
    "coupon_lines": [],
    "refunds": []
  }
```
