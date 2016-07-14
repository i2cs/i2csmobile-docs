#i2CSMobile : 12 Featured Products

This contains API calls related to Featured Products

##12.1 api2/featured : Get Featured Products

Returns a list of Featured products. This is populated from selected featured product list from i2CSMobile admin panel


> Supported Parameters

* `width` [Number] Image thumbnail width in pixels. defualt is taken from the Featured module

* `height` [Number] Image thumbnail height in pixels. defualt is taken from the Featured module

> Success Response

```
{
  "heading_title": "Featured",
  "products": [
    {
      "product_id": "42",
      "thumb": "http://localhost/opencart-2.1.0.1/upload/image/cache/catalog/demo/apple_cinema_30-50x50.jpg",
      "name": "Apple Cinema 30&quot;",
      "description": "description",
      "price": "$122.00",
      "price_clear": "100.0000",
      "special": "$110.00",
      "special_clear": "90.0000",
      "mobile_special": false,
      "mobile_special_clear": null,
      "tax": "$90.00",
      "rating": 0,
      "images": [
        "http://localhost/opencart-2.1.0.1/upload/image/cache/catalog/demo/hp_1-100x100.jpg",
        "http://localhost/opencart-2.1.0.1/upload/image/cache/catalog/demo/compaq_presario-100x100.jpg",
        "http://localhost/opencart-2.1.0.1/upload/image/cache/catalog/demo/canon_eos_5d_1-100x100.jpg"
      ]
    }
  ]
}
```

> Error Response

```
[]
```

* Empty response is caused by not setting a Featured module in the i2CSMobile admin panel