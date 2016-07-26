##Quick Start with Ionic Starter
###A guide to quickly set up and running the i2CSMobile app with ionic starter package

This guide will explain you how to setup the app quickly using an ionic starter template. In a starter template we provide content of `www` folder, and all the additional dependencies should be installed by running few commands. Extract the content of the downloaded zip file. The package contains two folders for `ionic` app and `opencart` module. Open your CMD or terminal and navigate to the place where you would like your project to be initialized (Ex. `C:\projects\`).
```
I2CSMOBILE_PACKAGE
|__ ionic
|   |__ starter
|   |__ full-package
|__ opencart
    |__ ***
```

This product is based on ionic platform. You have to install ionic CLI if you haven't done it yet. Please refer to [Installing the CLI globally](http://ionicframework.com/docs/cli/install.html)

####1. CREATE AN APP
```
ionic start myapp "C:\I2CSMOBILE_PACKAGE\ionic\starter\www"
cd myapp
```

####2. INSTALL DEPENDENCIES

Note: You need to provide `GCM_PROJECT_NUMBER` When installing push notification plugin. Please follow [this tutorial](http://docs.ionic.io/docs/push-overview) to get a `GCM_PROJECT_NUMBER`. The latest plugin update requires that a SENDER_ID variable be set for Android. That is actually your GCM Project Number. If you're not using Android, you'll just need to pass a random string (you could even use the above command as-is).

```
ionic plugin add cordova-plugin-device@1.1.1
ionic plugin add cordova-plugin-statusbar@2.1.0
ionic plugin add ionic-plugin-keyboard@1.0.8
ionic plugin add cordova-plugin-network-information@1.2.1
ionic plugin add https://github.com/katzer/cordova-plugin-local-notifications.git
ionic plugin add cordova-plugin-app-event@1.2.0
ionic plugin add cordova-plugin-splashscreen@3.2.2
ionic plugin add cordova-plugin-device-orientation@1.0.3
ionic plugin add cordova-plugin-whitelist@1.2.2
ionic plugin add phonegap-plugin-push --variable SENDER_ID=GCM_PROJECT_NUMBER
ionic plugin add https://github.com/vliesaputra/DeviceInformationPlugin
ionic plugin add cordova-plugin-google-analytics@0.8.1
ionic plugin add cordova-plugin-x-socialsharing@5.0.12
ionic plugin add ionic-plugin-deploy@0.5.4
ionic plugin add cordova-plugin-app-version@0.1.8
```

####3. INIT THE IONIC PROJECT
```
ionic io init
```
####4. ADD PLATFORMS
```
ionic platform add android
```
####5. BUILD IT FOR A PLATFORM OR SEE IT IN BROWSER 

You can build the apk with following command. Make sure you have installed Android SDK on your computer before running this.
```
ionic build android
```

Or you can test the app in your web browser by entering following command. Note that you can use `ionic serve` to start a local development server for app dev and testing. Most of the mobile app specific features (ex. Push notifications .etc) are disabled when you run `ionic serve` command.
```
ionic serve
```

##Quick Start with Full Source
###A guide to quickly set up and running the i2CSMobile app with ionic full source package

Full source comes with all the dependencies. You need to extract the content of the `full-source.zip` and navigate to the path with CMD.

####1. EXTRACT CONTENT OF `full-source.zip` TO A NEW FOLDER

####2. NAVIGATE TO THE PATH (where `www` folder is located)
```
cd myapp
```
####3. INSTALL NPM PACKAGES
```
npm install
```

####4. INIT THE IONIC PROJECT
```
ionic io init
```
####5. ADD PLATFORMS
```
ionic platform add android
```
####6. BUILD IT FOR A PLATFORM OR SEE IT IN BROWSER 

You can build the apk with following command. Make sure you have installed Android SDK on your computer before running this.
```
ionic build android
```

Or you can test the app in your web browser by entering following command. Note that you can use `ionic serve` to start a local development server for app dev and testing. Most of the mobile app specific features (ex. Push notifications .etc) are disabled when you run `ionic serve` command.
```
ionic serve
```
