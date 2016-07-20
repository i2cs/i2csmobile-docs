##Getting Started

A small guide which will give a brief overview to i2CSMobile app
----

We believe that you have successfully started an instance of i2CSMobile app by following installation guide. The project structure is as follows,

```
www
|__ app
|__ css
|__ img
|__ languages
|__ lib
|__ templates
|__ index.html
    
```

###1. APP
The app folder contains the actual modules of the app. Each module has its own folder and consist of several `html` and `js` files. We tried to keep modules as much independent as possible, thus removing or adding a new module affects minimum code change. The product comes with few default modules,

```
app
|__ common
|__ shop
|__ cart
|__ info
|__ offers
|__ menu
|__ payment_modules
|__ app.js
|__ controllers.js
|__ variables.js
    
```

Normally each module which interacts directly with end user has following structure. We have 4 different `js` files to initialize the angular module, which we believe very easy to maintain a clean source code.

```
app
|__ sample
    |__ templates
		|__ item_list.html
		|__ layout.html
	|__ sample.module.js
	|__ sample.config.js
	|__ sample.service.js
	|__ sample.controllers.js
```	

`sample` is the name of the module. We use the naming convention as `MODULE_NAME.module.js` .etc to define the `js` files of the module. 

Go to [02 Creating a Module](02 Creating a Module.md) for a detailed explanation about modules.

###1.1. COMMON

Common folder is the place for `services` and `widgets` which are common for the entire application. There are few core `services` and `widgets` provided by default.

* `app.service.js`
This has service calls related to customer registration, login and logout

* `analytics.service.js`
Google analytics service. Captures page views.

* `data.service.js`
Calls the http API endpoints and resolves the response. Contains authentication call, `apiLogin` which should be called before using apiSecuredPost method. otherwise it will reject the request with error status of 0 on API calls which needs the authentication. The `dataService` is responsible for providing a `promise` object containing the requested data. On a success response it returns the data from the server, and on an error the promise rejects with the HTTP server response. i.e, HTTP server response object contains,

```
config:Object
data:Object
headers:function(c)
status:406
statusText:"Not Acceptable"
```

* `notification.service.js`
Initializes the notification service. This will register the device for push notifications. Subscribes the device for a scheduled notification with random greeting message notified in 86400000 seconds from now

* `update.service.js`
Initializes the update service. This will check for available app updates on start and once in a 5 minutes. If an update is available, checks for network connection. If the device is connected to a WIFI connection, download the update and install, otherwise popup informing the update will be downloaded when device is connected to a WIFI

###1.2. SHOP

Shop is the default landing module of the app. It has all the functionality related to the product catalog of the shopping cart application.

> Shop home view

* Promotional banners
* Categories view
* Featured items
* Latest items
* Infinite scroll

> Product view

* Image slide show
* Specifications
* Product options (checkbox, radio, select, text, textarea, date, datetime, .etc)
* Share with friends

> Product search view

* Search for keywords
* Infinite scroll

> Product category view

* Latest products of selected category
* Infinite scroll

###1.3. CART

Cart module consists of the functionality of the Cart tab of the mobile app. It communicates with the API to add items to cart, checkout and place new orders. 

> Cart home view

* Load current shopping cart
* Remove items from shopping cart

> Cart checkout view

* Fill user data
* Select shipping method
* Select payment method
* Place the order

###1.4. INFO

Info section contains everything related to the customer self care. 

> Info home view

* Login/Logout
* About us
* Contact us
* UI Language switch

> Order history

* Show order list
* Select order and see invoice

###1.5. OFFERS

Offers tab shows image feed from a banner and special priced items.

> Offers home view

* Offer banner feed
* Special priced products

###1.6. MENU

This contains main layout entry points of the app. Out-of-the-box product comes with two different templates for menu styles, tab navigation and side menu navigation.

> Tabs

Default is the tabs UI. `tabs.html` contains the icons which should be added to each tab in the UI.

> Side menu

Enables a left side menu to navigate.

###1.7. PAYMENT MODULES

Payment modules are to communicate with customizable payment gateways. A payment module exactly follows the same pattern as any other module. When placing an order with a payment method with additional steps involved, for example a credit card method, the app will search in `payment_modules` directory for a module with that payment code. The system will route to the `home` state of the payment module, so that user can enter additional data and proceed with the checkout.

###1.8. APP.JS

`app.js` is the main entry point of the application. Whenever you create or delete a module, you will have to update the angular main module initialization and register or unregister the module.

```javascript
var starter = angular.module('starter', ['ionic', 'sample.module')
```

Apart from that, the `app.js` file contains configurations. This file has the main route entry of the app. You can switch the main layout (tabs or side menu) by toggling following lines. The app is bootstrapped from an abstract state called `app`. Then it branches into two abstract states, `app.menu` and `app.main`. All the states which inherit `app.menu` state will have either tabs or side menu, whereas `app.main` will have a clean layout without tabs or side menus.  

```javascript
state('menu', {
	url: '/app/menu',
	abstract: true,
	templateUrl: 'app/menu/templates/tabs.html',
	//templateUrl: 'app/menu/templates/side.html',
	controller: 'AppCtrl'
})
```


###1.9. CONTROLLERS.JS

This file contains two mandatory controllers, `WelcomeCtrl` and `AppCtrl`. 

###2.0. VARIABLES.JS

This is the place you have to edit in order to change some of the configurable values of the app. Most important configuration is the `BASE_API_URL`. Set it to your OpenCart instance once you are successfully installed the OpenCart module for i2CSMobile app.

```javascript
.constant('BASE_API_URL', 'http://shop.i2csmobile.com/index.php?route=api2')
```
