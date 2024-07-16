+++
title = "App"
weight = 2
+++

## Setting up the App to use the Cloud Backend

### Web Setup

The easiest way to test the app is by using the web build. To run the app without installations Docker can be used.

```
docker-compose up
```

This will build the app and start a webserver listening at http://loalhost:5000. The web build will automatically use the local backend unless specified otherwise. This can be changed in file */lib/flavors.dart*. Here, change the *default* value to the URL of the cloud endpoint you want to use for testing. This will usually be one of the two other URLs visible in the file. Use of the DEV distribution is recommended in most cases.

If the Flutter SDK is installed locally, the App can also be started with the following commands:

```
flutter config --enable-web
flutter pub get
flutter run -d chrome --web-port 5000
```

Port 5000 is important due to CORS and Origin Controls defined in the backend.

By pressing r in the console window while the app is running it's possible to display changes without needing to rebuild the app.

### Mobile Setup

If the Flutter SDK is installed locally on your system, the app can also be run directly in an emulator.

The app can be tested either on device using the installed emulator or on your phone. If you are planning on testing the app on a macOS device in flutter it is recommended to either use the android emulator or instead test the app directly on your phone. This is due to the fact that the iOS emulator on macOS does not support camera mocking.

To test the mobile app on your development device without setup of a local environment run the flutter app with the following command:

```
flutter pub get
flutter run --flavor dev -t lib/main-dev.dart --release
```

This will automatically set up the app to access the cloud DEV API unless specified otherwise. This fully set-up environment will enable you to experiment with the app. Be mindful of testing the application on a live deployment.

### Activating your device

To active your device, generate a token with the [Tenant Admin Console](https://admin.dev.katapp.org/login). Log in using the previously provided login information. Head to *Register Device* and type in fitting information to set up your device. The information entered for the registration does not need to be correct for testing, as long as the entry is uniquely identifiable and can be attributed to its creator. Once registered, head over to *Manage Device*. Find the newly created device and press *GENERATE DEVICE TOKEN*. Use the generated Token to activate the app.