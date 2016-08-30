#Installation guide of i2CSMobile OpenCart 2.1 API module

##Pre-Requisites

###WooCommerce

In this guide we assume that you already have `WooCommerce` plgin installed in your `WordPress` site. If you have not done so, please navigate to the following link and install `WooCommerce`. [https://wordpress.org/plugins/woocommerce/](https://wordpress.org/plugins/woocommerce/)

###MetaSlider

We use slideshow banners in the app. In order to provide the functionality we use another plugin called `MetaSlider`. If your app needs the banner functionality (main screen banner, offer banner, or any other image content you would like to control from the `WooCommerce` backend) please install the `MetaSlider` plugin. 

> *Note* If you wish to use another existing banner plugin, you will have to edit the `get_banner` method of `class-wc-rest-i2cs-store-controller.php` file.

[https://wordpress.org/plugins/ml-slider/](https://wordpress.org/plugins/ml-slider/) 

##Installation

1. Upload the plugin files to the `/wp-content/plugins/i2csmobile-for-woo directory`, or install the plugin through the WordPress plugins screen directly. You can search for "i2CSMobile App" in plugins section of `WordPress` admin panel

2. Activate the plugin through the 'Plugins' screen in `WordPress`

3. Plugin API is accessible via `http://store_address/wp-json/i2cs/v1/`