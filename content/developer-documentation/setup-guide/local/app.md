+++
title = "App"
weight = 4
+++

## Local App Setup

### Web Setup

The easiest way to test the app is using the web build with Docker:

```bash
docker-compose up
```

This starts a webserver at http://localhost:5000. The web build automatically uses the local backend.

Alternatively, with Flutter SDK installed locally:

```bash
flutter config --enable-web
flutter pub get
flutter run -d chrome --web-port 5000
```

> **Note**: Port 5000 is required due to CORS and Origin Controls in the backend.

Press `r` in the console to hot-reload changes without rebuilding.

### Mobile Setup

#### Emulator Testing

The app can be tested on an emulator or physical device. For macOS users:
- Use Android emulator or physical device
- iOS simulator doesn't support camera mocking
- Android emulator can use your webcam (configure in emulator settings)

To use local backend with emulator:

1. Edit `/lib/flavors.dart`
2. Replace both `Flavor.DEV` and `Flavor.PROD` URLs:
   - For Android emulator: `http://10.0.2.2:9997/v1`
   - For iOS simulator: `http://localhost:9997/v1`

> ⚠️ **Warning**: Don't commit these changes! They'll break production builds.

Run the app:
```bash
flutter pub get
flutter run --flavor dev -t lib/main-dev.dart --debug
```

#### Physical Device Testing

Requirements:
- Device and development machine on same network
- Backend running and accessible
- Firewall allowing port 9997

In `/lib/flavors.dart`, replace `localhost` with your machine's IP:
```
http://YOUR_IP:9997/v1
```

### Device Activation

You need a device token to use the app. Get one via:

#### Option 1: Tenant Admin Console

1. Log in as admin
2. Go to "Register device"
3. Fill form (values are for your reference only)
4. Go to "Manage device"
5. Click "GENERATE DEVICE TOKEN"
6. Save the token securely

#### Option 2: Script

Use `getAppDeviceToken.sh` in `katapp-backend/scripts/` to generate a default token. This creates a new device if none exists.

Paste the token into KatApp to activate your device.