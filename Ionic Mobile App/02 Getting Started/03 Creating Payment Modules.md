##Creating Payment Modules

With this tutorial we will create a new payment module in i2CSMobile app
----

###Introduction to Payment Modules

We have a pluggable payment module structure as defined in the following figure. `payment_modules.config.js` and `payment_modules.module.js` files are system files. 'payment_modules.module.js' file contains information about which payment modules are registered to the app.

```
app
|__ payment_modules
	|
	|__ i2cs_alipay
	|	|
	|	|__ templates
	|	|	|__ layout.html
	|	|	|__ home.html
	|	|
	|	|__ i2cs_alipay.config.js
	|	|__ i2cs_alipay.controller.js
	|	|__ i2cs_alipay.module.js
	|	|__ i2cs_alipay.service.js
	|
	|__ templates
	|	|__ layout.html
	|
	|__ payment_modules.config.js
	|__ payment_modules.module.js
```	

`i2cs_alipay` is the name of the payment module. We use the naming convention as `PAYMENT_MODULE_NAME.module.js` .etc to define the `js` files of the module. We need to have the same payment module name as in the `OpenCart` payment module code. The mobile app payment module will automatically loaded as the last step of checkout flow.

###Payment Module in Checkout Flow 

The checkout flow in the i2CSMobile app is same as the checkout flow of the OpenCart. App collects user data, address, payment method and shipping method and when user taps on `confirm` button the order will be placed in the system. Then the app will search for registered payment modules having same name as code of the selected payment option of OpenCart and invoke the home route if it's available. If the payment module is not found, it will show the success page.

Ex.
1. User fills personal info
2. Selects Shipping method
3. Selects Payment method with payment code `i2cs_alipay`
4. Confirms the order. This will place the order with Pending status.
5. App will invoke the home page of `i2cs_alipay` module
6. Proceed with steps depending on the implementation of the payment module. Service methods of the payment module are responsible for updating the API with correct statuses. You need to register a payment handler in the OpenCart back-end to communicate with the payment module of the mobile app.
 

###Module Components

Payment modules follow the same module structure as in any other general module for i2CSMobile app. Read [02 Creating a Module](02 Creating a Module.md) for more information.

###Installing the Module

This step is similar to the steps of installing any other module, but with an exception. Again we need to edit two files.

1. www/index.html
2. www/app/payment_modules/payment_modules.module.js

In the `index.html` file we need to import 4 `js` files. We can do that simply by adding following lines in the `<head>` tag,
```
	<script src="app/payment_modules/i2cs_alipay/i2cs_alipay.module.js"></script>
	<script src="app/payment_modules/i2cs_alipay/i2cs_alipay.config.js"></script>
	<script src="app/payment_modules/i2cs_alipay/i2cs_alipay.controller.js"></script>
	<script src="app/payment_modules/i2cs_alipay/i2cs_alipay.service.js"></script>
```

In the `payment_modules.module.js` module file we need to inject the new module as a dependency. 

```
	angular.module('payments.module', ['ui.router', 'i2cs_alipay.module']);
```

### Testing the Module

To invoke the module, you have to enable the payment module from the OpenCart system first. And then confirm and place an order by selecting the payment module. If everything is fine, you should be seeing the home page of the payment module.