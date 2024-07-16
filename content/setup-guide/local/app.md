+++
title = "App"
weight = 4
+++

## Local App Setup

### Web Setup

The easiest way to test the app is by using the web build. To run the app without instalations Docker can be used once again.

```
docker-compose up
```

This will build the app and start a webserver listening on port 5000 at http://loalhost:5000. The web build will automatically use the local backend unless specified otherwise. If the Flutter SDK is installed locally the App can also be started with the following commands:

```
flutter config --enable-web
flutter pub get
flutter run -d chrome --web-port 5000
```

Port 5000 is important due to CORS and Origin Controls defined in the backend.

By pressing r in the console window while the app is running new changes can be applied without needing to rebuild the app.

### Mobile Setup

If the Flutter SDK is installed locally on your system the app can also be run directly in an emulator.

The app can be tested either on device using the emulator or on your phone. If you are planning on testing the app on a macOS device in flutter it is recommended to instead test the app directly on your phone. This is due to the fact that the iOS emulator on macOS does not support camera mocking.

To test the mobile app in an emulator with a local backend modify the URLs in file */lib/flavors.dart*. Replace both Flavor.DEV and Flavor.PROD with http://localhost:9997/v1. ⚠️ **Do not push this change to the remote repository. 🔴 Doing so so may break production** as the app is automatically built and deployed from the GitHub repository on specific conditions and will cease to work in the cloud deployment with these changes applied ⚠️.

After this setup run the flutter app with the following commands:

```
flutter pub get
flutter run --flavor dev -t lib/main-dev.dart --release
```

With the modified URLs in */lib/flavors.dart* the app will use the local API.

#### Using the Local Backend with a Physical Phone

When using an actual phone for testing, make sure your phone and development device are both connected to the same network. When changing the URLs in */lib/flavors.dart*, use the IP address of the device running the backend instead of localhost. For example: http://localhost:9997/v1 turns to http://127.0.0.1:9997/v1 if 127.0.0.1 is your IP. You may also need to allow UDP/TCP connections to port 9997 on the same network in the firewall of the development device. With these steps completed the app can be ran on a physical device using a local deployment of the backend.

### Activating your device

To be able to use the app a Device user needs to be created. One way to do this is using the previously set up Tenant Admin Console.

* Log in with the previously created admin user
* Head to "Register device"
* Submit the form (All fields are purely for your own identification, no need to fill in correct values)
* Head to "Manage device"
* Click on "GENERATE DEVICE TOKEN" next to your newly created device
* Confirm the creation of the token
* Save the token somewhere safe

Alternatively the *getAppDeviceToken.sh* script in the *scripts* directory of the *katapp-backend* repository can be used to generate a default token. This can be used if you do not want to interact with the Tenant Admin Console. A new device will be generated for you with default values if there is no existing device.

Once you have obtained the token from either the Tenant Admin Console or the script paste it into the KatApp for device activation.