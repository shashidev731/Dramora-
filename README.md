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

## v1.1 changes
- Android 15 edge-to-edge fix (content no longer sits under the status bar); keyboard-safe login.
- App no longer jumps back to Home on background token refreshes; safer genre buttons.
- "Forgot password" in the app + `reset.html` page (host with GitHub Pages).
- New standalone admin (`admin/index.html`): own sign-in, edit/delete series and episodes, publish confirmations, upload size limits, escaped output, visible errors.
- Supabase library pinned to an exact version.

## One-time Supabase setup (dashboard)
1. Authentication > Emails > SMTP Settings: add a custom SMTP provider (built-in email is heavily rate limited).
2. Authentication > URL Configuration > Redirect URLs: add `https://shashidev731.github.io/Dramora-/**`.
3. Run the policy audit query (see chat) and confirm only admins can write to series/episodes/storage and drafts are not readable by anon.
