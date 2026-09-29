# DRAMORA Release Package

This package contains the DRAMORA Android app shell, the connected web app, and launch documentation.

## Current architecture
- Android WebView shell
- Supabase Auth + Postgres + Storage
- Published-series / published-episode model
- My List and watch-history sync
- Vertical video playback

## Important licensing gate
The database currently contains placeholder series marked `draft`. Do not publish or upload third-party episodes until written distribution rights are confirmed.

## Build
Open this folder in Android Studio with JDK 17 and Android SDK 35 installed. Let Gradle sync, then Build > Build APK(s). A signed release build requires your own Android signing key.

## Before public release
1. Replace placeholder content with cleared/licensed titles.
2. Set a real DRAMORA support email/domain in the app/legal pages.
3. Review privacy policy and terms with appropriate legal advice.
4. Test authentication, playback, progress, My List, and offline/poor-network behavior.
5. Create and securely store a release signing key.
6. Build a signed release APK.
7. Test the exact signed APK on multiple Android devices.
