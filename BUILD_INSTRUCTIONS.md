# How to Build APK

## Option 1: Using GitHub Actions (Recommended - No Installation Required)

1. **Fork this repository** to your GitHub account
2. Go to the **Actions** tab in your forked repository
3. Enable GitHub Actions if prompted
4. Click on **"Build APK"** workflow
5. Click **"Run workflow"** button
6. Wait for the build to complete (~5 minutes)
7. Download the APK from the **Artifacts** section

## Option 2: Build Locally (Requires Android Studio)

### Step 1: Install Android Studio
1. Download from: https://developer.android.com/studio
2. Run the installer
3. Follow the setup wizard (it will install Java + Android SDK)

### Step 2: Accept Android Licenses
```bash
flutter doctor --android-licenses
```
Press `y` to accept all licenses

### Step 3: Build the APK
```bash
flutter build apk --release
```

The APK will be at: `build/app/outputs/flutter-apk/app-release.apk`

## Option 3: Install on Device via USB (Easiest for Testing)

1. Enable **Developer Options** on your Android device:
   - Go to Settings > About Phone
   - Tap "Build Number" 7 times
   
2. Enable **USB Debugging**:
   - Go to Settings > Developer Options
   - Enable "USB Debugging"

3. Connect your device via USB

4. Run:
```bash
flutter devices
flutter run --release
```

This will install and run the app directly on your device!

## Current Build Status

The project uses:
- Flutter SDK
- Google Maps
- Geolocation
- Route planning features

For issues, check `flutter doctor` output.
