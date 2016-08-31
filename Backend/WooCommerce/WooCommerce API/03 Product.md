#i2CSMobile : 03 Product

Contains product catalog related functions

##3.1 products : Product List `GET`

Get Products list.

> Supported Parameters

* `slug` [String] Limit result set to products with a specific slug
* `status` [String] Limit result set to products assigned a specific status
* `type` [String] Limit result set to products assigned a specific type
* `category` [String] Limit result set to products assigned a specific category
* `tag` [String] Limit result set to products assigned a specific tag
* `shipping_class` [String] Limit result set to products assigned a specific shipping class
* `attribute` [String] Limit result set to products with a specific attribute
* `attribute_term` [String] Limit result set to products with a specific attribute term (required an assigned attribute)
* `sku` [String] Limit result set to products with a specific SKU
* `featured` [Boolean] Whether to load featured items only

> Success Response

```
[
 {
    "id": 93,
    "name": "Woo Single #1",
    "slug": "woo-single-1",
    "permalink": "http://localhost/wordpress/product/woo-single-1/",
    "date_created": "2013-06-07T11:36:34",
    "date_modified": "2013-06-07T11:36:34",
    "type": "simple",
    "status": "publish",
    "featured": false,
    "catalog_visibility": "visible",
    "description": "<p>Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Vestibulum tortor quam, feugiat vitae, ultricies eget, tempor sit amet, ante. Donec eu libero sit amet quam egestas semper. Aenean ultricies mi vitae est. Mauris placerat eleifend leo.</p>\n",
    "short_description": "<p>Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Vestibulum tortor quam, feugiat vitae, ultricies eget, tempor sit amet, ante. Donec eu libero sit amet quam egestas semper. Aenean ultricies mi vitae est. Mauris placerat eleifend leo.</p>\n",
    "sku": "",
    "price": "3",
    "regular_price": "3",
    "sale_price": "",
    "date_on_sale_from": "",
    "date_on_sale_to": "",
    "price_html": "<span class=\"woocommerce-Price-amount amount\"><span class=\"woocommerce-Price-currencySymbol\">&#36;</span>3.09</span>",
    "on_sale": false,
    "purchasable": true,
    "total_sales": 0,
    "virtual": false,
    "downloadable": true,
    "downloads": [],
    "download_limit": -1,
    "download_expiry": -1,
    "download_type": "standard",
    "external_url": "",
    "button_text": "",
    "tax_status": "taxable",
    "tax_class": "",
    "manage_stock": false,
    "stock_quantity": null,
    "in_stock": true,
    "backorders": "no",
    "backorders_allowed": false,
    "backordered": false,
    "sold_individually": false,
    "weight": "",
    "dimensions": {
      "length": "",
      "width": "",
      "height": ""
    },
    "shipping_required": true,
    "shipping_taxable": true,
    "shipping_class": "",
    "shipping_class_id": 0,
    "reviews_allowed": true,
    "average_rating": "0.00",
    "rating_count": 0,
    "related_ids": [
      90,
      83,
      99,
      87,
      96
    ],
    "upsell_ids": [],
    "cross_sell_ids": [],
    "parent_id": 0,
    "purchase_note": "",
    "categories": [
      {
        "id": 11,
        "name": "Music",
        "slug": "music"
      },
      {
        "id": 13,
        "name": "Singles",
        "slug": "singles"
      }
    ],
    "tags": [],
    "images": [
      {
        "id": 95,
        "date_created": "2013-06-07T11:36:22",
        "date_modified": "2013-06-07T11:36:22",
        "src": "http://localhost/wordpress/wp-content/uploads/2013/06/cd_4_angle.jpg",
        "shop_single": "http://localhost/wordpress/wp-content/uploads/2013/06/cd_4_angle-600x600.jpg",
        "shop_thumbnail": "http://localhost/wordpress/wp-content/uploads/2013/06/cd_4_angle-180x180.jpg",
        "name": "cd_4_angle",
        "alt": "",
        "position": 0
      },
      {
        "id": 94,
        "date_created": "2013-06-07T11:36:10",
        "date_modified": "2013-06-07T11:36:10",
        "src": "http://localhost/wordpress/wp-content/uploads/2013/06/cd_4_flat.jpg",
        "shop_single": "http://localhost/wordpress/wp-content/uploads/2013/06/cd_4_flat-600x600.jpg",
        "shop_thumbnail": "http://localhost/wordpress/wp-content/uploads/2013/06/cd_4_flat-180x180.jpg",
        "name": "cd_4_flat",
        "alt": "",
        "position": 1
      }
    ],
    "attributes": [],
    "default_attributes": [],
    "variations": [],
    "grouped_products": [],
    "menu_order": 0
  },
]
```

##3.2 products/search : Product Search `GET`

Search for products by given term.

> Supported Parameters

* `term` [String] Search term
* `limit` [Number] Number of items per page
* `page` [Number] Page number
* `exclude` [Array] Comma seperated `id` list to exclude from results
* `include` [Array] Comma seperated `id` list to include in results


> Success Response

```
[
  {
    "id": 15,
    "name": "Woo Logo",
    "slug": "woo-logo",
    "permalink": "http://localhost/wordpress/product/woo-logo/",
    "date_created": "2013-06-07T10:35:51",
    "date_modified": "2013-06-07T10:35:51",
    "type": "simple",
    "status": "publish",
    "featured": true,
    "catalog_visibility": "visible",
    "description": "<p>Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Vestibulum tortor quam, feugiat vitae, ultricies eget, tempor sit amet, ante. Donec eu libero sit amet quam egestas semper. Aenean ultricies mi vitae est. Mauris placerat eleifend leo.</p>\n",
    "short_description": "<p>Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Vestibulum tortor quam, feugiat vitae, ultricies eget, tempor sit amet, ante. Donec eu libero sit amet quam egestas semper. Aenean ultricies mi vitae est. Mauris placerat eleifend leo.</p>\n",
    "sku": "",
    "price": "18",
    "regular_price": "20",
    "sale_price": "18",
    "date_on_sale_from": "",
    "date_on_sale_to": "",
    "price_html": "<del><span class=\"woocommerce-Price-amount amount\"><span class=\"woocommerce-Price-currencySymbol\">&#36;</span>20.60</span></del> <ins><span class=\"woocommerce-Price-amount amount\"><span class=\"woocommerce-Price-currencySymbol\">&#36;</span>18.54</span></ins>",
    "on_sale": true,
    "purchasable": true,
    "total_sales": 0,
    "virtual": false,
    "downloadable": false,
    "downloads": [],
    "download_limit": -1,
    "download_expiry": -1,
    "download_type": "standard",
    "external_url": "",
    "button_text": "",
    "tax_status": "taxable",
    "tax_class": "",
    "manage_stock": true,
    "stock_quantity": 5,
    "in_stock": true,
    "backorders": "no",
    "backorders_allowed": false,
    "backordered": false,
    "sold_individually": false,
    "weight": "",
    "dimensions": {
      "length": "",
      "width": "",
      "height": ""
    },
    "shipping_required": true,
    "shipping_taxable": true,
    "shipping_class": "",
    "shipping_class_id": 0,
    "reviews_allowed": true,
    "average_rating": "4.00",
    "rating_count": 1,
    "related_ids": [
      22,
      47,
      31,
      34,
      37
    ],
    "upsell_ids": [
      60
    ],
    "cross_sell_ids": [],
    "parent_id": 0,
    "purchase_note": "",
    "categories": [
      {
        "id": 9,
        "name": "Clothing",
        "slug": "clothing"
      },
      {
        "id": 14,
        "name": "T-shirts",
        "slug": "t-shirts"
      }
    ],
    "tags": [],
    "images": [
      {
        "id": 16,
        "date_created": "2013-06-07T10:35:28",
        "date_modified": "2013-06-07T10:35:28",
        "src": "http://localhost/wordpress/wp-content/uploads/2013/06/T_1_front.jpg",
        "shop_single": "http://localhost/wordpress/wp-content/uploads/2013/06/T_1_front-600x600.jpg",
        "shop_thumbnail": "http://localhost/wordpress/wp-content/uploads/2013/06/T_1_front-180x180.jpg",
        "name": "T_1_front",
        "alt": "",
        "position": 0
      },
      {
        "id": 17,
        "date_created": "2013-06-07T10:35:39",
        "date_modified": "2013-06-07T10:35:39",
        "src": "http://localhost/wordpress/wp-content/uploads/2013/06/T_1_back.jpg",
        "shop_single": "http://localhost/wordpress/wp-content/uploads/2013/06/T_1_back-600x600.jpg",
        "shop_thumbnail": "http://localhost/wordpress/wp-content/uploads/2013/06/T_1_back-180x180.jpg",
        "name": "T_1_back",
        "alt": "",
        "position": 1
      }
    ],
    "attributes": [],
    "default_attributes": [],
    "variations": [],
    "grouped_products": [],
    "menu_order": 0
  }
]
```

##3.3 products/:id : Product Details `[GET]`

Get product details by `id`.

> Success Response

```
{
  "id": 99,
  "name": "Woo Single #2",
  "slug": "woo-single-2",
  "permalink": "http://localhost/wordpress/product/woo-single-2/",
  "date_created": "2013-06-07T11:38:12",
  "date_modified": "2016-08-02T07:10:03",
  "type": "variable",
  "status": "publish",
  "featured": false,
  "catalog_visibility": "visible",
  "description": "<p>Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Vestibulum tortor quam, feugiat vitae, ultricies eget, tempor sit amet, ante. Donec eu libero sit amet quam egestas semper. Aenean ultricies mi vitae est. Mauris placerat eleifend leo.</p>\n",
  "short_description": "<p>Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Vestibulum tortor quam, feugiat vitae, ultricies eget, tempor sit amet, ante. Donec eu libero sit amet quam egestas semper. Aenean ultricies mi vitae est. Mauris placerat eleifend leo.</p>\n",
  "sku": "",
  "price": "3",
  "regular_price": "",
  "sale_price": "",
  "date_on_sale_from": "",
  "date_on_sale_to": "",
  "price_html": "<span class=\"woocommerce-Price-amount amount\"><span class=\"woocommerce-Price-currencySymbol\">&#36;</span>3.09</span>&ndash;<span class=\"woocommerce-Price-amount amount\"><span class=\"woocommerce-Price-currencySymbol\">&#36;</span>6.18</span>",
  "on_sale": false,
  "purchasable": true,
  "total_sales": 31,
  "virtual": false,
  "downloadable": false,
  "downloads": [],
  "download_limit": -1,
  "download_expiry": -1,
  "download_type": "standard",
  "external_url": "",
  "button_text": "",
  "tax_status": "taxable",
  "tax_class": "",
  "manage_stock": false,
  "stock_quantity": null,
  "in_stock": true,
  "backorders": "no",
  "backorders_allowed": false,
  "backordered": false,
  "sold_individually": false,
  "weight": "",
  "dimensions": {
    "length": "",
    "width": "",
    "height": ""
  },
  "shipping_required": true,
  "shipping_taxable": true,
  "shipping_class": "",
  "shipping_class_id": 0,
  "reviews_allowed": true,
  "average_rating": "4.50",
  "rating_count": 2,
  "related_ids": [
    93,
    96,
    90,
    87,
    83
  ],
  "upsell_ids": [],
  "cross_sell_ids": [],
  "parent_id": 0,
  "purchase_note": "",
  "categories": [
    {
      "id": 11,
      "name": "Music",
      "slug": "music"
    },
    {
      "id": 13,
      "name": "Singles",
      "slug": "singles"
    }
  ],
  "tags": [],
  "images": [
    {
      "id": 100,
      "date_created": "2013-06-07T11:37:51",
      "date_modified": "2013-06-07T11:37:51",
      "src": "http://localhost/wordpress/wp-content/uploads/2013/06/cd_6_angle.jpg",
      "shop_single": "http://localhost/wordpress/wp-content/uploads/2013/06/cd_6_angle-600x600.jpg",
      "shop_thumbnail": "http://localhost/wordpress/wp-content/uploads/2013/06/cd_6_angle-180x180.jpg",
      "name": "cd_6_angle",
      "alt": "",
      "position": 0
    },
    {
      "id": 101,
      "date_created": "2013-06-07T11:38:03",
      "date_modified": "2013-06-07T11:38:03",
      "src": "http://localhost/wordpress/wp-content/uploads/2013/06/cd_6_flat.jpg",
      "shop_single": "http://localhost/wordpress/wp-content/uploads/2013/06/cd_6_flat-600x600.jpg",
      "shop_thumbnail": "http://localhost/wordpress/wp-content/uploads/2013/06/cd_6_flat-180x180.jpg",
      "name": "cd_6_flat",
      "alt": "",
      "position": 1
    }
  ],
  "attributes": [
    {
      "id": 1,
      "name": "color",
      "position": 0,
      "visible": true,
      "variation": true,
      "options": [
        "Black",
        "Green",
        "Light Blue @"
      ]
    },
    {
      "id": 2,
      "name": "input something",
      "position": 1,
      "visible": true,
      "variation": true,
      "options": [
        "d",
        "sd"
      ]
    }
  ],
  "default_attributes": [
    {
      "id": 1,
      "name": "color",
      "option": "black"
    },
    {
      "id": 2,
      "name": "input something",
      "option": "d"
    }
  ],
  "variations": [
    {
      "id": 103,
      "date_created": "2016-08-02T06:59:48",
      "date_modified": "2016-08-02T07:16:27",
      "permalink": "http://localhost/wordpress/product/woo-single-2/?attribute_pa_color=green&attribute_pa_input=sd",
      "sku": "",
      "price": "4",
      "regular_price": "4",
      "sale_price": "",
      "date_on_sale_from": "",
      "date_on_sale_to": "",
      "on_sale": false,
      "purchasable": true,
      "visible": true,
      "virtual": false,
      "downloadable": false,
      "downloads": [],
      "download_limit": -1,
      "download_expiry": -1,
      "tax_status": "taxable",
      "tax_class": "",
      "manage_stock": false,
      "stock_quantity": null,
      "in_stock": true,
      "backorders": "no",
      "backorders_allowed": false,
      "backordered": false,
      "weight": "",
      "dimensions": {
        "length": "",
        "width": "",
        "height": ""
      },
      "shipping_class": "",
      "shipping_class_id": 0,
      "image": [
        {
          "id": 100,
          "date_created": "2013-06-07T11:37:51",
          "date_modified": "2013-06-07T11:37:51",
          "src": "http://localhost/wordpress/wp-content/uploads/2013/06/cd_6_angle.jpg",
          "shop_single": "http://localhost/wordpress/wp-content/uploads/2013/06/cd_6_angle-600x600.jpg",
          "shop_thumbnail": "http://localhost/wordpress/wp-content/uploads/2013/06/cd_6_angle-180x180.jpg",
          "name": "cd_6_angle",
          "alt": "",
          "position": 0
        }
      ],
      "attributes": [
        {
          "id": 1,
          "name": "color",
          "option": "green"
        },
        {
          "id": 2,
          "name": "input something",
          "option": "sd"
        }
      ]
    }
  ],
  "grouped_products": [],
  "menu_order": 0
}
```

##3.4 products/categories : Product Categories `[GET]`

Get product categories.

> Success Response

```
[
  {
    "id": 15,
    "name": "Albums",
    "slug": "albums",
    "parent": 11,
    "description": "",
    "display": "default",
    "image": [],
    "menu_order": 0,
    "count": 4
  }
]
```

##3.5 products/:id/reviews : Product Reviews List `[GET]`

Get product reviews.

> Success Response

```
[
  {
    "id": 40,
    "date_created": "2013-06-07T11:58:43",
    "review": "This album proves why The Woo are the best band ever. Best music ever!",
    "rating": 4,
    "name": "Cobus Bester",
    "email": "bester.c@gmail.com",
    "verified": false
  }
]
```

##3.6 products/:id/reviews : Post Product Review `[POST]`

Adds a product reviews.

> Supported Parameters

* `comment` [String] Review comment
* `rating` [Number] Rating value (must be in between 0 - 5)
* `author` [String] Author name (required if not logged in)
* `email` [String] Author email (required if not logged in)

> Success Response

```
[
  {
    "id": 40,
    "date_created": "2013-06-07T11:58:43",
    "review": "This album proves why The Woo are the best band ever. Best music ever!",
    "rating": 4,
    "name": "Cobus Bester",
    "email": "bester.c@gmail.com",
    "verified": false
  }
]
```


