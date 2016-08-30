#i2CSMobile : 01 Store

Contains meta data of the store. Can use get requests to query for information like countries, currencies etc.

##1.1 store/countries : Get Countries `GET`

Get all allowed countries or shipping countries.

> Supported Parameters

* `shipping` [Boolean] Get Shipping Countries only


> Success Response

```
{
  "AF": "Afghanistan",
  "AL": "Albania",
  "US": "United States (US)"
}
```

##1.2 store/currency : Get Base Currency `GET`

Get base currency of the store.

> Success Response

```
"&#36;"
```

##1.3 store/banner : Get Banner `GET`

Get banner details by `id`. Returns a list of images that are availbale in the banner. Backend must have additional plugin `ml-slide` installed in order to work correctly. On error, returns an empty array.

> Supported Parameters

* `id` [Number] Banner id


> Success Response

```
[
  {
    "title": "promo-banners2",
    "link": "#/app/product/1",
    "image": "http://localhost/wordpress/wp-content/uploads/2016/08/promo-banners2.png"
  },
  {
    "title": "promo-banners1",
    "link": "#/app/product/1",
    "image": "http://localhost/wordpress/wp-content/uploads/2016/08/promo-banners1.png"
  },
  {
    "title": "promo-banners4",
    "link": "#/app/product/1",
    "image": "http://localhost/wordpress/wp-content/uploads/2016/08/promo-banners4.png"
  },
  {
    "title": "promo-banners3",
    "link": "#/app/product/1",
    "image": "http://localhost/wordpress/wp-content/uploads/2016/08/promo-banners3.png"
  }
]
```

##1.4 store/states : Get States `GET`

Get states by country code.

> Supported Parameters

* `cc` [String] Country code. ex, `US`


> Success Response

```
{
  "AL": "Alabama",
  "AK": "Alaska",
  ...
}
```

##1.5 store/language : Set Language `POST`

Set store language.

** Not implemented as it requires 3rd party plugins **

> Supported Parameters

* `language` [String] Language code. ex, `en`
