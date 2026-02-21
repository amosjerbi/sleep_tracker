# Sleep Tracker Android Widget

Android home-screen widget focused on two quick-glance metrics:
- Time left until your configured wake-up time
- Daily usage/health summary shown in the header (steps/calories/distance variant in current builds)

## Repository Contents

This repository currently stores build/distribution artifacts:

- `app-debug.apk`: Installable debug APK
- `Sleep tracker Android.zip`: Zipped Android Studio project/source
- `output-metadata.json`: APK output metadata

If you want to work on code directly, unzip `Sleep tracker Android.zip` and open it in Android Studio.

## Install the Widget (APK)

1. Transfer/install `app-debug.apk` on your Android device.
2. Long-press home screen and add the widget from the widgets list.
3. Open widget configuration and set your wake-up time.
4. Grant required permissions when prompted (usage access, activity/sensor access depending on build).

## Main Features

- Sleep countdown to wake-up time
- Configurable wake-up time
- Compact side-by-side widget layout
- Tap-to-refresh widget updates
- Screen-time section for top app usage (when usage access is granted)

## Source Development (from ZIP)

1. Unzip `Sleep tracker Android.zip`.
2. Open the project in Android Studio.
3. Sync Gradle.
4. Build debug APK:
   - `./gradlew :app:assembleDebug`

## Permissions Used

- `android.permission.PACKAGE_USAGE_STATS` (via Usage Access settings)
- `android.permission.INTERNET` (for network-based features in some variants)
- Location permissions in weather-enabled variants

## Notes

- Widget behavior and displayed metrics depend on the currently packaged build variant.
- Debug APKs are not intended for Play Store release.
