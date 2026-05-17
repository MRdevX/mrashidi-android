# mrashidi-android

Android app for [mrashidi.me](https://mrashidi.me), built as a [Trusted Web Activity (TWA)](https://developer.chrome.com/docs/android/trusted-web-activity) using [Bubblewrap](https://github.com/GoogleChromeLabs/bubblewrap).

## Requirements

- [Node.js](https://nodejs.org) 18+
- [Bubblewrap CLI](https://www.npmjs.com/package/@bubblewrap/cli) — `npm install -g @bubblewrap/cli`
- Android SDK (via Android Studio or standalone)
- JDK 17 (e.g. via [sdkman](https://sdkman.io))

## Setup

On first run, Bubblewrap will configure the Android SDK and JDK paths:

```bash
bubblewrap doctor
```

## Build

```bash
bubblewrap build
```

Outputs:
- `app-release-signed.apk` — signed APK for direct install/testing
- `app-release-bundle.aab` — app bundle for Google Play submission

## Signing

The keystore file (`android.keystore`) is excluded from version control. Keep it backed up securely — it is required to publish updates to Google Play.

## Update

When the web app changes (manifest, icons, theme color), re-run:

```bash
bubblewrap update
bubblewrap build
```
