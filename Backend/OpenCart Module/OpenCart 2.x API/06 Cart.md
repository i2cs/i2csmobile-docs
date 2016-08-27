#i2CSMobile : 06 Cart

This contains API calls related to Shopping Cart

##6.1 api2/cart/add : Add Product to Cart

Adds a Product to Shopping Cart

> Supported Parameters

* `product_id` [Number] Product id

* `quantity` [Number] Quantity

* `option` [Array] Product options as an array

Option array should be in the format of `option[product_option_id] = product_option_value_id`. If the product option field of a Product is as follows,

```
"options": [
    {
      "product_option_id": "218",
      "product_option_value": [
        {
          "product_option_value_id": "5",
          "option_value_id": "32",
          "name": "Small",
          "image": null,
          "price": "$12.00",
          "price_prefix": "+"
        }
      ],
      "option_id": "1",
      "name": "Radio",
      "type": "radio",
      "value": "",
      "required": "1"
    }
  ]
```

the `option` array should be,

```
option[218] = 5
```

in the post parameters to select the value `Small`

> Success Response

```
{
  "success": "Success: You have modified your shopping cart!"
}
```
> Error Response

```
{
  "error": {
    "store": "Product can not be bought from the store you have choosen!"
  }
}
```
* Caused by providing non existing `product_id`

```
{
  "error": {
    "option": {
      "225": "Delivery Date required!"
    }
  }
}
```
* Caused by not providing required options

##6.2 api2/cart/products : Get Products of Cart

Get Products of the Shopping Cart

> Success Response

```
{
  "products": [
    {
      "0": "USD",
      "1": "USD",
      "cart_id": "7",
      "product_id": "43",
      "name": "MacBook",
      "model": "Product 16",
      "thumb": "http://localhost/opencart-2.1.0.1/upload/image/cache/catalog/demo/macbook_1-75x75.jpg",
      "option": [],
      "quantity": "2",
      "stock": true,
      "shipping": "0",
      "price": "$602.00",
      "total": "$1,204.00",
      "price_clean": 602,
      "total_clean": 1204,
      "reward": 1200
    }
  ],
  "vouchers": [],
  "totals": [
    {
      "title": "Sub-Total",
      "text": "$1,000.00"
    },
    {
      "title": "Eco Tax (-2.00)",
      "text": "$4.00"
    },
    {
      "title": "VAT (20%)",
      "text": "$200.00"
    },
    {
      "title": "Total",
      "text": "$1,204.00"
    }
  ]
}
```

##6.3 api2/cart/edit : Update Cart

Update Quantity of a Product of the Shopping Cart. No error is returned. `cart_id` is the key given for each cart item. See `cart/products` to find the `cart_id`

> Supported Parameters

* `key` [Number] Cart item id

* `quantity` [Number] New quantity


> Success Response

```
{
  "success": "Success: You have modified your shopping cart!"
}
```

##6.4 api2/cart/remove : Remove Product from Cart

Remove Product from the Shopping Cart

> Supported Parameters

* `key` [Number] Cart item id. `cart_id` is the key given for each cart item. See `cart/products` to find the `cart_id`


> Success Response

```
{
  "success": "Success: You have modified your shopping cart!"
}
```
