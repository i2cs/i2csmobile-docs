##Deploy App to Live Devices

This demonstrates how to push your updates to devices which already installed the app
----

###Introduction
We use `ionic deploy` service to push app updates to devices. The app core has pre defined methods to periodically check it's servers for new app updates. If such update is found, the end user will see a popup in their mobile app askig if it is ok to download the update and install it automatically. If the user is connected to a wifi network, the app will automatically update itself. When you need to send such update to devices follow the below instructions.

###Deploy Service

####Channels

Deploy channels give you the ability to deploy different snapshots of your app to different devices.

There are three channels available for every app by default: production, staging, and dev. You can create more channels if needed. By default, snapshots will pull from the production channel.

 
####Snapshots

Snapshots are created by uploading a bundled version of your app code using the Ionic CLI. These snapshots can then be deployed to different channels, and ultimately applied to a user’s device.

In the following examples, fill in the following:

> NOTE	A short description of this snapshot

> CHANNEL_TAG	production, staging, dev, or a tag of a custom channel


Whenever you’re ready to create a snapshot of your application, run the upload command:

```
$ ionic upload --note "NOTE"
```

This will bundle your local app code and upload it as a unique snapshot.

 
####Deploying to Channels

When you upload with the `--deploy` flag, your snapshot is immediately deployed to a channel. You can alternatively use the Dashboard to deploy snapshots that have been uploaded.

```
$ ionic upload --note "NOTE" --deploy CHANNEL_TAG
```

####Binary Versioning
You can determine if a snapshot is applicable for a device by using binary versioning. Binary versioning requires that you use a semantic version for your build version.

> The semantic versioning format is a common strategy for flexible and predictable versioning. The format comprises three parts, major.minor.patch. When we compare versions, we adhere to version precedence. Example: 1.0.0 < 2.0.0 < 2.1.0 < 2.1.1.

To set the version of the snapshot, you have to log in to the ionic admin panel from your browser, select the app and navigate to the `deploy` section.

As you develop your app, you may need to add or update Cordova plugins, update the platform sdk support, or make other changes that would require a binary update. If you deploy a snapshot of your app expecting such changes, your app may crash. Binary versioning lets you halt live deployments on devices that would otherwise break the app.
