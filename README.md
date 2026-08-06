<p align="center">
  <a href="https://sipario.tv">
    <img src="https://sipario.tv/favicon.svg" alt="Sipario" width="88">
  </a>
</p>

# Sipario Releases

Public downloads for [Sipario](https://sipario.tv), a native media player for
sources you provide. Sipario hosts no media and requires no account.

## What Sipario does

- Native playback with hardware decoding for 4K, HDR, Dolby Vision, broad audio,
  and text or bitmap subtitles.
- Exact resume, Continue Watching, track memory, Skip Intro/Credits, and Up Next.
- User-provided Stremio-compatible add-ons, M3U/Xtream, local or NAS media, and
  Jellyfin/Emby libraries.
- Encrypted device pairing and sync without a Sipario account.

Feature and format support varies by platform, device, and connected display.

## Download

| Platform | Download | Status |
|---|---|---|
| Android TV / Google TV | [Sipario-TV.apk](https://sipario.tv/download/tv) | Stable sideload build |
| macOS | [Sipario-macos.dmg](https://sipario.tv/download/mac) | Stable |
| Windows | [Sipario-windows.msi](https://sipario.tv/download/windows) | Alpha |

Android TV users can also open Downloader and enter code **5358756**.

[Latest release notes](https://github.com/Aiml3ss/sipario-releases/releases/latest)

## Install notes

- **Android TV:** sideload the APK. Existing installs update in place.
- **macOS:** drag Sipario to Applications. The current build is not notarized;
  Control-click the app and choose **Open** on first launch.
- **Windows:** the alpha is unsigned. SmartScreen may require **More info → Run
  anyway**.
- **Apple TV:** native alpha exists, but no public download is distributed here.

## Repository purpose

This repository contains release assets only—not Sipario source code. Every
latest release carries these stable filenames so website downloads and app
updaters keep working:

- `Sipario-TV.apk`
- `Sipario-macos.dmg`
- `Sipario-windows.msi`
- `world-news.m3u8`

## Problems

[Open an issue](https://github.com/Aiml3ss/sipario-releases/issues) for a broken
download or released-build problem. Include platform, app version, device, and
reproduction steps.
