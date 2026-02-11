# Flutter Android CI Demo

A Flutter Android app that builds a debug APK via GitHub Actions and uploads it to AutoDevice.

## Build

```bash
flutter pub get
flutter build apk --debug
```

The output APK is at `build/app/outputs/flutter-apk/app-debug.apk`.

## CI/CD

The GitHub Actions workflow (`.github/workflows/build.yml`) runs on every push to `main`:

1. Sets up Flutter 3.27.4
2. Builds a debug APK with `flutter build apk --debug`
3. Uploads the APK to AutoDevice

## Required Secrets

- `AUTODEVICE_API_KEY` — AutoDevice API key for uploading builds
