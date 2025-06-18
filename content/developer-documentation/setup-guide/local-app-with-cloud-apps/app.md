+++
title = "App"
weight = 2
+++

## Setting up the App to use the Cloud Backend

### Web Setup

The easiest way to test the app is using the web build with Docker:

```
docker-compose up
```

This builds the app and starts a webserver at http://localhost:5000. By default, the web build uses the local backend. To use a cloud endpoint instead, modify the `default` value in `/lib/flavors.dart` to your desired cloud URL (DEV distribution recommended).

Alternatively, with Flutter SDK installed locally:

```
flutter config --enable-web
flutter pub get
flutter run -d chrome --web-port 5000
```

Note: Port 5000 is required due to backend CORS and Origin Controls.

Press `r` in the console to hot-reload changes without rebuilding.

#### CORS Issues

If you encounter CORS errors, launch Chrome with web security disabled:

Windows:
```
cd C:\Program Files (x86)\Google\Chrome\Application
chrome.exe --disable-web-security --user-data-dir=c:\my-chrome-data\data
```

Mac:
```
open -n -a /Applications/Google\ Chrome.app/Contents/MacOS/Google\ Chrome --args --user-data-dir="/tmp/chrome_dev_sess_1" --disable-web-security
```

### Mobile Setup

With Flutter SDK installed, you can run the app directly in an emulator or on your physical device.

For macOS users: Use Android emulator or physical device testing since iOS simulator doesn't support camera mocking. Android emulators can use your development machine's webcam (configure in emulator settings).

To run on your development device:

```
flutter pub get
flutter run --flavor dev -t lib/main-dev.dart --debug
```

This automatically connects to the cloud DEV API. Note: Be cautious when testing on live deployments.

### Device Activation

1. Go to [Tenant Admin Console](https://admin.dev.katapp.org/login)
2. Log in with provided credentials
3. Navigate to *Register Device* and create a new device entry
   - For testing, any unique identifier is sufficient
4. Go to *Manage Device*
5. Find your device and click *GENERATE DEVICE TOKEN*
6. Use the generated token to activate the app