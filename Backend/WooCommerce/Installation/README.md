#Installation guide of i2CSMobile WooCommerce API plugin

##Pre-Requisites

###WooCommerce

In this guide we assume that you already have `WooCommerce` plugin installed in your `WordPress` site. If you have not done so, please navigate to the following link and install `WooCommerce`. [https://wordpress.org/plugins/woocommerce/](https://wordpress.org/plugins/woocommerce/)

###MetaSlider

We use slideshow banners in the app. In order to provide the functionality we use another plugin called `MetaSlider`. If your app needs the banner functionality (main screen banner, offer banner, or any other image content you would like to control from the `WooCommerce` backend) please install the `MetaSlider` plugin. 

> *Note* If you wish to use another existing banner plugin, you will have to edit the `get_banner` method of `class-wc-rest-i2cs-store-controller.php` file.

[https://wordpress.org/plugins/ml-slider/](https://wordpress.org/plugins/ml-slider/) 

##Installation

1. Upload the plugin files to the `/wp-content/plugins/i2csmobile-for-woo directory`, or install the plugin through the WordPress plugins screen directly. You can search for "i2CSMobile App" in plugins section of `WordPress` admin panel

2. Activate the plugin through the 'Plugins' screen in `WordPress`

3. Plugin API is accessible via `http://store_address/wp-json/i2cs/v1/`

#Testing the API

This section demonstrates to do a quick test to see if the API is working properly. Working API is mandatory for all the functionality of the mobile app. We are pulling data to present in your app from your store via the API. In this section we use a 3rd party API call maker to see if it returns a valid response.

In this tutorial, we use a free API tester named Postman. Please download it here,

https://www.getpostman.com

See https://www.getpostman.com/docs/introduction to learn how to install and setup Postman. 

###Import the Postman test project

1.	Once you successfully installed the Postman app, you can import the `i2CSMobile_API_FullTest.json`

2.	Import environments (`i2CSMobile_API_Environment.json`), and change the url value to your OpenCart instance. See https://www.getpostman.com/docs/environments to learn how to set environment variables.

3.	Run the test collection to see what API methods needs to be fixed

4.	Ideally you should get 100% pass rate. Otherwise there can be faild test cases depending on the data. For example, one test case might fail if your store doesn’t support Cash on delivery payment. But if you are getting a `200 OK` status code for all the tests, you are too good to go ahead with `i2CSMobile`.

#####Common issues

1.	I'm getting "No route was found matching the URL and request method"

   Please check if your plugin is correctly installed and is activated. And also double check the `url` is correct in the POSTMAN environment.
