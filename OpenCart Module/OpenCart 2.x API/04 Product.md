#i2CSMobile : 04 Product

This test will run API calls related to Product controller

##4.1 api2/product/search : Search for Products

Get a Products matching `search` criteria via API

> Supported Parameters

* `search` [String] Search criteria

* `tag` [String] Tag name to search

* `category_id` [Number] Category id 

* `sub_category` [Number] Sub category id 

* `sort` [String] Sort products by Ex `p.sort_order`

* `order` [String] Order by `ASC` or `DESC`

* `page` [Number] Page number

* `limit` [Number] Number of products to fetch per page. if not provided, `config_product_limit` value will be taken from system

> Success Response

```
{
  "text_empty": "There is no product that matches the search criteria.",
  "products": [
    {
      "product_id": "42",
      "thumb": "http://localhost/opencart-2.1.0.1/upload/image/cache/catalog/demo/apple_cinema_30-228x228.jpg",
      "name": "Apple Cinema 30&quot;",
      "description": "\r\n\tThe 30-inch Apple Cinema HD Display delivers an amazing 2560 x 1600 pixel resolution. Designed sp..",
      "price": "$122.00",
      "price_clear": "100.0000",
      "special": "$110.00",
      "special_clear": "90.0000",
      "mobile_special": false,
      "mobile_special_clear": null,
      "tax": "$90.00",
      "minimum": "2",
      "rating": 0,
      "images": [
        "http://localhost/opencart-2.1.0.1/upload/image/cache/catalog/demo/hp_1-100x100.jpg",
        "http://localhost/opencart-2.1.0.1/upload/image/cache/catalog/demo/compaq_presario-100x100.jpg",
        "http://localhost/opencart-2.1.0.1/upload/image/cache/catalog/demo/canon_eos_5d_1-100x100.jpg"
      ]
    }
  ],
  "search": "apple",
  "description": "apple",
  "category_id": "0",
  "sub_category": "0",
  "sort": "p.sort_order",
  "order": "ASC",
  "limit": 10
}
```

##4.2 api2/product : Get a Product

Get a Product by `product_id` via API

> Supported Parameters

* `product_id` [Number] Id of the product

> Success Response

```
{
  "heading_title": "Apple Cinema 30&quot;",
  "product_id": 42,
  "manufacturer": "Apple",
  "manufacturers": "8",
  "model": "Product 15",
  "reward": "100",
  "points": "400",
  "description": "description",
  "stock": "In Stock",
  "popup": "http://localhost/opencart-2.1.0.1/upload/image/cache/catalog/demo/apple_cinema_30-500x500.jpg",
  "thumb": "http://localhost/opencart-2.1.0.1/upload/image/cache/catalog/demo/apple_cinema_30-228x228.jpg",
  "images": [
    {
      "popup": "http://localhost/opencart-2.1.0.1/upload/image/cache/catalog/demo/canon_logo-500x500.jpg",
      "thumb": "http://localhost/opencart-2.1.0.1/upload/image/cache/catalog/demo/canon_logo-74x74.jpg",
      "preview": "http://localhost/opencart-2.1.0.1/upload/image/cache/catalog/demo/canon_logo-228x228.jpg"
    }
  ],
  "price": "$122.00",
  "special": "$110.00",
  "mobile_special": false,
  "tax": "$90.00",
  "discounts": [
    {
      "quantity": "10",
      "price": "$107.60"
    }
  ],
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
  ],
  "minimum": "2",
  "review_status": "1",
  "review_guest": true,
  "customer_name": "",
  "reviews": "0 reviews",
  "rating": 0,
  "captcha": "",
  "attribute_groups": [
    {
      "attribute_group_id": "6",
      "name": "Processor",
      "attribute": [
        {
          "attribute_id": "3",
          "name": "Clockspeed",
          "text": "100mhz"
        }
      ]
    }
  ],
  "products": [
    {
      "product_id": "40",
      "thumb": "http://localhost/opencart-2.1.0.1/upload/image/cache/catalog/demo/iphone_1-80x80.jpg",
      "name": "iPhone",
      "description": "\r\n\tiPhone is a revolutionary new mobile phone that allows you to make a call by simply tapping a nam..",
      "price": "$123.20",
      "price_clear": "101.0000",
      "special": false,
      "special_clear": null,
      "mobile_special": false,
      "mobile_special_clear": null,
      "tax": "$101.00",
      "minimum": "1",
      "rating": 0,
      "href": "http://localhost/opencart-2.1.0.1/upload/index.php?route=product/product&amp;product_id=40"
    }
  ],
  "tags": [],
  "recurrings": []
}
```
