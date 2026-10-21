# ChronoX — Android live clock wallpaper starter

This is an original starter project inspired by the *category* of live clock wallpaper apps, not a copy of DepthX branding or assets.

## Included
- Native Android `WallpaperService` that draws a clock directly on the wallpaper surface.
- A simple in-app preview.
- Three clock-style variants, four accent colors, and a locally saved favorite toggle.
- Low-frequency redraw: once per second only while the wallpaper engine is visible.
- Android system wallpaper preview/apply flow.

## Important limitations
- This is source code, **not a compiled APK**. A compatible Android SDK and Gradle build environment are required to build/install it.
- Current style/color preferences are shared via app preferences; Android may run the wallpaper service in a separate process on some devices, so test preference visibility on the target phone.
- The “favorite” toggle currently saves the selected configuration as a simple favorite flag, not a full multi-wallpaper library.
- This starter uses a static dark background with a live clock. It does not yet include video backgrounds, downloadable wallpaper packs, lock-screen-only controls, monetization, or a full wallpaper gallery.
- Actual lock-screen wallpaper support depends on the Android version and device manufacturer. The app requests Android's standard live-wallpaper picker; the user chooses where to apply it.
- Battery-conscious behavior: redraws once per second only when visible, with no continuous animation loop. Avoid high-FPS effects for always-on wallpaper use.

## Build
Open this folder in Android Studio (current stable), let Gradle sync, then select **Build > Build APK(s)**.
Minimum SDK is Android 8.0 (API 26); compile SDK 35.
