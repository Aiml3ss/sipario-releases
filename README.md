<p align="center">
  <a href="https://sipario.tv">
    <img src="https://sipario.tv/favicon.svg" alt="Sipario" width="88">
  </a>
</p>

# Sipario Releases

Public downloads for [Sipario](https://sipario.tv), a private native media
player and library for sources you provide. Sipario hosts no media and requires
no Sipario account.

## Features

### Browse and organize

- Native remote-first TV interfaces and native desktop apps—not a browser
  player wrapped as an app.
- Android TV, macOS, and Windows provide Home, Movies, Series, Search, title
  details, cast, seasons, episodes, collections, similar titles, trailers,
  ratings, and rich metadata. The Apple TV alpha includes Home, Films, Series,
  Search, details, episodes, and ranked source selection.
- Android TV adds Discover, voice search, year/provider filters, an
  upcoming-episode calendar, and Library sorting with poster or list views.
- Continue Watching is available across every native app. Android TV, macOS,
  and the Apple TV alpha return to the same source and position when it remains
  available; Windows restores the position and resolves the source again.
- My Library and watched state are available on Android TV, macOS, and Windows.
  Android TV also provides Start Over. Android TV, macOS, and Windows provide
  Up Next and automatic next-episode playback; Android TV and macOS prefetch the
  next episode.
- Private on-device recommendations learn from viewing and taste ratings on
  Android TV, macOS, and Windows. All three include upcoming-episode calendar
  views; macOS can also send upcoming-episode notifications.
- Ranked source pickers show release quality and details. Android TV prefetches
  and refreshes sources; macOS and Windows can automatically try backup sources
  or switch source and quality in-player without losing the current position.

### Bring your own sources

- Stremio-compatible add-on manifests on every current native app.
- Jellyfin and Emby personal media servers on Android TV, macOS, and Windows.
- Local files and folders on macOS and Windows, including mounted network
  storage; Android TV can browse UPnP/DLNA media servers.
- User-supplied M3U playlists and Xtream accounts for Live TV.
- Optional, removable starter packs for free public channels, world news, and
  public-domain Classic Cinema on Android TV, macOS, and Windows.

### Live TV

- Android TV, macOS, and Windows can add M3U or Xtream sources directly. The
  Apple TV alpha can add M3U directly and receive Xtream setup through encrypted
  pairing.
- Android TV, macOS, and Windows provide a native channel grid, XMLTV EPG
  now/next data, and a time-aligned program guide. Apple TV currently provides
  a basic channel grid.
- Android TV, macOS, and Windows include channel search, favorites, recents,
  group/category filters, and category show/hide tools for large source lists.
  Android TV also includes A–Z sorting; Android TV and macOS include an
  in-player channel guide.
- Multiple Live TV sources load into one interface on Android TV, macOS, and
  Windows. Streams play directly through the native player; sipario.tv does not
  proxy or transcode them.
- macOS and Windows can also browse Xtream movie and series libraries when the
  configured source provides them.

### Playback

- **Android TV:** libmpv hardware playback for HEVC/AV1 10-bit, HDR10/HLG, and
  Live TV; Media3 handles true Dolby Vision. Content frame-rate matching is
  available on compatible hardware.
- **Dolby Vision conversion:** Android TV offers an experimental, off-by-default,
  device-gated conversion for confirmed dual-layer Profile 7 MKVs to
  single-layer Profile 8.1. It rewrites Dolby Vision metadata and drops the
  enhancement layer without re-encoding the base-layer video, with
  converter-aware resume and seeking.
- **macOS:** in-window libmpv with VideoToolbox hardware decode, HDR output,
  TrueHD/DTS-HD decode or HDMI passthrough, thumbnail scrubbing, and a
  Picture-in-Picture-style floating panel. Dolby Vision sources currently play
  their HDR10 base layer.
- **macOS video enhancement:** content-routed chroma reconstruction/downscaling,
  Anime4K for animation, and experimental opt-in MetalFX spatial upscaling for
  supported SDR playback.
- **macOS player extras:** sleep timer, live statistics, aspect adjustment,
  audio/subtitle sync, always-on-top playback, source switching, and automatic
  backup-source failover.
- **Windows alpha:** embedded libmpv with D3D11 hardware decode and display-gated
  HDR10, bounded source failover, highest-quality HLS selection, and manual
  in-player source/quality switching.
- **Apple TV alpha:** AVPlayer handles Apple-native HLS/MP4/MOV; TVVLCKit
  handles MKV, uncommon codecs, and advanced/external subtitles, with fallback
  from AVPlayer to TVVLCKit when needed.
- **SRT subtitles:** Android TV automatically selects preferred-language text
  sidecars from add-ons or OpenSubtitles and can use exact-file hash matching.
  macOS supports OpenSubtitles lookup plus drag-and-drop SRT/ASS files. Windows
  supports embedded tracks and online subtitle results. Apple TV supports
  embedded and external text subtitles.
- **Subtitle controls:** preferred-language selection, remembered track choices,
  timing adjustment, and appearance controls are available on Android TV,
  macOS, and Windows. Apple TV provides preferred-language selection and
  half-second timing adjustment.
- **Player controls:** Android TV and macOS support chapters, playback speed,
  and optional Skip Intro/Recap/Credits markers. Windows adds ±10-second seek,
  frame/chapter stepping, 0.25–4× speed, sleep timer, statistics, fullscreen,
  always-on-top, and PiP. Apple TV provides native remote play/pause,
  ±10-second seek, scrubber, audio-track selection, and subtitle timing.
- **macOS system integration:** media keys, AirPods and Control Center commands,
  system Now Playing, and a menu-bar mini-controller.

### Profiles, sync, and Trakt

- macOS, Android TV, and the Apple TV alpha support optional viewer profiles
  with names, avatars, Kids mode, shared or profile-specific sources, and a
  temporary Guest profile that saves nothing.
- On Android TV and macOS, profiles separate My Library, Continue Watching,
  watched state, progress, taste ratings, recommendations, viewing preferences,
  sources, and Trakt. Apple TV profiles currently separate Continue Watching,
  subtitle preference, sources, and Trakt.
- End-to-end encrypted device pairing transfers supported source configuration
  and credentials without exposing them to the relay. Windows currently imports
  a Jellyfin server and username through pairing but requires the password to be
  entered locally.
- macOS and Android TV continuously sync the household profile list plus each
  active profile's My Library, progress, watched state, taste ratings, and
  shared or profile-specific Stremio add-on choices. Windows syncs My Library;
  Apple TV alpha syncs profiles, add-on choices, source overrides, and progress
  while profiles are enabled.
- On macOS and Android TV, optional Trakt integration imports watched history
  and playback progress, syncs the Trakt watchlist with My Library, marks titles
  watched or unwatched, and scrobbles playback. Windows currently scrobbles;
  Apple TV alpha imports resume progress and scrobbles start/pause/stop.

### Privacy and maintenance

- No Sipario account is required. Sipario has no hosted media, advertising
  tracker, or mandatory telemetry. Media travels directly between your
  configured source and device.
- Recommendations stay on-device. The Sipario pairing and sync relay receives
  ciphertext, not source credentials; credentials are sent only to services you
  configure.
- Apple TV stores credentials in Keychain. Android TV uses Keystore-backed
  storage for Trakt tokens and M3U/Xtream credentials; Stremio URLs, Jellyfin
  tokens, and the sync key remain in app-private preferences. Windows protects
  Trakt tokens with DPAPI; Xtream and Jellyfin credentials remain in its local
  preferences file. Windows crash reports stay local unless you choose to share
  them.
- In-app updates are available on macOS and the Android TV sideload build;
  macOS verifies the downloaded update before installation. Windows currently
  checks for new versions and installs updates manually.

## Platform availability

| Platform | Availability |
|---|---|
| Android TV / Google TV | Beta/early-access sideload APK. Playback is verified on onn 4K Plus; other boxes still need validation. Play Store build is not public yet. |
| macOS | Stable Apple Silicon DMG. Current public dependency bundle requires macOS 26 or newer. |
| Windows | Alpha preview MSI. Signing and wider hardware validation are still in progress. |
| Apple TV | Native alpha. No public build yet; signed hardware and TestFlight validation are pending. |

Feature and format support varies by platform, app version, source, device, and
connected display.

## Download

| Platform | Download | Status |
|---|---|---|
| Android TV / Google TV | [Sipario-TV.apk](https://sipario.tv/download/tv) | Beta sideload build |
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
