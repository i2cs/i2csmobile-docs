#Installation guide of i2CSMobile OpenCart 2.1 API module

##Configurations

This section describes the configurations you have to do in order to make the mobile app work with the OpenCart store. We try to keep your existing store as it is, and use the same data for the mobile app. That’s why we need configurations. In simple terms, we tell OpenCart to provide data to the new mobile app by setting configurations.

###Getting Started

We try to keep mobile app related processes and default web app processes away as much as possible. With this, we can achieve better control on how your customers see necessary content. For example, what if you want to make some items available only for mobile app but not to the web, or the other way around? What if you want to give special discounted prices for mobile app orders, and a different discount if the user is registered in mobile app? We have answers for all these questions, good thing is we can do that with minimum changes to your existing shopping cart.

To go ahead, we assume that you have successfully installed the `i2CSMobile` module for OpenCart 2.x and made at least one successful API call. Furthermore you need an admin account having proper privileges to do necessary configuration changes on `i2CSMobile` module.

###Creating a new Customer Group [Optional Step]

Please note that this section is optional. You can create a new Customer Group for mobile app users to make maximum use of the `i2CSMobile` app.

1.	Go to `OpenCart Admin panel > Customers > Customer Groups`

2.	Click on `Add New` button

3.	Choose a name for your group. We used Mobile app as the name for this guide

###Creating a new Store [Optional Step]

Please note that this section is optional. You can go ahead with default store or any other store you have created within your OpenCart and let the mobile use data from them. But if you create a new store dedicated to the mobile app, you can do beautiful things like creating special offers on mobile, have different product catalogs on mobile and web and more.

1.	Go to `OpenCart Admin panel > Settings`

2.	In the Store page, click on  Add New button

3.	Enter details of the new store and save. In the Store URL field, include the full URL to your store. Make sure to add '/' at the end. Example: http://www.yourdomain.com/path/ .Don’t use directories to create a new store. You should always point another domain or sub domain to your hosting. See http://docs.opencart.com/system/setting/store/ to learn more about creating a new store in OpenCart. If you are using localhost, add 127.0.0.1 instead of localhost and get the new url to add to the Store URL. In this guide, we used http://localhost/opencart-2.1.0.1/upload/ as the default store URL. So we have to add http://127.0.0.1/opencart-2.1.0.1/upload/ in the Store URL of the new store we are creating. 

4.	Go to Option tab, go to Customer Group dropdown and select Mobile app customer group as the default group to use for this store. Customer Groups and select all customer groups whom should have the access to the mobile app. Make sure you select the Mobile app customer group along with any other customer group.

5.	Save to add the new store. You will be shown a success message `Success: You have modified Stores!`

###Creating a new API User [Optional Step]

Please note that this section is optional. You can use the existing API user as the API user for our mobile app. But still, it’s better to have a totally different user to provide mobile API data.

1.	Go to `OpenCart Admin panel > Settings > API` to open APIs view

2.	In the APIs page, click on  Add New button

3.	Choose a name for your API. We used mobile as the name for this guide

4.	Click on Generate button to create a new API Key

5.	Set the status to Enabled and then click on save icon to create the API user

6.	Now you have successfully crated a new API 

###I2CSMobile Settings

Now you are ready to setup the configurations and make them all wire up to get the mobile app up and running. We had couple of non-required steps previously to take maximum advantage from the API. But even if you have skipped them, you can continue from this step.

1.	Go to `OpenCart Admin panel > Extensions > Modules > i2CSMobile`

####Settings Tab

This is the tab where you can make all the configuration changes to the `i2CSMobile` system. Changes you make here are directly reflected to the mobile app, thus it’s recommended to test the live app each time you make any configuration change.

1.	You have to set the Mobile API Key to let `i2CSMobile` module access the inner data of your OpenCart store. Go to Settings > Users > API and click on the API you would like to associate with. In this guide, we used the newly created mobile api. Select the entire API Key and Copy `(CTRL + C or right click and select copy)`

2.	Come back to `i2CSMobile` module and paste the key inside Mobile API Key field

3.	Select the customer group for mobile app on Mobile User Group field. In our guide, we use Mobile app group. Customers are added to Mobile User Group when they are registered through mobile app. Furthermore, mobile only special prices are also calculated and presented based on this user group. You can see this special price on mobile in the purchase button and on item view page. This represents the price you offer to your mobile app users if the create an account in mobile app.

4.	You can set the main banner of the home screen of the app from Main Banner field. All the available banners will be loaded to the dropdown and you may select one among them. Main banner is the one you can see in the Landing page of the app.

5.	You can configure a secondary banner in the API. In most cases you might need to show special offers in the main screen. Offer Banner field is to define a banner which appears in the home screen.

6.	There is an Offers Tab in the mobile app to show new offers and special priced items. You can set an array of images to be listed there by configuring Offers Tab Banner field.

7.	I2CSMobile app supports featured items slideshow out-of-the box. You can see this in the shop main screen under the title Featured Products. Configuration for the featured items is available in the i2CSMobile admin panel with Featured Items Module dropdown. If you don’t see anything in the dropdown, please add Featured module and create a new featured item module. You can set items to be listed in the Featured Products section within the featured items module. See http://docs.opencart.com/extension/module/ to learn about core modules. 

8.	There is a set of categories in the Shop main screen of the mobile app to provide quick navigation for the customers. You can configure which categories you’d like to show in the app using Categories field. If none of the categories are selected, the system will show all the parent categories.

#####Common Issues

1.  I don’t see products when run the app

    Please check if the API tests are passed. If all of them are working, you have to check all the configurations are correct in mobile app. Check for the Base API url variable and confirm whether it’s pointed to the correct API url.

2.  I didn’t create a new store. Would it be a problem?

    No. It will work fine even if you have only one store within the OpenCart. It’s totally an optional step to create a new store 


####[Section 3 : Testing the API](03 Testing the API.md) 
