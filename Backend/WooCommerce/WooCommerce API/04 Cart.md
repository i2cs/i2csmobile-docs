#i2CSMobile : 04 Cart

Contains cart related functions

##4.1 cart/add : Add to Cart `POST`

Adds a product to cart.

> Supported Parameters

* `product_id` [Number] Product id
* `quantity` [Number] Quantity
* `variation_id` [Number] Variation id

> Success Response

```
{
  "cart": {
    "9f61408e3afb633e50cdf1b20de6f466": {
      "product_id": 56,
      "variation_id": 0,
      "variation": [],
      "quantity": 2,
      "line_total": 70,
      "line_tax": 2.1,
      "line_subtotal": 70,
      "line_subtotal_tax": 2.1,
      "line_tax_data": {
        "total": {
          "1": 2.1
        },
        "subtotal": {
          "1": 2.1
        }
      },
      "data": {
        "id": 56,
        "post": {
          "ID": 56,
          "post_author": "1",
          "post_date": "2013-06-07 11:07:19",
          "post_date_gmt": "2013-06-07 11:07:19",
          "post_content": "Pellentesque habitant.",
          "post_status": "publish",
          "comment_status": "open",
          "ping_status": "closed",
          "post_password": "",
          "post_name": "ninja-silhouette-2",
          "to_ping": "",
          "pinged": "",
          "post_modified": "2013-06-07 11:07:19",
          "post_modified_gmt": "2013-06-07 11:07:19",
          "post_content_filtered": "",
          "post_parent": 0,
          "guid": "http://demo.woothemes.com/woocommerce/?post_type=product&amp;p=56",
          "menu_order": 0,
          "post_type": "product",
          "post_mime_type": "",
          "comment_count": "9",
          "filter": "raw"
        },
        "product_type": "simple",
        "total_stock": null,
        "price": "35",
        "tax_status": "taxable",
        "tax_class": "",
        "virtual": "no"
      },
      "product": {
        "id": 56,
        "name": "Ninja Silhouette",
        "slug": "ninja-silhouette-2",
        "permalink": "http://localhost/wordpress/product/ninja-silhouette-2/",
        "date_created": "2013-06-07T11:07:19",
        "date_modified": "2013-06-07T11:07:19",
        "type": "simple",
        "status": "publish",
        "featured": true,
        "catalog_visibility": "visible",
        "description": "<p>Pellentesque habitant",
        "sku": "",
        "price": "35",
        "regular_price": "35",
        "sale_price": "",
        "date_on_sale_from": "",
        "date_on_sale_to": "",
        "price_html": "<span class=\"woocommerce-Price-amount amount\"><span class=\"woocommerce-Price-currencySymbol\">&#36;</span>36.05</span>",
        "on_sale": false,
        "purchasable": true,
        "total_sales": 13,
        "virtual": false,
        "downloadable": false,
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
        "average_rating": "3.86",
        "rating_count": 7,
        "related_ids": [
          19,
          40,
          37,
          50,
          53
        ],
        "upsell_ids": [],
        "cross_sell_ids": [
          31
        ],
        "parent_id": 0,
        "images": [
          {
            "id": 57,
            "date_created": "2013-06-07T11:06:32",
            "date_modified": "2013-06-07T11:06:32",
            "src": "http://localhost/wordpress/wp-content/uploads/2013/06/hoodie_5_front.jpg",
            "shop_single": "http://localhost/wordpress/wp-content/uploads/2013/06/hoodie_5_front-600x600.jpg",
            "shop_thumbnail": "http://localhost/wordpress/wp-content/uploads/2013/06/hoodie_5_front-180x180.jpg",
            "name": "hoodie_5_front",
            "alt": "",
            "position": 0
          },
          {
            "id": 58,
            "date_created": "2013-06-07T11:07:10",
            "date_modified": "2013-06-07T11:07:10",
            "src": "http://localhost/wordpress/wp-content/uploads/2013/06/hoodie_5_back.jpg",
            "shop_single": "http://localhost/wordpress/wp-content/uploads/2013/06/hoodie_5_back-600x600.jpg",
            "shop_thumbnail": "http://localhost/wordpress/wp-content/uploads/2013/06/hoodie_5_back-180x180.jpg",
            "name": "hoodie_5_back",
            "alt": "",
            "position": 1
          }
        ],
        "attributes": []
      }
    }
  },
  "cart_total": 94.76,
  "cart_subtotal": 84.46,
  "shipping_total": 10,
  "shipping_tax_total": 0.3,
  "subtotal_ex_tax": 82,
  "taxes_total": 2.76,
  "currency": "USD",
  "coupon_discount_amounts": [],
  "_wpnonce": "9c6dfb9ef4"
}
```

##4.2 cart/update_quantity : Update Cart `POST`

Update cart item quantity.

> Supported Parameters

* `cart_key` [String] Cart line key
* `quantity` [Number] New quantity


> Success Response

Update cart item quantity.

> Supported Parameters

* `cart_key` [String] Cart line key
* `quantity` [Number] New quantity


> Success Response

```
{
  "cart": {
    "9f61408e3afb633e50cdf1b20de6f466": {
      "product_id": 56,
      "variation_id": 0,
      "variation": [],
      "quantity": 2,
      "line_total": 70,
      "line_tax": 2.1,
      "line_subtotal": 70,
      "line_subtotal_tax": 2.1,
      "line_tax_data": {
        "total": {
          "1": 2.1
        },
        "subtotal": {
          "1": 2.1
        }
      },
      "data": {
        "id": 56,
        "post": {
          "ID": 56,
          "post_author": "1",
          "post_date": "2013-06-07 11:07:19",
          "post_date_gmt": "2013-06-07 11:07:19",
          "post_content": "Pellentesque habitant.",
          "post_status": "publish",
          "comment_status": "open",
          "ping_status": "closed",
          "post_password": "",
          "post_name": "ninja-silhouette-2",
          "to_ping": "",
          "pinged": "",
          "post_modified": "2013-06-07 11:07:19",
          "post_modified_gmt": "2013-06-07 11:07:19",
          "post_content_filtered": "",
          "post_parent": 0,
          "guid": "http://demo.woothemes.com/woocommerce/?post_type=product&amp;p=56",
          "menu_order": 0,
          "post_type": "product",
          "post_mime_type": "",
          "comment_count": "9",
          "filter": "raw"
        },
        "product_type": "simple",
        "total_stock": null,
        "price": "35",
        "tax_status": "taxable",
        "tax_class": "",
        "virtual": "no"
      },
      "product": {
        "id": 56,
        "name": "Ninja Silhouette",
        "slug": "ninja-silhouette-2",
        "permalink": "http://localhost/wordpress/product/ninja-silhouette-2/",
        "date_created": "2013-06-07T11:07:19",
        "date_modified": "2013-06-07T11:07:19",
        "type": "simple",
        "status": "publish",
        "featured": true,
        "catalog_visibility": "visible",
        "description": "<p>Pellentesque habitant",
        "sku": "",
        "price": "35",
        "regular_price": "35",
        "sale_price": "",
        "date_on_sale_from": "",
        "date_on_sale_to": "",
        "price_html": "<span class=\"woocommerce-Price-amount amount\"><span class=\"woocommerce-Price-currencySymbol\">&#36;</span>36.05</span>",
        "on_sale": false,
        "purchasable": true,
        "total_sales": 13,
        "virtual": false,
        "downloadable": false,
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
        "average_rating": "3.86",
        "rating_count": 7,
        "related_ids": [
          19,
          40,
          37,
          50,
          53
        ],
        "upsell_ids": [],
        "cross_sell_ids": [
          31
        ],
        "parent_id": 0,
        "images": [
          {
            "id": 57,
            "date_created": "2013-06-07T11:06:32",
            "date_modified": "2013-06-07T11:06:32",
            "src": "http://localhost/wordpress/wp-content/uploads/2013/06/hoodie_5_front.jpg",
            "shop_single": "http://localhost/wordpress/wp-content/uploads/2013/06/hoodie_5_front-600x600.jpg",
            "shop_thumbnail": "http://localhost/wordpress/wp-content/uploads/2013/06/hoodie_5_front-180x180.jpg",
            "name": "hoodie_5_front",
            "alt": "",
            "position": 0
          },
          {
            "id": 58,
            "date_created": "2013-06-07T11:07:10",
            "date_modified": "2013-06-07T11:07:10",
            "src": "http://localhost/wordpress/wp-content/uploads/2013/06/hoodie_5_back.jpg",
            "shop_single": "http://localhost/wordpress/wp-content/uploads/2013/06/hoodie_5_back-600x600.jpg",
            "shop_thumbnail": "http://localhost/wordpress/wp-content/uploads/2013/06/hoodie_5_back-180x180.jpg",
            "name": "hoodie_5_back",
            "alt": "",
            "position": 1
          }
        ],
        "attributes": []
      }
    }
  },
  "cart_total": 94.76,
  "cart_subtotal": 84.46,
  "shipping_total": 10,
  "shipping_tax_total": 0.3,
  "subtotal_ex_tax": 82,
  "taxes_total": 2.76,
  "currency": "USD",
  "coupon_discount_amounts": [],
  "_wpnonce": "9c6dfb9ef4"
}
```

##4.3 cart : Get Cart `[GET]`

Get current state of the shopping cart.


> Success Response

```
{
  "cart": {
    "9f61408e3afb633e50cdf1b20de6f466": {
      "product_id": 56,
      "variation_id": 0,
      "variation": [],
      "quantity": 2,
      "line_total": 70,
      "line_tax": 2.1,
      "line_subtotal": 70,
      "line_subtotal_tax": 2.1,
      "line_tax_data": {
        "total": {
          "1": 2.1
        },
        "subtotal": {
          "1": 2.1
        }
      },
      "data": {
        "id": 56,
        "post": {
          "ID": 56,
          "post_author": "1",
          "post_date": "2013-06-07 11:07:19",
          "post_date_gmt": "2013-06-07 11:07:19",
          "post_content": "Pellentesque habitant.",
          "post_status": "publish",
          "comment_status": "open",
          "ping_status": "closed",
          "post_password": "",
          "post_name": "ninja-silhouette-2",
          "to_ping": "",
          "pinged": "",
          "post_modified": "2013-06-07 11:07:19",
          "post_modified_gmt": "2013-06-07 11:07:19",
          "post_content_filtered": "",
          "post_parent": 0,
          "guid": "http://demo.woothemes.com/woocommerce/?post_type=product&amp;p=56",
          "menu_order": 0,
          "post_type": "product",
          "post_mime_type": "",
          "comment_count": "9",
          "filter": "raw"
        },
        "product_type": "simple",
        "total_stock": null,
        "price": "35",
        "tax_status": "taxable",
        "tax_class": "",
        "virtual": "no"
      },
      "product": {
        "id": 56,
        "name": "Ninja Silhouette",
        "slug": "ninja-silhouette-2",
        "permalink": "http://localhost/wordpress/product/ninja-silhouette-2/",
        "date_created": "2013-06-07T11:07:19",
        "date_modified": "2013-06-07T11:07:19",
        "type": "simple",
        "status": "publish",
        "featured": true,
        "catalog_visibility": "visible",
        "description": "<p>Pellentesque habitant",
        "sku": "",
        "price": "35",
        "regular_price": "35",
        "sale_price": "",
        "date_on_sale_from": "",
        "date_on_sale_to": "",
        "price_html": "<span class=\"woocommerce-Price-amount amount\"><span class=\"woocommerce-Price-currencySymbol\">&#36;</span>36.05</span>",
        "on_sale": false,
        "purchasable": true,
        "total_sales": 13,
        "virtual": false,
        "downloadable": false,
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
        "average_rating": "3.86",
        "rating_count": 7,
        "related_ids": [
          19,
          40,
          37,
          50,
          53
        ],
        "upsell_ids": [],
        "cross_sell_ids": [
          31
        ],
        "parent_id": 0,
        "images": [
          {
            "id": 57,
            "date_created": "2013-06-07T11:06:32",
            "date_modified": "2013-06-07T11:06:32",
            "src": "http://localhost/wordpress/wp-content/uploads/2013/06/hoodie_5_front.jpg",
            "shop_single": "http://localhost/wordpress/wp-content/uploads/2013/06/hoodie_5_front-600x600.jpg",
            "shop_thumbnail": "http://localhost/wordpress/wp-content/uploads/2013/06/hoodie_5_front-180x180.jpg",
            "name": "hoodie_5_front",
            "alt": "",
            "position": 0
          },
          {
            "id": 58,
            "date_created": "2013-06-07T11:07:10",
            "date_modified": "2013-06-07T11:07:10",
            "src": "http://localhost/wordpress/wp-content/uploads/2013/06/hoodie_5_back.jpg",
            "shop_single": "http://localhost/wordpress/wp-content/uploads/2013/06/hoodie_5_back-600x600.jpg",
            "shop_thumbnail": "http://localhost/wordpress/wp-content/uploads/2013/06/hoodie_5_back-180x180.jpg",
            "name": "hoodie_5_back",
            "alt": "",
            "position": 1
          }
        ],
        "attributes": []
      }
    }
  },
  "cart_total": 94.76,
  "cart_subtotal": 84.46,
  "shipping_total": 10,
  "shipping_tax_total": 0.3,
  "subtotal_ex_tax": 82,
  "taxes_total": 2.76,
  "currency": "USD",
  "coupon_discount_amounts": [],
  "_wpnonce": "9c6dfb9ef4"
}
```

##4.4 cart/delete : Delete Cart Item `[POST]`

Delete cart item.

> Supported Parameters

* `cart_key` [String] Cart line key


> Success Response

```
{
  "cart": {
    "9f61408e3afb633e50cdf1b20de6f466": {
      "product_id": 56,
      "variation_id": 0,
      "variation": [],
      "quantity": 2,
      "line_total": 70,
      "line_tax": 2.1,
      "line_subtotal": 70,
      "line_subtotal_tax": 2.1,
      "line_tax_data": {
        "total": {
          "1": 2.1
        },
        "subtotal": {
          "1": 2.1
        }
      },
      "data": {
        "id": 56,
        "post": {
          "ID": 56,
          "post_author": "1",
          "post_date": "2013-06-07 11:07:19",
          "post_date_gmt": "2013-06-07 11:07:19",
          "post_content": "Pellentesque habitant.",
          "post_status": "publish",
          "comment_status": "open",
          "ping_status": "closed",
          "post_password": "",
          "post_name": "ninja-silhouette-2",
          "to_ping": "",
          "pinged": "",
          "post_modified": "2013-06-07 11:07:19",
          "post_modified_gmt": "2013-06-07 11:07:19",
          "post_content_filtered": "",
          "post_parent": 0,
          "guid": "http://demo.woothemes.com/woocommerce/?post_type=product&amp;p=56",
          "menu_order": 0,
          "post_type": "product",
          "post_mime_type": "",
          "comment_count": "9",
          "filter": "raw"
        },
        "product_type": "simple",
        "total_stock": null,
        "price": "35",
        "tax_status": "taxable",
        "tax_class": "",
        "virtual": "no"
      },
      "product": {
        "id": 56,
        "name": "Ninja Silhouette",
        "slug": "ninja-silhouette-2",
        "permalink": "http://localhost/wordpress/product/ninja-silhouette-2/",
        "date_created": "2013-06-07T11:07:19",
        "date_modified": "2013-06-07T11:07:19",
        "type": "simple",
        "status": "publish",
        "featured": true,
        "catalog_visibility": "visible",
        "description": "<p>Pellentesque habitant",
        "sku": "",
        "price": "35",
        "regular_price": "35",
        "sale_price": "",
        "date_on_sale_from": "",
        "date_on_sale_to": "",
        "price_html": "<span class=\"woocommerce-Price-amount amount\"><span class=\"woocommerce-Price-currencySymbol\">&#36;</span>36.05</span>",
        "on_sale": false,
        "purchasable": true,
        "total_sales": 13,
        "virtual": false,
        "downloadable": false,
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
        "average_rating": "3.86",
        "rating_count": 7,
        "related_ids": [
          19,
          40,
          37,
          50,
          53
        ],
        "upsell_ids": [],
        "cross_sell_ids": [
          31
        ],
        "parent_id": 0,
        "images": [
          {
            "id": 57,
            "date_created": "2013-06-07T11:06:32",
            "date_modified": "2013-06-07T11:06:32",
            "src": "http://localhost/wordpress/wp-content/uploads/2013/06/hoodie_5_front.jpg",
            "shop_single": "http://localhost/wordpress/wp-content/uploads/2013/06/hoodie_5_front-600x600.jpg",
            "shop_thumbnail": "http://localhost/wordpress/wp-content/uploads/2013/06/hoodie_5_front-180x180.jpg",
            "name": "hoodie_5_front",
            "alt": "",
            "position": 0
          },
          {
            "id": 58,
            "date_created": "2013-06-07T11:07:10",
            "date_modified": "2013-06-07T11:07:10",
            "src": "http://localhost/wordpress/wp-content/uploads/2013/06/hoodie_5_back.jpg",
            "shop_single": "http://localhost/wordpress/wp-content/uploads/2013/06/hoodie_5_back-600x600.jpg",
            "shop_thumbnail": "http://localhost/wordpress/wp-content/uploads/2013/06/hoodie_5_back-180x180.jpg",
            "name": "hoodie_5_back",
            "alt": "",
            "position": 1
          }
        ],
        "attributes": []
      }
    }
  },
  "cart_total": 94.76,
  "cart_subtotal": 84.46,
  "shipping_total": 10,
  "shipping_tax_total": 0.3,
  "subtotal_ex_tax": 82,
  "taxes_total": 2.76,
  "currency": "USD",
  "coupon_discount_amounts": [],
  "_wpnonce": "9c6dfb9ef4"
}
```

##4.5 cart/coupon : Apply Coupon `[POST]`

Apply coupon discount to the cart. Applied coupons will be removed if `coupon_code` is empty

> Supported Parameters

* `coupon_code` [String] Coupon code.


> Success Response

```
{
  "success": "Coupon code applied successfully."
}
```

```
{
  "success": "Coupon code removed successfully."
}
```

> Error Response

```
{
  "error": "Coupon code already applied!"
}
```

```
{
  "error": "Coupon \"11554\" does not exist!"
}
```

##4.6 cart/address : Set Customer Address `[POST]`

Set customer address to calculate shipping and taxes etc.

> Supported Parameters

* `city` [String] City
* `postcode` [String] Postcode
* `state` [String] State
* `country_id` [String] Country code. ex, `US`

> Success Response

```
{
  "cart": {
    "9f61408e3afb633e50cdf1b20de6f466": {
      "product_id": 56,
      "variation_id": 0,
      "variation": [],
      "quantity": 2,
      "line_total": 70,
      "line_tax": 2.1,
      "line_subtotal": 70,
      "line_subtotal_tax": 2.1,
      "line_tax_data": {
        "total": {
          "1": 2.1
        },
        "subtotal": {
          "1": 2.1
        }
      },
      "data": {
        "id": 56,
        "post": {
          "ID": 56,
          "post_author": "1",
          "post_date": "2013-06-07 11:07:19",
          "post_date_gmt": "2013-06-07 11:07:19",
          "post_content": "Pellentesque habitant.",
          "post_status": "publish",
          "comment_status": "open",
          "ping_status": "closed",
          "post_password": "",
          "post_name": "ninja-silhouette-2",
          "to_ping": "",
          "pinged": "",
          "post_modified": "2013-06-07 11:07:19",
          "post_modified_gmt": "2013-06-07 11:07:19",
          "post_content_filtered": "",
          "post_parent": 0,
          "guid": "http://demo.woothemes.com/woocommerce/?post_type=product&amp;p=56",
          "menu_order": 0,
          "post_type": "product",
          "post_mime_type": "",
          "comment_count": "9",
          "filter": "raw"
        },
        "product_type": "simple",
        "total_stock": null,
        "price": "35",
        "tax_status": "taxable",
        "tax_class": "",
        "virtual": "no"
      },
      "product": {
        "id": 56,
        "name": "Ninja Silhouette",
        "slug": "ninja-silhouette-2",
        "permalink": "http://localhost/wordpress/product/ninja-silhouette-2/",
        "date_created": "2013-06-07T11:07:19",
        "date_modified": "2013-06-07T11:07:19",
        "type": "simple",
        "status": "publish",
        "featured": true,
        "catalog_visibility": "visible",
        "description": "<p>Pellentesque habitant",
        "sku": "",
        "price": "35",
        "regular_price": "35",
        "sale_price": "",
        "date_on_sale_from": "",
        "date_on_sale_to": "",
        "price_html": "<span class=\"woocommerce-Price-amount amount\"><span class=\"woocommerce-Price-currencySymbol\">&#36;</span>36.05</span>",
        "on_sale": false,
        "purchasable": true,
        "total_sales": 13,
        "virtual": false,
        "downloadable": false,
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
        "average_rating": "3.86",
        "rating_count": 7,
        "related_ids": [
          19,
          40,
          37,
          50,
          53
        ],
        "upsell_ids": [],
        "cross_sell_ids": [
          31
        ],
        "parent_id": 0,
        "images": [
          {
            "id": 57,
            "date_created": "2013-06-07T11:06:32",
            "date_modified": "2013-06-07T11:06:32",
            "src": "http://localhost/wordpress/wp-content/uploads/2013/06/hoodie_5_front.jpg",
            "shop_single": "http://localhost/wordpress/wp-content/uploads/2013/06/hoodie_5_front-600x600.jpg",
            "shop_thumbnail": "http://localhost/wordpress/wp-content/uploads/2013/06/hoodie_5_front-180x180.jpg",
            "name": "hoodie_5_front",
            "alt": "",
            "position": 0
          },
          {
            "id": 58,
            "date_created": "2013-06-07T11:07:10",
            "date_modified": "2013-06-07T11:07:10",
            "src": "http://localhost/wordpress/wp-content/uploads/2013/06/hoodie_5_back.jpg",
            "shop_single": "http://localhost/wordpress/wp-content/uploads/2013/06/hoodie_5_back-600x600.jpg",
            "shop_thumbnail": "http://localhost/wordpress/wp-content/uploads/2013/06/hoodie_5_back-180x180.jpg",
            "name": "hoodie_5_back",
            "alt": "",
            "position": 1
          }
        ],
        "attributes": []
      }
    }
  },
  "cart_total": 94.76,
  "cart_subtotal": 84.46,
  "shipping_total": 10,
  "shipping_tax_total": 0.3,
  "subtotal_ex_tax": 82,
  "taxes_total": 2.76,
  "currency": "USD",
  "coupon_discount_amounts": [],
  "_wpnonce": "9c6dfb9ef4"
}
```

##4.7 cart/shipping : Get Shipping Methods `[GET]`

Get available shipping methods.


> Success Response

```
{
  "methods": {
    "flat_rate:1": {
      "id": "flat_rate:1",
      "label": "Flat Rate",
      "cost": "10.00",
      "taxes": {
        "1": 0.3
      },
      "method_id": "flat_rate"
    }
  },
  "choosen_method": "flat_rate:1"
}
```

##4.8 cart/shipping : Set Shipping Method `[POST]`

Set shipping method.

> Supported Parameters

* `shipping_method` [String] Selected shipping method code. ex, `flat_rate:1`

> Success Response

```
true
```

##4.9 cart/payment : Get Payment Methods `[GET]`

Get available payment methods.


> Success Response

```
{
  "bacs": {
    "locale": null,
    "order_button_text": null,
    "enabled": "yes",
    "title": "Direct Bank Transfer",
    "description": "Make your payment directly into our bank account. Please use your Order ID as the payment reference. Your order won't be shipped until the funds have cleared in our account.",
    "chosen": null,
    "method_title": "BACS",
    "method_description": "Allows payments by BACS, more commonly known as direct bank/wire transfer.",
    "has_fields": false,
    "countries": null,
    "availability": null,
    "icon": "",
    "supports": [
      "products"
    ],
    "max_amount": 0,
    "view_transaction_url": "",
    "new_method_label": "",
    "plugin_id": "woocommerce_",
    "id": "bacs",
    "errors": [],
    "settings": {
      "enabled": "yes",
      "title": "Direct Bank Transfer",
      "description": "Make your payment directly into our bank account. Please use your Order ID as the payment reference. Your order won't be shipped until the funds have cleared in our account.",
      "instructions": "Make your payment directly into our bank account. Please use your Order ID as the payment reference. Your order won't be shipped until the funds have cleared in our account.",
      "account_name": "",
      "account_number": "",
      "sort_code": "",
      "bank_name": "",
      "iban": "",
      "bic": ""
    },
    "instructions": "Make your payment directly into our bank account. Please use your Order ID as the payment reference. Your order won't be shipped until the funds have cleared in our account.",
    "account_details": [
      {
        "account_name": "",
        "account_number": "",
        "sort_code": "",
        "bank_name": "",
        "iban": "",
        "bic": ""
      }
    ]
  },
  "cheque": {
    "order_button_text": null,
    "enabled": "yes",
    "title": "Check Payments",
    "description": "Please send a check to Store Name, Store Street, Store Town, Store State / County, Store Postcode.",
    "chosen": null,
    "method_title": "Check Payments",
    "method_description": "Allows check payments. Why would you take checks in this day and age? Well you probably wouldn't but it does allow you to make test purchases for testing order emails and the 'success' pages etc.",
    "has_fields": false,
    "countries": null,
    "availability": null,
    "icon": "",
    "supports": [
      "products"
    ],
    "max_amount": 0,
    "view_transaction_url": "",
    "new_method_label": "",
    "plugin_id": "woocommerce_",
    "id": "cheque",
    "errors": [],
    "settings": {
      "enabled": "yes",
      "title": "Check Payments",
      "description": "Please send a check to Store Name, Store Street, Store Town, Store State / County, Store Postcode.",
      "instructions": "Please send a check to Store Name, Store Street, Store Town, Store State / County, Store Postcode."
    },
    "instructions": "Please send a check to Store Name, Store Street, Store Town, Store State / County, Store Postcode."
  },
  "cod": {
    "order_button_text": null,
    "enabled": "yes",
    "title": "Cash on Delivery",
    "description": "Pay with cash upon delivery.",
    "chosen": null,
    "method_title": "Cash on Delivery",
    "method_description": "Have your customers pay with cash (or by other means) upon delivery.",
    "has_fields": false,
    "countries": null,
    "availability": null,
    "icon": "",
    "supports": [
      "products"
    ],
    "max_amount": 0,
    "view_transaction_url": "",
    "new_method_label": "",
    "plugin_id": "woocommerce_",
    "id": "cod",
    "errors": [],
    "settings": {
      "enabled": "yes",
      "title": "Cash on Delivery",
      "description": "Pay with cash upon delivery.",
      "instructions": "Pay with cash upon delivery.",
      "enable_for_methods": [],
      "enable_for_virtual": "yes"
    },
    "instructions": "Pay with cash upon delivery.",
    "enable_for_methods": [],
    "enable_for_virtual": true
  },
  "paypal": {
    "order_button_text": "Proceed to PayPal",
    "enabled": "yes",
    "title": "PayPal",
    "description": "Pay via PayPal; you can pay with your credit card if you don't have a PayPal account.",
    "chosen": null,
    "method_title": "PayPal",
    "method_description": "PayPal standard sends customers to PayPal to enter their payment information. PayPal IPN requires fsockopen/cURL support to update order statuses after payment. Check the <a href=\"http://localhost/wordpress/wp-admin/admin.php?page=wc-status\">system status</a> page for more details.",
    "has_fields": false,
    "countries": null,
    "availability": null,
    "icon": null,
    "supports": [
      "products",
      "refunds"
    ],
    "max_amount": 0,
    "view_transaction_url": "",
    "new_method_label": "",
    "plugin_id": "woocommerce_",
    "id": "paypal",
    "errors": [],
    "settings": {
      "enabled": "yes",
      "email": "poosathecat@gmail.com",
      "title": "PayPal",
      "description": "Pay via PayPal; you can pay with your credit card if you don't have a PayPal account.",
      "testmode": "yes",
      "debug": "no",
      "receiver_email": "poosathecat@gmail.com",
      "identity_token": "",
      "invoice_prefix": "WC-",
      "send_shipping": "no",
      "address_override": "no",
      "paymentaction": "authorization",
      "page_style": "",
      "api_username": "poosathecat_api1.gmail.com"
    },
    "testmode": true,
    "debug": false,
    "email": "poosathecat@gmail.com",
    "receiver_email": "poosathecat@gmail.com",
    "identity_token": ""
  }
}
```

##4.10 cart/payment : Set Payment Method `[POST]`

Set payment method.

> Supported Parameters

* `payment_method` [String] Selected payment method code. ex, `bacs`


> Success Response

```
true
```






