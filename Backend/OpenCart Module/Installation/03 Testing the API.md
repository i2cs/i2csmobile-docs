#Installation guide of i2CSMobile OpenCart 2.1 API module

##Testing the API

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

1.	Im getting HTTP Error 503 Service unavailable error

   Please check if you have enabled maintenance mode in the OpenCart admin panel. You can check that from,
   Log into your OpenCart Dashboard.
      - Go to System > Settings.
      - Select your store from the list and click “Edit”
      - Go to the “Server” tab.
      - Find the Maintenance Mode section (usually third from the top) and change it to “No”

2.	Get Featured Products test is failed (12.1 api2/featured : Get Featured Products)

   Please check if you have set the Featured Items Module value in the `i2CSMobile` admin panel. You might need to save the module for the first time even if you see a value is selected in the dropdown. If you don’t see any value there, go to OpenCart modules list and add a new module by  clicking on Edit button of Featured item. Save the newly created Featured module and set some products as featured items. See http://docs.opencart.com/extension/module/ to learn more about core modules of OpenCart.

3.	Latest products/ Special products tests are failing

   Failing these test cases might be caused by not having products in your OpenCart store or not having enough access to navigate products. This can happen when you create a new store and not adding each item to the new store. Go to `OpenCart Admin panel > Products > Edit > Links > Stores` and see if your newly created store is checked. See http://docs.opencart.com/catalog/product/link/ to learn how to add stores to your products. If you don’t have any item with special prices, you wont be able to pass the Special Products test case. See http://docs.opencart.com/catalog/product/special/  to learn how to add special prices.
