# BLUTOOTH Audio Studio

Android audio-customisation prototype, version 0.1.0.

## Prototype features
- Local audio-file playback
- Android platform Equalizer effect (band count varies by device)
- Android BassBoost effect where supported
- Bluetooth audio output status display
- Dark UI
- GitHub Actions workflow that builds a debug APK

## Important limitations
- Equalizer and bass boost apply to audio played through this app, and are dependent on the device's Android audio-effect implementation.
- This prototype does not provide guaranteed system-wide EQ for YouTube, Spotify, games, or other apps.
- Bluetooth output status is informational; it does not pair/connect devices or control proprietary headphone features.
- Test on a real Android phone. Emulator audio-effect support may differ.

## Build locally
1. Install Android Studio and Android SDK Platform 35.
2. Open this folder in Android Studio and allow Gradle sync.
3. Build > Build Bundle(s) / APK(s) > Build APK(s).

Alternatively, with JDK 17 and Gradle installed:
```bash
gradle assembleDebug
```
APK output:
`app/build/outputs/apk/debug/app-debug.apk`

## Build on GitHub
1. Create a new GitHub repository.
2. Upload/push all files from this project to the repository's `main` branch.
3. Open the repository's **Actions** tab.
4. Select **Build Android APK** and run the workflow, or push a commit to `main`.
5. Open the successful workflow run and download the `BLUTOOTH-Audio-Studio-debug-apk` artifact.
6. Extract the downloaded artifact ZIP to get `app-debug.apk`.

This is a debug/test APK, not a Play Store release.
