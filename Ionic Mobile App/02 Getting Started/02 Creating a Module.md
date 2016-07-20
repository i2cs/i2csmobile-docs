##Creating a Module

This guide will take you through how to create a new module in i2CSMobile app
----

###Anatomy of a Module

Normally each module which interacts directly with end user has following structure. We have 4 different `js` files to initialize the angular module, which we believe very easy to maintain a clean source code. From these `js` files, `sample.module.js`, `sample.config.js` and `sample.controllers.js` are mandatory. 

`templates` folder contains all the UI template `html` files of the module. As a practice we keep a layout template on each module, and it invokes the appropriate template of a given UI state. In our example, we have one template named `item_list.html`.

```
app
|__ sample
    |
	|__ templates
	|	|__ item_list.html
	|	|__ layout.html
	|
	|__ sample.module.js
	|__ sample.config.js
	|__ sample.service.js
	|__ sample.controllers.js
```	

`sample` is the name of the module. We use the naming convention as `MODULE_NAME.module.js` .etc to define the `js` files of the module. 

###Module Components

`sample.module.js`
-----

This contains nothing more than just the initiation of the angular module. Since most of our modules needs routing, we will have to import `ui.router` dependency. If there are any other dependency specific to the module, this is the place to add them.

```javascript
'use strict';

angular.module('sample.module', ['ui.router']);
```

`sample.config.js` 
-----

This file contains the configurations of the module we are creating. Configurations includes the routing and any other needed `config`. Note that this module contains two views, one for the tabs theme and the other is for the side menu theme. For this example we use the same `layout.html` for both views.

```javascript
'use strict';

angular.module('sample.module')
    .config(function config($stateProvider) {
        $stateProvider
            .state('app.menu.sample', {
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
            .state('app.menu.sample.list', {
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

This contains an abstract view for the module. In this architecture, each module carries their own layout page. The layout page contains in an `abstract` state, so it can't be rendered alone. The state `app.menu.sample.list` is derived through the abstract state and it contains the real `html` markup of the module state. We recommend to use `sample.config.js` if you need more configurations to be injected to the module. 

The layout page contains the following markup to invoke the view.

```
<ion-nav-view name="sampleContent"></ion-nav-view>
```

`sample.service.js` 
-----

For the sample module, we need a service layer to communicate with the back-end API. We use angular `promise` chains to pass data from API to the UI. Since most of the services interact with the API, we have defined a core serviec called `dataService`. The `dataService` is responsible for providing a `promise` object containing the requested data. On a success response it returns the data from the server, and on an error the promise rejects with the HTTP server response. i.e, HTTP server response object contains,

```
config:Object
data:Object
headers:function(c)
status:406
statusText:"Not Acceptable"
```

```javascript
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

```

Note : `this.GetAdvanced` service method gets the $http response into an object with name `data`. If data coming from the API needs to be manipulated from app side before rendering in UI, we  recommend you to do those changes within the `service` layer. `this.GetAdvanced` method is an example for that.

`sample.controllers.js` 
-----

This file contains all the necessary `controllers` of the module.

```javascript
'use strict';

angular
    .module('sample.module')
    .controller('SampleCtrl', function ($scope, SampleService) {
    	SampleService.GetSomething().then(function(data){
    		$scope.list = data;
    	})
    });
```

We pass the angular `promise` up to the controller level and consume data only at the point of executing the function from the controller. This practice made most of the async calls very easy to manage and project dynamically to the UI.
Note : Keep `$scope` variable in between controller and the UI template as a practice. Since we are not passing `$scope` to service layer, it's very easy to get rid of `$scope` variable and start using `this`

###Installing the Module

In order to install a new module, we need to edit two files.

1. www/index.html
2. www/app/app.js

In the `index.html` file we need to import 4 `js` files. We can do that simply by adding following lines in the `<head>` tag,
```
	<script src="app/sample/sample.module.js"></script>
	<script src="app/sample/sample.config.js"></script>
	<script src="app/sample/sample.controller.js"></script>
	<script src="app/sample/sample.service.js"></script>
```

In the `app.js` main module file we need to inject the new module as a dependency. 

```
	var starter = angular.module('starter', ['ionic', 'ngCordova', 'ngLocalize', 'ionic.service.core', 'ionic.service.analytics', 'starter.controllers', 'shop.module', 'offers.module', 'cart.module', 'info.module', 'payments.module', 'auth.module', 'sample.module'])
```

### Testing the Module

To invoke the module, you can add a link in any other working module html with a `ui-sref` attribute to the module ui state. Note that to see a proper page, you might need to add some content into the `item_list.html` page. 

```
<a ui-sref="app.menu.sample.list">Sample</a>
```