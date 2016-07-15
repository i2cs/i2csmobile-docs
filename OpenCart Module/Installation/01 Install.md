#Installation guide of i2CSMobile OpenCart 2.1 API module

##Pre-Requisites

###OpenCart

In this guide we assume that you already have OpenCart 2.x version installed, and you have admin privileges to install OpenCart extensions via Extension Installer. If you face problems while uploading the i2CSMobile extension, please double check for folder permissions of your OpenCart installation.

If you don’t have OpenCart installed, please download and install it first. We used OpenCart 2.1 as the sample OpenCart system for this guide and all screenshots are based on OpenCart 2.1.0.
[http://www.opencart.com/?route=download/download](http://www.opencart.com/?route=download/download)

Please follow installation guide of OpenCart to install it
[http://docs.opencart.com/installation](http://docs.opencart.com/installation) 


###OCMOD

We use OCMOD to do necessary changes of your system. OCMOD is a system that allows store owners to be able to modify their store by uploading a compressed file that contains XML, SQL and PHP files. It comes with installation of OpenCart 2.x versions and you don’t need to install it separately.

I2CSMobile extension can modify your OpenCart store in a way that it works without changing any of the core files. This means that if i2CSMobile extension is removed none of the original OpenCart files need to be restored or fixed.

For more information about OCMOD please follow this link

[https://github.com/opencart/opencart/wiki/Modification-System](https://github.com/opencart/opencart/wiki/Modification-System)


##Installation

1. Navigate to the admin panel of your OpenCart installation by providing admin username and password. You have to log in to OpenCart with a user having privileges to add an extension. Account you have created while installing the OpenCart is a super user and it’s recommended to log in with that user account.

2. Go to `Extensions` menu and click on `Extension Installer`

3.	Click on `Upload` button

4.	Browse for i2CSMobile ocmod extension file, and select it. Ex, `i2cs_mobile_OCv2.1.x.ocmod.zip`
  * On a success installation you will see a success message `Success: You have installed your extension!`
  * If you face error saying FTP needs to be enabled in the settings please install following fix to enable non FTP enabled uploads. Once you install the modification, please go through `step 5` and `step 6` to apply the modification, and come back to `step 4`. http://www.opencart.com/index.php?route=extension/extension/info&extension_id=18892 

5.	Go to Extensions menu and click on Modifications item

6.	Click on the Refresh  button. This will apply your modifications to the system

7.	Go to `Extensions > Modules`. Click Edit button of `i2CSMobile` module in the module list 

8.	You have successfully installed the module!


####[Section 2 : Configurations](02 Configurations.md) 
