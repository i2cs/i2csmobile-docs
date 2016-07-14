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
|__ menu
|__ offers
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

`sample.module.js`
-----

This contains nothing more than just the initiation of the angular module. Since most of our modules needs routing, we will have to import `ui.router` dependency.

```javascript
'use strict';

angular.module('sample.module', ['ui.router']);
```

`sample.config.js` 
-----

This file contains the configurations of the module we are creating. Configurations includes the routing and any other needed `config`. Note that this module contains two views, one for the tabs theme and the other is for the side menu theme.

```javascript
'use strict';

angular.module('sample.module')
    .config(function config($stateProvider) {
        $stateProvider
            .state('app.sample', {
                url: '/sample',
                abstract: true,
                views: {
                    'tab-sample': {
                        templateUrl: 'app/sample/templates/layout.html'
                    },
                    'menu': {
                        templateUrl: 'app/sample/templates/layout.html'
                    }
                }
            })
            .state('app.sample.list', {
                url: '/list',
                views: {
                    'sampleContent': {
                        templateUrl: 'app/sample/templates/item_list.html',
                        controller: 'SampleCtrl'
                    }
                }
            })
	});
```

This contains an abstract view for the module. In this architecture, each module carries their own layout page. The layout page contains in an `abstract` state, so it can't be rendered alone. The state `app.sample.list` is derived through the abstract state and it contains the real `html` markup of the module state. We recommend to use this file if you need more configurations to be injected to the module.

`sample.service.js` 
-----

For the sample module, we need a service layer to communicate with the back-end API. We use angular `promise` chains to pass data from API to the UI. 

```javascript
(function () {
    'use strict';
    angular
        .module('sample.module')
        .service('SampleService', function ($http, $q, dataService) {
			this.GetSomething = function () {
                return dataService.apiSecuredPost('/ctrl/sample');
            }
			
			this.GetAdvanced = function () {
                return dataService.apiSecuredPost('/ctrl/sample').then(function (data) {
                    data.new = data.old * 2;
					return data;
                }, function(data){
					return data;
				});
            }
		});
})();
```

Note : `this.GetAdvanced` service method gets the $http response into an object with name `data`. If data coming from the API needs to be manipulated from app side before rendering in UI, we  recommend you to do those changes within the `service` layer. `this.GetAdvanced` method is an example for that.

`sample.controllers.js` 
-----

This file contains all the necessary `controllers` of the module.

```javascript
'use strict';

angular
    .module('cart.module')
    .controller('SampleCtrl', function ($scope, SampleService) {
    	SampleService.GetSomething().then(function(data){
    		$scope.list = data;
    	})
    });
```

We pass the angular `promise` up to the controller level and consume data only at the point of executing the function from the controller. This practice made most of the async calls very easy to manage and project dynamically to the UI.
Note : Keep `$scope` variable in between controller and the UI template as a practice. Since we are not passing `$scope` to service layer, it's very easy to get rid of `$scope` and start using `this`

###1.1. COMMON

Common folder is the place for `services` and `directives` which are common for the entire application.

* app.service.js
This has service calls related to customer registration, login and logout

* analytics.service.js
Google analytics service. Captures page views.

* data.service.js
Calls the http API endpoints and resolves the response. Contains authentication call, which should be called before using apiSecuredPost method. otherwise it will reject the request with error status of 0 on API calls which needs the authentication

* notification.service.js
Initializes the notification service. This will register the device for push notifications. Subscribes the device for a scheduled notification with random greeting message notified in 86400000 seconds from now

* update.service.js
Initializes the update service. This will check for available app updates on start and once in a 5 minutes. If an update is available, checks for network connection. If the device is connected to a WIFI connection, download the update and install, otherwise popup informing the update will be downloaded when device is connected to a WIFI

###1.1. CART

Cart module consists of the functionality of the Cart tab of the mobile app. It communicates with the API to add items to cart, checkout and place new orders. 

> Cart home view
* Load current shopping cart
* Remove items from shopping cart

> Cart checkout view
* Fill user data
* Select shipping method
* Select payment method
* Place the order
