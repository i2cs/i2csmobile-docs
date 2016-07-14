#i2CSMobile : 11 Design

This contains API calls related to Designs and Banners

##11.1 api2/design/banners : Get Banners

Returns Banners/Slideshows of the system. If `banner_id` parametr is passed, it returns the banner identified by the id. Otherwise it returns `main_banner` and `offers_banner` which are configured in the i2CSMobile admin panel.

> Supported Parameters

* `banner_id` [Number] Banner id

* `banner_width` [Number] Banner width in pixels

* `banner_height` [Number] Banner height in pixels


> Success Response

```
{
  "banners": [],
  "main_banners": [
    {
      "title": "MacBookAir",
      "link": "",
      "image": "http://localhost/opencart-2.1.0.1/upload/image/cache/catalog/demo/banners/MacBookAir-1140x380.jpg"
    },
    {
      "title": "iPhone 6",
      "link": "#/app/product/49",
      "image": "http://localhost/opencart-2.1.0.1/upload/image/cache/catalog/demo/banners/iPhone6-1140x380.jpg"
    }
  ],
  "offer_banner": [
    {
      "title": "HP Banner",
      "link": "#/app/product/7",
      "image": "http://localhost/opencart-2.1.0.1/upload/image/cache/catalog/demo/compaq_presario-1140x380.jpg"
    }
  ]
}
```

##11.2 api2/design/offers : Get Offers Banners

Returns Offer Banners/Slideshows which are configured in the i2CSMobile admin panel.

> Success Response

```
{
  "banners": [
    {
      "title": "HP Banner",
      "link": "",
      "image": "http://saasthara.com/i2cs/shops/demo/upload/image/cache/catalog/demo/compaq_presario-1140x380.jpg"
    }
  ]
}
```