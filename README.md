<p align="center">
  <a href="https://sipario.tv">
    <img src="https://sipario.tv/favicon.svg" alt="Sipario" width="88">
  </a>
</p>

<h1 align="center">Sipario Releases</h1>

<p align="center">
  Public downloads for the Sipario macOS desktop app and Android TV APK.
</p>

This repository is the public release shelf for Sipario. It intentionally does
not contain the development source tree; active development stays in the private
`Aiml3ss/sipario` repo while binaries ship here.

## Downloads

| Platform | Current Download | Release Notes |
|---|---|---|
| macOS desktop | [Download the DMG](https://github.com/Aiml3ss/sipario-releases/releases/latest/download/Sipario-macos.dmg) | [macos-v0.41.0](https://github.com/Aiml3ss/sipario-releases/releases/tag/macos-v0.41.0) |
| Android TV | [Download the APK](https://github.com/Aiml3ss/sipario-releases/releases/download/android-tv-v1.4.9/sipario-android-tv-v1.4.9.apk) | [android-tv-v1.4.9](https://github.com/Aiml3ss/sipario-releases/releases/tag/android-tv-v1.4.9) |

Stable website links:

- <https://sipario.tv/download/mac>
- <https://sipario.tv/download/tv>

## What You Get

Sipario is a native media player for your own media sources.

- macOS: SwiftUI/AppKit desktop app with libmpv playback, in-window GPU video,
  desktop picture controls, upscaling/filter passes, subtitle controls, and
  self-updates.
- Android TV: native Jetpack Compose app built for the remote, libmpv playback,
  hardware decode, Dolby Vision/HDR handling, audio/subtitle track controls,
  Stream Info, and sideload updates.
- No bundled media catalog, no hosted streams, no account requirement.

## Install Notes

### macOS

Download `Sipario-macos.dmg`, open it, and drag Sipario into Applications.

The current macOS build is not Apple-notarized yet. On first launch, use
Control-click -> Open, or clear the quarantine flag:

```bash
xattr -dr com.apple.quarantine /Applications/Sipario.app
```

### Android TV

Download `sipario-android-tv-v1.4.9.apk` and sideload it on an Android TV or
Google TV device.

With adb:

```bash
adb install -r sipario-android-tv-v1.4.9.apk
```

The APK is version `1.4.9` / versionCode `21`.

## Checksums

```text
Sipario-macos.dmg
sha256 bf5a37388b77d584c8f62f1b806b6c5d6d9d06959390154d8f8a7984fe53360f

sipario-android-tv-v1.4.9.apk
sha256 39985790fa47f7616c28be5a0872db0e417715d1c9a81e59dbdf1af1a5ac68dc
```

## Feedback

Use [Issues](https://github.com/Aiml3ss/sipario-releases/issues) for install
problems, broken downloads, or playback reports from a released build. Include
your platform, app version, device model, and what happened when you pressed
Play.
