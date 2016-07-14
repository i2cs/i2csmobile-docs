#i2CSMobile : 13 Latest Products

This contains API calls related to Latest Products

##13.1 api2/latest : Get Latest Products

Returns a list of products sorted in laters order


> Supported Parameters

* `start` [Number] Start index of products. Used for infinite scroll pagination

* `limit` [Number] Limit products per one request

* `width` [Number] Image thumbnail width in pixels. defualt is `200px`

* `height` [Number] Image thumbnail height in pixels. defualt is `200px`

> Success Response

```
{
  "heading_title": "Latest",
  "products": [
    {
      "product_id": "47",
      "thumb": "http://localhost/opencart-2.1.0.1/upload/image/cache/catalog/demo/hp_1-50x50.jpg",
      "name": "HP LP3065",
      "description": "description",
      "price": "$122.00",
      "price_clear": "100.0000",
      "special": false,
      "special_clear": null,
      "mobile_special": "$26.00",
      "mobile_special_clear": "20.0000",
      "tax": "$100.00",
      "rating": 0,
      "images": [
        "http://localhost/opencart-2.1.0.1/upload/image/cache/catalog/demo/hp_3-100x100.jpg"
      ]
    }
  ]
}
```
