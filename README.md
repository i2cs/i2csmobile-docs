# 14.1 api2/order_history : Order History
  
\-Order list of logged in customer. Has to be a registered customer to return data





> Success Response



\`\`\`

\{

  "orders": \[\]

\}

\`\`\`



  
## Resource URL
  
 \- \[POST\] : [{{url}}?route=api2/order_history]({{url}}?route=api2/order_history)
 
### Request example:
  
	{{url}}?route=api2/order_history  
	  

 
# 2.1 api2/user_register : Create a New Customer 
  
\-Registers a new customer to the store. Set default customer group \`config\_customer\_group\_id\` from store settings to assign new mobile app registered users into one group



> Supported Parameters



\* \`firstname\` \[String\] Customers first name. must be between 1 and 32 characters



\* \`lastname\` \[String\] Customers last name. must be between 1 and 32 characters



\* \`email\` \[Email\] Customers email address. must be a valid email address



\* \`password\` \[String\] Password. must be between 4 and 20 characters



\* \`confirm\` \[String\] Password confirmation. should be same as the password



\* \`telephone\` \[String\] Customers telephone number. must be between 3 and 32 characters



\* \`address\_1\` \[String\] Address line 1. must be between 3 and 128 characters



\* \`address\_2\` \[String\] Address line 2



\* \`city\` \[String\] Address City. must be between 2 and 128 characters



\* \`postcode\` \[String\] Postal code



\* \`country\_id\` \[Number\] Country id



\* \`zone\_id\` \[Number\] Zone id



\* \`customer\_group\_id\` \[Number\] Customer group id. if none provided \`config\_customer\_group\_id\` will be assigned



\* \`newsletter\` \[Boolean\] Sign up for newsletters



> Success Response \[returns with \`customer\_info\` field\]



\`\`\`

\{

  "customer\_info": \{

    "customer\_id": "3",

    "customer\_group\_id": "1",

    "store\_id": "0",

    "firstname": "Madusha",

    "lastname": "Kumarasiri",

    "email": "i2cs.solutions@gmail.com",

    "telephone": "012345678",

    "fax": "",

    "password": "8574ada50307e3965d5cfd3a1266511e7f6bae50",

    "salt": "Zg6QkoTKH",

    "cart": null,

    "wishlist": null,

    "newsletter": "0",

    "address\_id": "3",

    "custom\_field": "",

    "ip": "::1",

    "status": "1",

    "approved": "1",

    "safe": "0",

    "token": "",

    "date\_added": "2016\-07\-02 14:52:11"

  \},

  "error\_warning": "",

  "error\_firstname": "",

  "error\_lastname": "",

  "error\_email": "",

  "error\_telephone": "",

  "error\_address\_1": "",

  "error\_city": "",

  "error\_postcode": "",

  "error\_country": "",

  "error\_zone": "",

  "error\_custom\_field": \[\],

  "error\_password": "",

  "error\_confirm": "",

  "customer\_group\_id": "",

  "firstname": "Madusha",

  "lastname": "Kumarasiri",

  "email": "i2cs.solutions@gmail.com",

  "telephone": "012345678",

  "fax": "",

  "company": "",

  "address\_1": "Address Line 1",

  "address\_2": "Address Line 2",

  "postcode": "00100",

  "city": "Colombo",

  "country\_id": "94",

  "zone\_id": "35131",

  "custom\_fields": \[\],

  "register\_custom\_field": \[\],

  "password": "123456",

  "confirm": "123456",

  "newsletter": ""

\}

\`\`\`



> Error Response



\`\`\`

\{

  "error\_warning": "Warning: E\-Mail Address is already registered\!",

  "error\_firstname": "",

  "error\_lastname": "",

  "error\_email": "",

  "error\_telephone": "",

  "error\_address\_1": "",

  "error\_city": "",

  "error\_postcode": "",

  "error\_country": "",

  "error\_zone": "",

  "error\_custom\_field": \[\],

  "error\_password": "",

  "error\_confirm": "",

  "customer\_group\_id": "",

  "firstname": "Madusha",

  "lastname": "Kumarasiri",

  "email": "i2cssolutions@gmail.com",

  "telephone": "012345678",

  "fax": "",

  "company": "",

  "address\_1": "Address Line 1",

  "address\_2": "Address Line 2",

  "postcode": "00100",

  "city": "Colombo",

  "country\_id": "94",

  "zone\_id": "35131",

  "custom\_fields": \[\],

  "register\_custom\_field": \[\],

  "password": "123456",

  "confirm": "123456",

  "newsletter": ""

\}

\`\`\`  
## Resource URL
  
 \- \[POST\] : [{{url}}?route=api2/user_register]({{url}}?route=api2/user_register)
 
## Request Parameters
  
name              | type | example value          
------------------|------|------------------------
firstname         | text | Madusha                
lastname          | text | Kumarasiri             
email             | text | i2cssolutions@gmail.com
password          | text | 123456                 
confirm           | text | 123456                 
telephone         | text | 012345678              
address_1         | text | Address Line 1         
address_2         | text | Address Line 2         
city              | text | Colombo                
postcode          | text | 00100                  
country_id        | text | 94                     
zone_id           | text | 35131                  
customer_group_id | text |                        
agree             | text | 1                      

 
### Request example:
  
	{{url}}?route=api2/user_register  
	city=Colombo&zone_id=35131&firstname=Madusha&confirm=123456&lastname=Kumarasiri&country_id=94&telephone=012345678&agree=1&customer_group_id=&address_1=Address+Line+1&address_2=Address+Line+2&password=123456&email=i2cssolutions%40gmail.com&postcode=00100  

 
# 9.1 api2/order/add : Add New Order
  
\-Adds a new Order to the system





> Supported Parameters



\* \`shipping\_method\` \[String\] Shipping method if previously not set



\* \`payment\_method\` \[String\] Payment method if previously not set



\* \`comment\` \[Number\] Image thumbnail width in pixels. defualt is \`200px\`



\* \`affiliate\_id\` \[Number\] Affiliate id



\* \`order\_status\_id\` \[Number\] Order history status id



> Success Response



\`\`\`

\{

  "order\_id": 2,

  "success": "Success: You have modified orders\!"

\}

\`\`\`



  
## Resource URL
  
 \- \[POST\] : [{{url}}?route=api2/order/add]({{url}}?route=api2/order/add)
 
## Request Parameters
  
name            | type | example value   
----------------|------|-----------------
shipping_method | text |                 
payment_method  | text |                 
comment         | text | customer comment
affiliate_id    | text |                 

 
### Request example:
  
	{{url}}?route=api2/order/add  
	payment_method=&comment=customer+comment&affiliate_id=&shipping_method=  

 
# 8.2 api2/payment/methods : Get Payment Methods
  
\-Returns available Payment methods



> Success Response



\`\`\`

\{

  "payment\_methods": \{

    "cod": \{

      "code": "cod",

      "title": "Cash On Delivery",

      "terms": "",

      "sort\_order": "5"

    \}

  \}

\}

\`\`\`



> Error Response



\* Caused by not setting a payment address. Set payment address before executing this method



\`\`\`

\{

  "error": "Warning: Payment address required\!"

\}

\`\`\`  
## Resource URL
  
 \- \[POST\] : [{{url}}?route=api2/payment/methods]({{url}}?route=api2/payment/methods)
 
### Request example:
  
	{{url}}?route=api2/payment/methods  
	  

 
# 8.3 api2/payment/method : Set Payment Method
  
\-Sets the Payment method for current shopping cart order. If cart is empty or does not support shipping, this will return an empty array



> Supported Parameters



\* \`payment\_method\` \[String\] Payment method code, ex : \`cod\`



> Success Response



\`\`\`

\{

  "success": "Success: Payment method has been set\!"

\}

\`\`\`  
## Resource URL
  
 \- \[POST\] : [{{url}}?route=api2/payment/method]({{url}}?route=api2/payment/method)
 
## Request Parameters
  
name           | type | example value
---------------|------|--------------
payment_method | text | cod          
               | text |              

 
### Request example:
  
	{{url}}?route=api2/payment/method  
	payment_method=cod&=  

 
# 4.1 api2/product/search : Search for Products
  
\-Get a Products matching \`search\` criteria via API



> Supported Parameters



\* \`search\` \[String\] Search criteria



\* \`tag\` \[String\] Tag name to search



\* \`category\_id\` \[Number\] Category id 



\* \`sub\_category\` \[Number\] Sub category id 



\* \`sort\` \[String\] Sort products by Ex \`p.sort\_order\`



\* \`order\` \[String\] Order by \`ASC\` or \`DESC\`



\* \`page\` \[Number\] Page number



\* \`limit\` \[Number\] Number of products to fetch per page. if not provided, \`config\_product\_limit\` value will be taken from system



> Success Response



\`\`\`

\{

  "text\_empty": "There is no product that matches the search criteria.",

  "products": \[

    \{

      "product\_id": "42",

      "thumb": "http://localhost/opencart\-2.1.0.1/upload/image/cache/catalog/demo/apple\_cinema\_30\-228x228.jpg",

      "name": "Apple Cinema 30&amp;quot;",

      "description": "\r\n\tThe 30\-inch Apple Cinema HD Display delivers an amazing 2560 x 1600 pixel resolution. Designed sp..",

      "price": "$122.00",

      "price\_clear": "100.0000",

      "special": "$110.00",

      "special\_clear": "90.0000",

      "mobile\_special": false,

      "mobile\_special\_clear": null,

      "tax": "$90.00",

      "minimum": "2",

      "rating": 0,

      "images": \[

        "http://localhost/opencart\-2.1.0.1/upload/image/cache/catalog/demo/hp\_1\-100x100.jpg",

        "http://localhost/opencart\-2.1.0.1/upload/image/cache/catalog/demo/compaq\_presario\-100x100.jpg",

        "http://localhost/opencart\-2.1.0.1/upload/image/cache/catalog/demo/canon\_eos\_5d\_1\-100x100.jpg"

      \]

    \}

  \],

  "search": "apple",

  "description": "apple",

  "category\_id": "0",

  "sub\_category": "0",

  "sort": "p.sort\_order",

  "order": "ASC",

  "limit": 10

\}

\`\`\`  
## Resource URL
  
 \- \[POST\] : [{{url}}?route=api2/product/search]({{url}}?route=api2/product/search)
 
## Request Parameters
  
name         | type | example value
-------------|------|--------------
search       | text | sony         
tag          | text |              
category_id  | text | 0            
sub_category | text | 0            
sort         | text | p.sort_order 
order        | text | ASC          
page         | text | 1            
limit        | text | 10           

 
### Request example:
  
	{{url}}?route=api2/product/search  
	sort=p.sort_order&search=sony&sub_category=0&page=1&tag=&limit=10&category_id=0&order=ASC  

 
# 3.1 api2/user_login : Customer Login
  
\-Sign in a costomer into the system by email address and password



> Supported Parameters



\* \`email\` \[Email\] Customers email address. must be a valid email address



\* \`password\` \[String\] Password. must be between 4 and 20 characters and must match with the account of the email address provided



> Success Response

\`\`\`

\{

  "customer\_info": \{

    "customer\_id": "2",

    "customer\_group\_id": "1",

    "store\_id": "0",

    "firstname": "Madusha",

    "lastname": "Kumarasiri",

    "email": "i2cssolutions@gmail.com",

    "telephone": "012345678",

    "fax": "",

    "cart": null,

    "wishlist": null,

    "newsletter": "0",

    "address\_id": "2",

    "custom\_field": "",

    "ip": "::1",

    "status": "1",

    "approved": "1",

    "safe": "0",

    "token": "",

    "date\_added": "2016\-07\-02 14:07:06"

  \},

  "error\_warning": "",

  "success": "",

  "email": "i2cssolutions@gmail.com",

  "password": "123456"

\}

\`\`\`



> Error Response



\`\`\`

\{

  "error\_warning": "Warning: No match for E\-Mail Address and/or Password.",

  "success": "",

  "email": "i2cssolutions@gmail.com",

  "password": "1234561"

\}

\`\`\`  
## Resource URL
  
 \- \[POST\] : [{{url}}?route=api2/user_login]({{url}}?route=api2/user_login)
 
## Request Parameters
  
name     | type | example value          
---------|------|------------------------
email    | text | i2cssolutions@gmail.com
password | text | 123456                 
         | text |                        

 
### Request example:
  
	{{url}}?route=api2/user_login  
	=&password=123456&email=i2cssolutions%40gmail.com  

 
# 4.2 api2/product : Get a Product
  
\-Get a Product by \`product\_id\` via API

> Supported Parameters

\* \`product\_id\` \[Number\] Id of the product

> Success Response

\`\`\`
\{
  "heading\_title": "Apple Cinema 30&amp;quot;",
  "product\_id": 42,
  "manufacturer": "Apple",
  "manufacturers": "8",
  "model": "Product 15",
  "reward": "100",
  "points": "400",
  "description": "description",
  "stock": "In Stock",
  "popup": "http://localhost/opencart\-2.1.0.1/upload/image/cache/catalog/demo/apple\_cinema\_30\-500x500.jpg",
  "thumb": "http://localhost/opencart\-2.1.0.1/upload/image/cache/catalog/demo/apple\_cinema\_30\-228x228.jpg",
  "images": \[
    \{
      "popup": "http://localhost/opencart\-2.1.0.1/upload/image/cache/catalog/demo/canon\_logo\-500x500.jpg",
      "thumb": "http://localhost/opencart\-2.1.0.1/upload/image/cache/catalog/demo/canon\_logo\-74x74.jpg",
      "preview": "http://localhost/opencart\-2.1.0.1/upload/image/cache/catalog/demo/canon\_logo\-228x228.jpg"
    \}
  \],
  "price": "$122.00",
  "special": "$110.00",
  "mobile\_special": false,
  "tax": "$90.00",
  "discounts": \[
    \{
      "quantity": "10",
      "price": "$107.60"
    \}
  \],
  "options": \[
    \{
      "product\_option\_id": "218",
      "product\_option\_value": \[
        \{
          "product\_option\_value\_id": "5",
          "option\_value\_id": "32",
          "name": "Small",
          "image": null,
          "price": "$12.00",
          "price\_prefix": "\+"
        \}
      \],
      "option\_id": "1",
      "name": "Radio",
      "type": "radio",
      "value": "",
      "required": "1"
    \}
  \],
  "minimum": "2",
  "review\_status": "1",
  "review\_guest": true,
  "customer\_name": "",
  "reviews": "0 reviews",
  "rating": 0,
  "captcha": "",
  "attribute\_groups": \[
    \{
      "attribute\_group\_id": "6",
      "name": "Processor",
      "attribute": \[
        \{
          "attribute\_id": "3",
          "name": "Clockspeed",
          "text": "100mhz"
        \}
      \]
    \}
  \],
  "products": \[
    \{
      "product\_id": "40",
      "thumb": "http://localhost/opencart\-2.1.0.1/upload/image/cache/catalog/demo/iphone\_1\-80x80.jpg",
      "name": "iPhone",
      "description": "\r\n\tiPhone is a revolutionary new mobile phone that allows you to make a call by simply tapping a nam..",
      "price": "$123.20",
      "price\_clear": "101.0000",
      "special": false,
      "special\_clear": null,
      "mobile\_special": false,
      "mobile\_special\_clear": null,
      "tax": "$101.00",
      "minimum": "1",
      "rating": 0,
      "href": "http://localhost/opencart\-2.1.0.1/upload/index.php?route=product/product&amp;amp;product\_id=40"
    \}
  \],
  "tags": \[\],
  "recurrings": \[\]
\}
\`\`\`  
## Resource URL
  
 \- \[POST\] : [{{url}}?route=api2/product]({{url}}?route=api2/product)
 
## Request Parameters
  
name       | type | example value 
-----------|------|---------------
product_id | text | {{product_id}}

 
### Request example:
  
	{{url}}?route=api2/product  
	product_id=%7B%7Bproduct_id%7D%7D  

 
# 7.3 api2/shipping/method : Set Shipping Method
  
\-Sets the Shipping method for current shopping cart order. If cart is empty or does not support shipping, this will return an empty array



> Supported Parameters



\* \`shipping\_method\` \[String\] Shipping method code, ex : \`flat\`



> Success Response



\`\`\`

\{

  "success": "Success: Shipping method has been set\!"

\}

\`\`\`  
## Resource URL
  
 \- \[POST\] : [{{url}}?route=api2/shipping/method]({{url}}?route=api2/shipping/method)
 
## Request Parameters
  
name            | type | example value
----------------|------|--------------
shipping_method | text | flat.flat    

 
### Request example:
  
	{{url}}?route=api2/shipping/method  
	shipping_method=flat.flat  

 
# 5.2 api2/category : Get Products of a Category
  
\-Get products of a category via API

> Supported Parameters

\* \`search\` \[String\] Search products by keywords. Product title field will be searched

\* \`sort\` \[String\] Sort products by Ex \`p.sort\_order\`

\* \`order\` \[String\] Order by \`ASC\` or \`DESC\`

\* \`page\` \[Number\] Page number

\* \`limit\` \[Number\] Number of products to fetch per page. if not provided, \`config\_product\_limit\` value will be taken from system

> Success Response

\`\`\`
\{
  "heading\_title": "Desktops",
  "text\_empty": "There are no products to list in this category.",
  "thumb": "http://localhost/opencart\-2.1.0.1/upload/image/cache/catalog/demo/compaq\_presario\-80x80.jpg",
  "description": "description",
  "categories": \[
    \{
      "name": "PC",
      "id": "26"
    \}
  \],
  "products": \[
    \{
      "product\_id": "42",
      "thumb": "http://localhost/opencart\-2.1.0.1/upload/image/cache/catalog/demo/apple\_cinema\_30\-228x228.jpg",
      "name": "Apple Cinema 30&amp;quot;",
      "description": "\r\n\tThe 30\-inch Apple Cinema HD Display delivers an amazing 2560 x 1600 pixel resolution. Designed sp..",
      "price": "$122.00",
      "price\_clear": "100.0000",
      "special": "$110.00",
      "special\_clear": "90.0000",
      "mobile\_special": false,
      "mobile\_special\_clear": null,
      "tax": "$90.00",
      "minimum": "2",
      "rating": 0,
      "images": \[
        "http://localhost/opencart\-2.1.0.1/upload/image/cache/catalog/demo/hp\_1\-100x100.jpg",
        "http://localhost/opencart\-2.1.0.1/upload/image/cache/catalog/demo/compaq\_presario\-100x100.jpg",
        "http://localhost/opencart\-2.1.0.1/upload/image/cache/catalog/demo/canon\_eos\_5d\_1\-100x100.jpg"
      \]
    \}
  \],
  "sort": "p.sort\_order",
  "order": "ASC",
  "limit": 10
\}
\`\`\`  
## Resource URL
  
 \- \[POST\] : [{{url}}?route=api2/category]({{url}}?route=api2/category)
 
## Request Parameters
  
name   | type | example value  
-------|------|----------------
path   | text | {{category_id}}
search | text | apple          
sort   | text | p.sort_order   
order  | text | ASC            
page   | text | 1              
limit  | text | 10             

 
### Request example:
  
	{{url}}?route=api2/category  
	sort=p.sort_order&search=apple&page=1&limit=10&path=%7B%7Bcategory_id%7D%7D&order=ASC  

 
# 16.2 api2/address/getZones: Get Zones
  
\-Returns a list of Zones of a given Country. \`country\_id\` field is required







> Supported Parameters



\* \`country\_id\` \[Number\] Country id







> Success Response



\`\`\`

\{

  "zones": \[

    \{

      "zone\_id": "1388",

      "country\_id": "94",

      "name": "Flat Island",

      "code": "F",

      "status": "1"

    \},

    \{

      "zone\_id": "1391",

      "country\_id": "94",

      "name": "Heard Island",

      "code": "H",

      "status": "1"

    \},

    \{

      "zone\_id": "1389",

      "country\_id": "94",

      "name": "McDonald Island",

      "code": "M",

      "status": "1"

    \},

    \{

      "zone\_id": "1390",

      "country\_id": "94",

      "name": "Shag Island",

      "code": "S",

      "status": "1"

    \}

  \]

\}

\`\`\`  
## Resource URL
  
 \- \[POST\] : [{{url}}?route=api2/address/getZones]({{url}}?route=api2/address/getZones)
 
## Request Parameters
  
name       | type | example value
-----------|------|--------------
country_id | text | 94           

 
### Request example:
  
	{{url}}?route=api2/address/getZones  
	country_id=94  

 
# 14.1 api2/order_history : Order History
  
\-Order list of logged in customer. Has to be a registered customer to return data





> Success Response



\`\`\`

\{

  "orders": \[\]

\}

\`\`\`



  
## Resource URL
  
 \- \[POST\] : [{{url}}?route=api2/order_history]({{url}}?route=api2/order_history)
 
### Request example:
  
	{{url}}?route=api2/order_history  
	  

 
# 2.1 api2/user_register : Create a New Customer 
  
\-Registers a new customer to the store. Set default customer group \`config\_customer\_group\_id\` from store settings to assign new mobile app registered users into one group



> Supported Parameters



\* \`firstname\` \[String\] Customers first name. must be between 1 and 32 characters



\* \`lastname\` \[String\] Customers last name. must be between 1 and 32 characters



\* \`email\` \[Email\] Customers email address. must be a valid email address



\* \`password\` \[String\] Password. must be between 4 and 20 characters



\* \`confirm\` \[String\] Password confirmation. should be same as the password



\* \`telephone\` \[String\] Customers telephone number. must be between 3 and 32 characters



\* \`address\_1\` \[String\] Address line 1. must be between 3 and 128 characters



\* \`address\_2\` \[String\] Address line 2



\* \`city\` \[String\] Address City. must be between 2 and 128 characters



\* \`postcode\` \[String\] Postal code



\* \`country\_id\` \[Number\] Country id



\* \`zone\_id\` \[Number\] Zone id



\* \`customer\_group\_id\` \[Number\] Customer group id. if none provided \`config\_customer\_group\_id\` will be assigned



\* \`newsletter\` \[Boolean\] Sign up for newsletters



> Success Response \[returns with \`customer\_info\` field\]



\`\`\`

\{

  "customer\_info": \{

    "customer\_id": "3",

    "customer\_group\_id": "1",

    "store\_id": "0",

    "firstname": "Madusha",

    "lastname": "Kumarasiri",

    "email": "i2cs.solutions@gmail.com",

    "telephone": "012345678",

    "fax": "",

    "password": "8574ada50307e3965d5cfd3a1266511e7f6bae50",

    "salt": "Zg6QkoTKH",

    "cart": null,

    "wishlist": null,

    "newsletter": "0",

    "address\_id": "3",

    "custom\_field": "",

    "ip": "::1",

    "status": "1",

    "approved": "1",

    "safe": "0",

    "token": "",

    "date\_added": "2016\-07\-02 14:52:11"

  \},

  "error\_warning": "",

  "error\_firstname": "",

  "error\_lastname": "",

  "error\_email": "",

  "error\_telephone": "",

  "error\_address\_1": "",

  "error\_city": "",

  "error\_postcode": "",

  "error\_country": "",

  "error\_zone": "",

  "error\_custom\_field": \[\],

  "error\_password": "",

  "error\_confirm": "",

  "customer\_group\_id": "",

  "firstname": "Madusha",

  "lastname": "Kumarasiri",

  "email": "i2cs.solutions@gmail.com",

  "telephone": "012345678",

  "fax": "",

  "company": "",

  "address\_1": "Address Line 1",

  "address\_2": "Address Line 2",

  "postcode": "00100",

  "city": "Colombo",

  "country\_id": "94",

  "zone\_id": "35131",

  "custom\_fields": \[\],

  "register\_custom\_field": \[\],

  "password": "123456",

  "confirm": "123456",

  "newsletter": ""

\}

\`\`\`



> Error Response



\`\`\`

\{

  "error\_warning": "Warning: E\-Mail Address is already registered\!",

  "error\_firstname": "",

  "error\_lastname": "",

  "error\_email": "",

  "error\_telephone": "",

  "error\_address\_1": "",

  "error\_city": "",

  "error\_postcode": "",

  "error\_country": "",

  "error\_zone": "",

  "error\_custom\_field": \[\],

  "error\_password": "",

  "error\_confirm": "",

  "customer\_group\_id": "",

  "firstname": "Madusha",

  "lastname": "Kumarasiri",

  "email": "i2cssolutions@gmail.com",

  "telephone": "012345678",

  "fax": "",

  "company": "",

  "address\_1": "Address Line 1",

  "address\_2": "Address Line 2",

  "postcode": "00100",

  "city": "Colombo",

  "country\_id": "94",

  "zone\_id": "35131",

  "custom\_fields": \[\],

  "register\_custom\_field": \[\],

  "password": "123456",

  "confirm": "123456",

  "newsletter": ""

\}

\`\`\`  
## Resource URL
  
 \- \[POST\] : [{{url}}?route=api2/user_register]({{url}}?route=api2/user_register)
 
## Request Parameters
  
name              | type | example value          
------------------|------|------------------------
firstname         | text | Madusha                
lastname          | text | Kumarasiri             
email             | text | i2cssolutions@gmail.com
password          | text | 123456                 
confirm           | text | 123456                 
telephone         | text | 012345678              
address_1         | text | Address Line 1         
address_2         | text | Address Line 2         
city              | text | Colombo                
postcode          | text | 00100                  
country_id        | text | 94                     
zone_id           | text | 35131                  
customer_group_id | text |                        
agree             | text | 1                      

 
### Request example:
  
	{{url}}?route=api2/user_register  
	city=Colombo&zone_id=35131&firstname=Madusha&confirm=123456&lastname=Kumarasiri&country_id=94&telephone=012345678&agree=1&customer_group_id=&address_1=Address+Line+1&address_2=Address+Line+2&password=123456&email=i2cssolutions%40gmail.com&postcode=00100  

 
# 9.1 api2/order/add : Add New Order
  
\-Adds a new Order to the system





> Supported Parameters



\* \`shipping\_method\` \[String\] Shipping method if previously not set



\* \`payment\_method\` \[String\] Payment method if previously not set



\* \`comment\` \[Number\] Image thumbnail width in pixels. defualt is \`200px\`



\* \`affiliate\_id\` \[Number\] Affiliate id



\* \`order\_status\_id\` \[Number\] Order history status id



> Success Response



\`\`\`

\{

  "order\_id": 2,

  "success": "Success: You have modified orders\!"

\}

\`\`\`



  
## Resource URL
  
 \- \[POST\] : [{{url}}?route=api2/order/add]({{url}}?route=api2/order/add)
 
## Request Parameters
  
name            | type | example value   
----------------|------|-----------------
shipping_method | text |                 
payment_method  | text |                 
comment         | text | customer comment
affiliate_id    | text |                 

 
### Request example:
  
	{{url}}?route=api2/order/add  
	payment_method=&comment=customer+comment&affiliate_id=&shipping_method=  

 
# 8.2 api2/payment/methods : Get Payment Methods
  
\-Returns available Payment methods



> Success Response



\`\`\`

\{

  "payment\_methods": \{

    "cod": \{

      "code": "cod",

      "title": "Cash On Delivery",

      "terms": "",

      "sort\_order": "5"

    \}

  \}

\}

\`\`\`



> Error Response



\* Caused by not setting a payment address. Set payment address before executing this method



\`\`\`

\{

  "error": "Warning: Payment address required\!"

\}

\`\`\`  
## Resource URL
  
 \- \[POST\] : [{{url}}?route=api2/payment/methods]({{url}}?route=api2/payment/methods)
 
### Request example:
  
	{{url}}?route=api2/payment/methods  
	  

 
# 8.3 api2/payment/method : Set Payment Method
  
\-Sets the Payment method for current shopping cart order. If cart is empty or does not support shipping, this will return an empty array



> Supported Parameters



\* \`payment\_method\` \[String\] Payment method code, ex : \`cod\`



> Success Response



\`\`\`

\{

  "success": "Success: Payment method has been set\!"

\}

\`\`\`  
## Resource URL
  
 \- \[POST\] : [{{url}}?route=api2/payment/method]({{url}}?route=api2/payment/method)
 
## Request Parameters
  
name           | type | example value
---------------|------|--------------
payment_method | text | cod          
               | text |              

 
### Request example:
  
	{{url}}?route=api2/payment/method  
	payment_method=cod&=  

 
# 4.1 api2/product/search : Search for Products
  
\-Get a Products matching \`search\` criteria via API



> Supported Parameters



\* \`search\` \[String\] Search criteria



\* \`tag\` \[String\] Tag name to search



\* \`category\_id\` \[Number\] Category id 



\* \`sub\_category\` \[Number\] Sub category id 



\* \`sort\` \[String\] Sort products by Ex \`p.sort\_order\`



\* \`order\` \[String\] Order by \`ASC\` or \`DESC\`



\* \`page\` \[Number\] Page number



\* \`limit\` \[Number\] Number of products to fetch per page. if not provided, \`config\_product\_limit\` value will be taken from system



> Success Response



\`\`\`

\{

  "text\_empty": "There is no product that matches the search criteria.",

  "products": \[

    \{

      "product\_id": "42",

      "thumb": "http://localhost/opencart\-2.1.0.1/upload/image/cache/catalog/demo/apple\_cinema\_30\-228x228.jpg",

      "name": "Apple Cinema 30&amp;quot;",

      "description": "\r\n\tThe 30\-inch Apple Cinema HD Display delivers an amazing 2560 x 1600 pixel resolution. Designed sp..",

      "price": "$122.00",

      "price\_clear": "100.0000",

      "special": "$110.00",

      "special\_clear": "90.0000",

      "mobile\_special": false,

      "mobile\_special\_clear": null,

      "tax": "$90.00",

      "minimum": "2",

      "rating": 0,

      "images": \[

        "http://localhost/opencart\-2.1.0.1/upload/image/cache/catalog/demo/hp\_1\-100x100.jpg",

        "http://localhost/opencart\-2.1.0.1/upload/image/cache/catalog/demo/compaq\_presario\-100x100.jpg",

        "http://localhost/opencart\-2.1.0.1/upload/image/cache/catalog/demo/canon\_eos\_5d\_1\-100x100.jpg"

      \]

    \}

  \],

  "search": "apple",

  "description": "apple",

  "category\_id": "0",

  "sub\_category": "0",

  "sort": "p.sort\_order",

  "order": "ASC",

  "limit": 10

\}

\`\`\`  
## Resource URL
  
 \- \[POST\] : [{{url}}?route=api2/product/search]({{url}}?route=api2/product/search)
 
## Request Parameters
  
name         | type | example value
-------------|------|--------------
search       | text | sony         
tag          | text |              
category_id  | text | 0            
sub_category | text | 0            
sort         | text | p.sort_order 
order        | text | ASC          
page         | text | 1            
limit        | text | 10           

 
### Request example:
  
	{{url}}?route=api2/product/search  
	sort=p.sort_order&search=sony&sub_category=0&page=1&tag=&limit=10&category_id=0&order=ASC  

 
# 3.1 api2/user_login : Customer Login
  
\-Sign in a costomer into the system by email address and password



> Supported Parameters



\* \`email\` \[Email\] Customers email address. must be a valid email address



\* \`password\` \[String\] Password. must be between 4 and 20 characters and must match with the account of the email address provided



> Success Response

\`\`\`

\{

  "customer\_info": \{

    "customer\_id": "2",

    "customer\_group\_id": "1",

    "store\_id": "0",

    "firstname": "Madusha",

    "lastname": "Kumarasiri",

    "email": "i2cssolutions@gmail.com",

    "telephone": "012345678",

    "fax": "",

    "cart": null,

    "wishlist": null,

    "newsletter": "0",

    "address\_id": "2",

    "custom\_field": "",

    "ip": "::1",

    "status": "1",

    "approved": "1",

    "safe": "0",

    "token": "",

    "date\_added": "2016\-07\-02 14:07:06"

  \},

  "error\_warning": "",

  "success": "",

  "email": "i2cssolutions@gmail.com",

  "password": "123456"

\}

\`\`\`



> Error Response



\`\`\`

\{

  "error\_warning": "Warning: No match for E\-Mail Address and/or Password.",

  "success": "",

  "email": "i2cssolutions@gmail.com",

  "password": "1234561"

\}

\`\`\`  
## Resource URL
  
 \- \[POST\] : [{{url}}?route=api2/user_login]({{url}}?route=api2/user_login)
 
## Request Parameters
  
name     | type | example value          
---------|------|------------------------
email    | text | i2cssolutions@gmail.com
password | text | 123456                 
         | text |                        

 
### Request example:
  
	{{url}}?route=api2/user_login  
	=&password=123456&email=i2cssolutions%40gmail.com  

 
# 4.2 api2/product : Get a Product
  
\-Get a Product by \`product\_id\` via API

> Supported Parameters

\* \`product\_id\` \[Number\] Id of the product

> Success Response

\`\`\`
\{
  "heading\_title": "Apple Cinema 30&amp;quot;",
  "product\_id": 42,
  "manufacturer": "Apple",
  "manufacturers": "8",
  "model": "Product 15",
  "reward": "100",
  "points": "400",
  "description": "description",
  "stock": "In Stock",
  "popup": "http://localhost/opencart\-2.1.0.1/upload/image/cache/catalog/demo/apple\_cinema\_30\-500x500.jpg",
  "thumb": "http://localhost/opencart\-2.1.0.1/upload/image/cache/catalog/demo/apple\_cinema\_30\-228x228.jpg",
  "images": \[
    \{
      "popup": "http://localhost/opencart\-2.1.0.1/upload/image/cache/catalog/demo/canon\_logo\-500x500.jpg",
      "thumb": "http://localhost/opencart\-2.1.0.1/upload/image/cache/catalog/demo/canon\_logo\-74x74.jpg",
      "preview": "http://localhost/opencart\-2.1.0.1/upload/image/cache/catalog/demo/canon\_logo\-228x228.jpg"
    \}
  \],
  "price": "$122.00",
  "special": "$110.00",
  "mobile\_special": false,
  "tax": "$90.00",
  "discounts": \[
    \{
      "quantity": "10",
      "price": "$107.60"
    \}
  \],
  "options": \[
    \{
      "product\_option\_id": "218",
      "product\_option\_value": \[
        \{
          "product\_option\_value\_id": "5",
          "option\_value\_id": "32",
          "name": "Small",
          "image": null,
          "price": "$12.00",
          "price\_prefix": "\+"
        \}
      \],
      "option\_id": "1",
      "name": "Radio",
      "type": "radio",
      "value": "",
      "required": "1"
    \}
  \],
  "minimum": "2",
  "review\_status": "1",
  "review\_guest": true,
  "customer\_name": "",
  "reviews": "0 reviews",
  "rating": 0,
  "captcha": "",
  "attribute\_groups": \[
    \{
      "attribute\_group\_id": "6",
      "name": "Processor",
      "attribute": \[
        \{
          "attribute\_id": "3",
          "name": "Clockspeed",
          "text": "100mhz"
        \}
      \]
    \}
  \],
  "products": \[
    \{
      "product\_id": "40",
      "thumb": "http://localhost/opencart\-2.1.0.1/upload/image/cache/catalog/demo/iphone\_1\-80x80.jpg",
      "name": "iPhone",
      "description": "\r\n\tiPhone is a revolutionary new mobile phone that allows you to make a call by simply tapping a nam..",
      "price": "$123.20",
      "price\_clear": "101.0000",
      "special": false,
      "special\_clear": null,
      "mobile\_special": false,
      "mobile\_special\_clear": null,
      "tax": "$101.00",
      "minimum": "1",
      "rating": 0,
      "href": "http://localhost/opencart\-2.1.0.1/upload/index.php?route=product/product&amp;amp;product\_id=40"
    \}
  \],
  "tags": \[\],
  "recurrings": \[\]
\}
\`\`\`  
## Resource URL
  
 \- \[POST\] : [{{url}}?route=api2/product]({{url}}?route=api2/product)
 
## Request Parameters
  
name       | type | example value 
-----------|------|---------------
product_id | text | {{product_id}}

 
### Request example:
  
	{{url}}?route=api2/product  
	product_id=%7B%7Bproduct_id%7D%7D  

 
# 7.3 api2/shipping/method : Set Shipping Method
  
\-Sets the Shipping method for current shopping cart order. If cart is empty or does not support shipping, this will return an empty array



> Supported Parameters



\* \`shipping\_method\` \[String\] Shipping method code, ex : \`flat\`



> Success Response



\`\`\`

\{

  "success": "Success: Shipping method has been set\!"

\}

\`\`\`  
## Resource URL
  
 \- \[POST\] : [{{url}}?route=api2/shipping/method]({{url}}?route=api2/shipping/method)
 
## Request Parameters
  
name            | type | example value
----------------|------|--------------
shipping_method | text | flat.flat    

 
### Request example:
  
	{{url}}?route=api2/shipping/method  
	shipping_method=flat.flat  

 
# 5.2 api2/category : Get Products of a Category
  
\-Get products of a category via API

> Supported Parameters

\* \`search\` \[String\] Search products by keywords. Product title field will be searched

\* \`sort\` \[String\] Sort products by Ex \`p.sort\_order\`

\* \`order\` \[String\] Order by \`ASC\` or \`DESC\`

\* \`page\` \[Number\] Page number

\* \`limit\` \[Number\] Number of products to fetch per page. if not provided, \`config\_product\_limit\` value will be taken from system

> Success Response

\`\`\`
\{
  "heading\_title": "Desktops",
  "text\_empty": "There are no products to list in this category.",
  "thumb": "http://localhost/opencart\-2.1.0.1/upload/image/cache/catalog/demo/compaq\_presario\-80x80.jpg",
  "description": "description",
  "categories": \[
    \{
      "name": "PC",
      "id": "26"
    \}
  \],
  "products": \[
    \{
      "product\_id": "42",
      "thumb": "http://localhost/opencart\-2.1.0.1/upload/image/cache/catalog/demo/apple\_cinema\_30\-228x228.jpg",
      "name": "Apple Cinema 30&amp;quot;",
      "description": "\r\n\tThe 30\-inch Apple Cinema HD Display delivers an amazing 2560 x 1600 pixel resolution. Designed sp..",
      "price": "$122.00",
      "price\_clear": "100.0000",
      "special": "$110.00",
      "special\_clear": "90.0000",
      "mobile\_special": false,
      "mobile\_special\_clear": null,
      "tax": "$90.00",
      "minimum": "2",
      "rating": 0,
      "images": \[
        "http://localhost/opencart\-2.1.0.1/upload/image/cache/catalog/demo/hp\_1\-100x100.jpg",
        "http://localhost/opencart\-2.1.0.1/upload/image/cache/catalog/demo/compaq\_presario\-100x100.jpg",
        "http://localhost/opencart\-2.1.0.1/upload/image/cache/catalog/demo/canon\_eos\_5d\_1\-100x100.jpg"
      \]
    \}
  \],
  "sort": "p.sort\_order",
  "order": "ASC",
  "limit": 10
\}
\`\`\`  
## Resource URL
  
 \- \[POST\] : [{{url}}?route=api2/category]({{url}}?route=api2/category)
 
## Request Parameters
  
name   | type | example value  
-------|------|----------------
path   | text | {{category_id}}
search | text | apple          
sort   | text | p.sort_order   
order  | text | ASC            
page   | text | 1              
limit  | text | 10             

 
### Request example:
  
	{{url}}?route=api2/category  
	sort=p.sort_order&search=apple&page=1&limit=10&path=%7B%7Bcategory_id%7D%7D&order=ASC  

 
# 16.2 api2/address/getZones: Get Zones
  
\-Returns a list of Zones of a given Country. \`country\_id\` field is required







> Supported Parameters



\* \`country\_id\` \[Number\] Country id







> Success Response



\`\`\`

\{

  "zones": \[

    \{

      "zone\_id": "1388",

      "country\_id": "94",

      "name": "Flat Island",

      "code": "F",

      "status": "1"

    \},

    \{

      "zone\_id": "1391",

      "country\_id": "94",

      "name": "Heard Island",

      "code": "H",

      "status": "1"

    \},

    \{

      "zone\_id": "1389",

      "country\_id": "94",

      "name": "McDonald Island",

      "code": "M",

      "status": "1"

    \},

    \{

      "zone\_id": "1390",

      "country\_id": "94",

      "name": "Shag Island",

      "code": "S",

      "status": "1"

    \}

  \]

\}

\`\`\`  
## Resource URL
  
 \- \[POST\] : [{{url}}?route=api2/address/getZones]({{url}}?route=api2/address/getZones)
 
## Request Parameters
  
name       | type | example value
-----------|------|--------------
country_id | text | 94           

 
### Request example:
  
	{{url}}?route=api2/address/getZones  
	country_id=94  

 
