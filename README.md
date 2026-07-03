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
| Android TV | [Download the APK](https://github.com/Aiml3ss/sipario-releases/releases/latest/download/Sipario-TV.apk) | [android-tv-v1.5.10](https://github.com/Aiml3ss/sipario-releases/releases/tag/android-tv-v1.5.10) |

Stable website links:

- <https://sipario.tv/download/mac>
- <https://sipario.tv/download/tv>

## What You Get

Sipario is a native media player for your own sources — built around the player,
not a catalog.

- **Plays what other apps refuse.** libmpv (ffmpeg) at the core decodes the
  codecs, containers, and subtitle formats that send other apps reaching for an
  external player. The TV app picks the engine per source — mpv for the widest
  coverage, the box's own hardware decoder when a title needs true Dolby Vision —
  with automatic fallback.
- **Full fidelity.** Dolby Vision tone-mapping, HEVC/AV1 10-bit, TrueHD/DTS-HD
  lossless decode or receiver passthrough, HDR — handed to real hardware, never
  silently transcoded down.
- **Language, guaranteed.** Preferred audio and subtitle languages are remembered
  and re-applied on every title, so episode two doesn't undo episode one.
- **Built-in polish.** Frame-exact seeks, thumbnail scrub on network streams,
  Skip Intro/Recap/Credits, Up Next for binges, and exact-source resume (same
  release, same second).
- **Native on both.** macOS is SwiftUI around libmpv with a gpu-next shader
  pipeline, on-device Whisper subtitles, picture-in-picture, and self-updates.
  Android TV is Jetpack Compose, remote-first, verified to 4K AV1 on low-cost
  boxes.
- **Live channels.** M3U and Xtream playlists play direct through the native
  player with a guide, plus a public lineup out of the box.
- **Yours, private.** No bundled catalog, no hosted streams, no account, no
  trackers; on-device discovery; end-to-end-encrypted pairing between devices.

## Screenshots

_Desktop app (macOS). Browse, live TV, library, and the native player._

| | |
|---|---|
| ![Home](docs/screenshots/home.jpg) | ![Live TV](docs/screenshots/live.jpg) |
| ![Library](docs/screenshots/library.jpg) | ![Films](docs/screenshots/films.jpg) |

The player — frosted control bar, live HDR badge, in-player menus:

![Player](docs/screenshots/player.jpg)

Full-quality playback through the native mpv pipeline:

![Player playing](docs/screenshots/player-playing.jpg)

## Install Notes

### macOS

Download `Sipario-macos.dmg`, open it, and drag Sipario into Applications.

The current macOS build is not Apple-notarized yet. On first launch, use
Control-click -> Open, or clear the quarantine flag:

```bash
xattr -dr com.apple.quarantine /Applications/Sipario.app
```

### Android TV

Download `Sipario-TV.apk` and sideload it on an Android TV or Google TV device.

With adb:

```bash
adb install -r Sipario-TV.apk
```

The current APK is version `1.5.10` / versionCode `33`. After the first install
the app checks for updates itself, so later versions arrive without another
manual sideload.

## Checksums

```text
Sipario-macos.dmg (macos-v0.41.0)
sha256 bf5a37388b77d584c8f62f1b806b6c5d6d9d06959390154d8f8a7984fe53360f

Sipario-TV.apk (android-tv-v1.5.10)
sha256 4a34dd3ad9d4984fe8053befe10f4dc6dd997eb40fff702aa492755aa0b7af6a
```

## Feedback

Use [Issues](https://github.com/Aiml3ss/sipario-releases/issues) for install
problems, broken downloads, or playback reports from a released build. Include
your platform, app version, device model, and what happened when you pressed
Play.
