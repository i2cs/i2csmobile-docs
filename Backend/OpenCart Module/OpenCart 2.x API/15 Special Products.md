#i2CSMobile : 15 Special Products

This contains API calls related to Special Products

##15.1 api2/special : Get Special Products

Returns a list of Special priced products. If `height` or `width` is not provided, defualt is `200px`

> Supported Parameters

* `start` [Number] Start index of products. Used for infinite scroll pagination

* `limit` [Number] Limit products per one request

* `width` [Number] Image thumbnail width in pixels. defualt is `200px`

* `height` [Number] Image thumbnail height in pixels. defualt is `200px`

> Success Response

```
{
  "heading_title": "Special Offers",
  "text_empty": "There are no special offer products to list.",
  "products": [
    {
      "product_id": "43",
      "thumb": "http://localhost/opencart-2.1.0.1/upload/image/cache/catalog/demo/macbook_1-200x200.jpg",
      "name": "MacBook",
      "description": "description",
      "price": "$602.00",
      "price_clear": "500.0000",
      "special": false,
      "special_clear": null,
      "mobile_special": "$26.00",
      "mobile_special_clear": "20.0000",
      "tax": "$500.00",
      "rating": 0,
      "images": [
        "http://localhost/opencart-2.1.0.1/upload/image/cache/catalog/demo/macbook_2-100x100.jpg",
        "http://localhost/opencart-2.1.0.1/upload/image/cache/catalog/demo/macbook_4-100x100.jpg",
        "http://localhost/opencart-2.1.0.1/upload/image/cache/catalog/demo/macbook_5-100x100.jpg"
      ]
    }
  ]
}
```