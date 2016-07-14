##Getting Started
###A small guide which will give a brief overview to i2CSMobile app

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

####1. APP
The app folder contains the actual modules of the app. Each module has its own folder and consist of several html and js files. We tried to keep modules as much independent as possible, thus removing or adding a new module affects minimum code change. The product comes with few default modules,

```
app
|__ cart
|__ common
|__ info
|__ menu
|__ offers
|__ payment_modules
|__ shop
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

> `sample.module.js` 

This contains nothing more than just the initiation of the angular module. Since most of our modules needs routing, we will have to import `ui.router` dependency.

```javascript
'use strict';

angular.module('sample.module', ['ui.router']);
```

> `sample.config.js` 

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

This contains an abstract view for the module. In this architecture, all modules carries their own layout page. The layout page contains in an `abstract` state, so it can't be rendered alone. The state `app.sample.list` is derived through the abstract state and it contains the real html markup of the module state. We recommend to use this file if you need more configurations to be injected to the module.

> `sample.service.js` 

For the sample module, we need a service layer to communicate with the backend API. We use angular `promise` chains to pass data from API to the UI. 

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

> `sample.controllers.js` 

This file contains all the neccessary `controllers` of the module.

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

We pass the angular `promis` up to the controller level and consume data only at the point of executing the function from the controlelr. This practice made most of the async calls very easy to manage and project dynamically to the UI.
Note : Since we are not passing `$scope` to service layer, it's very easy to get rid of `$scope` and start using `this`


####1.1. CART

Cart module consists of the functionality of the Cart tab of the mobile app. It communicates with the API to add items to cart, checkout and place new orders.

