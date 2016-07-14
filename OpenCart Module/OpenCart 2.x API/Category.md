##i2CSMobile : 05 Category

This test will run API calls related to Categories controller

##5.1 api2/category/all : Get All Categories

Get all categories via API. If categories are configured in the i2CSMobile admin panel, the systme returns them. Otherwise returns all categories

> Success Response

```
{
  "category_id": 0,
  "child_id": 0,
  "categories": [
    {
      "category_id": "20",
      "name": "Desktops",
      "image": "http://localhost/opencart-2.1.0.1/upload/image/cache/catalog/demo/compaq_presario-25x25.jpg"
    },
    {
      "category_id": "18",
      "name": "Laptops",
      "image": "http://localhost/opencart-2.1.0.1/upload/image/cache/catalog/demo/hp_2-25x25.jpg"
    },
    {
      "category_id": "25",
      "name": "Components",
      "image": ""
    },
    {
      "category_id": "57",
      "name": "Tablets",
      "image": ""
    },
    {
      "category_id": "17",
      "name": "Software",
      "image": ""
    },
    {
      "category_id": "24",
      "name": "Phones",
      "image": ""
    },
    {
      "category_id": "33",
      "name": "Cameras",
      "image": ""
    },
    {
      "category_id": "34",
      "name": "MP3",
      "image": "http://localhost/opencart-2.1.0.1/upload/image/cache/catalog/demo/ipod_touch_4-25x25.jpg"
    }
  ]
}
```

##5.2 api2/category : Get Products of a Category

Get products of a category via API

> Supported Parameters

* `search` [String] Search products by keywords. Product title field will be searched

* `sort` [String] Sort products by Ex `p.sort_order`

* `order` [String] Order by `ASC` or `DESC`

* `page` [Number] Page number

* `limit` [Number] Number of products to fetch per page. if not provided, `config_product_limit` value will be taken from system

> Success Response

```
{
  "heading_title": "Desktops",
  "text_empty": "There are no products to list in this category.",
  "thumb": "http://localhost/opencart-2.1.0.1/upload/image/cache/catalog/demo/compaq_presario-80x80.jpg",
  "description": "description",
  "categories": [
    {
      "name": "PC",
      "id": "26"
    }
  ],
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
  "sort": "p.sort_order",
  "order": "ASC",
  "limit": 10
}
```